#!/bin/bash

# Check if the script is run as root
if [ "$(id -u)" -ne 0 ]; then
  echo "Please run this script as root."
  exit 1
fi

# Get the old and new usernames
read -p "Enter the current username: " old_username
read -p "Enter the new username: " new_username

# Find the user's unique identifier (UID)
user_uid=$(id -u "$old_username")

# Change the user's account name
dscl . -change /Users/"$old_username" RecordName "$old_username" "$new_username"

# Change the user's home folder name
mv /Users/"$old_username" /Users/"$new_username"
dscl . -change /Users/"$new_username" NFSHomeDirectory /Users/"$old_username" /Users/"$new_username"

# Update the user's group
dscl . -change /Groups/staff GroupMembership "$old_username" "$new_username"

echo "Username changed from $old_username to $new_username."
