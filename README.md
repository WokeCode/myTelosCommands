# README

This guide will help you set up and use custom scripts for your Contiki NG environment. Follow the steps below to get everything configured and running.

## Commands guide
# makemote
This will create a Makefile and a c file. The files will be created dependant on your current directory so i.e. inside ~/contiki-ng/exercises/hello-world running makemote will create makefile and hello-world.c

# uploadmote
This will run the commands to upload the files in the current directory and log in to the mote

# loginmote
This will log in to the mote

## Setup Instructions

1. **Navigate to the Directory (inside of vagrant):**

    ```sh
    cd /usr/local/bin/
    ```

2. **Clone the Repository:**

    ```sh
    sudo git clone https://github.com/WokeCode/myTelosCommands.git
    ```

3. **Make the Scripts Executable:**

    Run the following commands to set the executable permissions for your scripts:

    ```sh
    sudo chmod +x /usr/local/bin/myTelosCommands/makemote
    sudo chmod +x /usr/local/bin/myTelosCommands/uploadmote
    sudo chmod +x /usr/local/bin/myTelosCommands/loginmote
    ```

4. **Update Your PATH:**

    - Open your shell configuration file in a text editor:

      ```sh
      nano ~/.bashrc
      ```

    - Add the following line to the end of the file:

      ```sh
      export PATH=$PATH:/usr/local/bin/myTelosCommands
      ```

    - Save and close the file:
      - Press `Ctrl+O` to save.
      - Press `Enter` to confirm.
      - Press `Ctrl+X` to exit.

5. **Apply the Changes:**

    Update your current shell session with the new PATH:

    ```sh
    source ~/.bashrc
    ```

6. **Verify the Setup:**

    - Navigate to your Contiki NG exercises directory:

      ```sh
      cd ~/contiki-ng/exercises
      ```

    - Create a test directory:

      ```sh
      mkdir test-exercises
      ```

    - Test the commands:

      ```sh
      makemote
      uploadmote
      ```

      - Press `Ctrl+C` to stop `uploadmote` if it’s running.

      ```sh
      loginmote
      ```

If you follow these steps, your custom commands should be set up and ready to use. If you encounter any issues, ensure that the paths and file permissions are correct.
