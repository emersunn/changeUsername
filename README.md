# Change Username Script for macOS

This shell script allows you to change a user account name on macOS. It requires administrator privileges to execute and can cause issues if not done correctly. Always have a backup of your data before making any changes.

## Requirements

- macOS
- Administrator access

## Usage

1. Clone this repository or download the `change_username.sh` script.
2. Open Terminal.
3. Navigate to the directory containing the `change_username.sh` script.
4. Make the script executable by running the following command:
```
chmod +x change_username.sh
```

5. Run the script with root privileges using:
```
sudo ./change_username.sh
```

6. Follow the prompts to enter the current and new usernames.

## Warning

This script does not update references to the old username in configuration files, application settings, or other locations. It's essential to test the system thoroughly after making these changes to ensure that everything is working correctly.
