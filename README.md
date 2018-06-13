# PM-2.5-Air-Quality-Network
Step-by-step instructions of how to build an open-source PM 2.5 air quality sensor network.

Step 1: Raspberry Pi Basic Setup
  
  ::: INSTALL THE RASPBIAN OPERATING SYSTEM :::
  - Go to https://www.raspberrypi.org/downloads/raspbian/ and download the latest version of Raspbian Stretch with Desktop.
    * The version used for our web server is Kernel 4.14, release date 2018-04-18
  - Use Etcher to Flash the image from the zip file to the microSD card for your Raspberry Pi.
    * https://etcher.io/
    
  ::: INSTALL THE VNC SERVER, CHANGE THE KEYBOARD LAYOUT, CHANGE THE TIMEZONE :::
  - I like to do everything from a VNC, so the next thing to do is go to your Terminal and run the command "sudo apt-get update".
    * This is standard procedure anytime you install something.
  - Now, run the command "sudo apt-get install realvnc-vnc-server".
  - When that is done, run the command "sudo raspi-config".
    * Next, I will fix the keyboard which is set up to UK standards rather than US.
      + Select "Localisation Options".
      + Select "Change Keyboard Layout".
        - My keyboard automatically updated to the correct configuration, if yours does not then just follow the prompts.
    * Also, let's fix the Timezone.
      + Select "Localisation Option".
      + Select "Change Timezone".
        - Follow the prompts, I selected "US", "Central".
    * Finally, let's do what we came to do and enable VNC Server.
      + Select "Interfacing Options".
        - Select "VNC" and Enable it.
  - An Icon should have appeared in the upper-right hand corner with the letters "vnc" in a square, click this icon.
    * Sign in or create an account by following the link to start VNC Server.
    * Install VNC Viewer on any computer you would like to log-in to the raspberry pi from.
      + When it is time to login, the default username and password on your pi is user: "pi" password "raspberry".
        - Awesome! Now, we have the capability for remote access!

  ::: CHANGE THE DEFAULT USERNAMES AND PASSWORDS :::
  - From the terminal, use the command "sudo passwd root" to change the root user password.
    * Change the password to whatever you would like.
    * Click the Raspberry at the top-right corner, go to "Shut Down", then select "Logout".
      + If you are logged in remotely, this will not log you off.
    * Change the user from "pi" to "Other...".
    * Login with the username: "root" and the password that you set.
  

Step 2: The Apache Web Server
  - From the terminal, run the command "sudo apt-get update".
  - Run the command sudo apt-get install apache2 -y
    * Great! Now, we have a web server.  From your raspberry pi, you can go to http://localhost/ to access your website!

Step 3: Install PostGRE SQL instructions.

Step 4: Install PHP
  - From the terminal run the command "sudo apt install php7.0 php7.0-pgsql
