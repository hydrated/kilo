# kilo
keystone container in Openstack kilo

The idea is to build a docker container with only the most essential components in Openstack, 
e.g.; keystone, rabbitmq, and mariadb.

After pulling and running the image, one should have a controller node running keystone, rabbitmq, mariadb and sshd, 
with pre-configured settings almost identical to official installation guide for Openstack Kilo, except for simplified 
password settings.

This is intented for use in development where one may connect to, deploy on, or write within the container.
Definitely NOT to be used in production due to little password protection.

At the time of development, I had not known that one may do automated builds using git repository, so I spent
quite amount of efforts absorbing all the config files into Dockerfile. But since almost everything is just a 
direct copy from official guide, it may be more favorable this way since one doesn't need to worry about hidden
configs. Everything is plain in the Dockerfile, except some minor tweaks needed for automation.

If you just want to skip the tedius configs and get your hands on a working minimal Openstack controller, then 
this is the image for you.
