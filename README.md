# Splunk Sandbox

Simple Vagrant file to get set up with Splunk environment sufficient
for working through the Splunk training courses.

1. Download latest Enterprise version of splunk to `./data` folder.

  [https://www.splunk.com/en_us/download.html](https://www.splunk.com/en_us/download.html)

2. Edit Vagrantfile to update filename to version just downloaded,
  update the script section and rpm -U command.

3. Run VM provisioned with splunk

        vagrant up

4. First time initialization steps:

        vagrant ssh
        sudo /opt/splunk/bin/splunk enable boot-start --accept-license
        # will require a password to be entered
        sudo systemctl start splunk

5. Login to Splunk web gui

  Initial username is `admin` with the password you chose during initialization.

  [http://localhost:8000/](http://localhost:8000/)

        