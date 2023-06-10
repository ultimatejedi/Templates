#Ansible-Semaphone
##A GUI interface for Ansible.
I got this idea from Christian's video https://www.youtube.com/watch?v=NyOSoLn5T5U

Make sure and go through to change all of the CHANGE_ME entries.

For the secure access key, you need to generate a new one.  This can be done with the following command:
```sh
head -c32 /dev/urandom | base64
```