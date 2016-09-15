#Setup ssh keys

This is needed to log into an ssh server with a more secure connection without prompting for a password.   

-> In local machine do:   
$ cd ~   
$ ssh-keygen -t rsa   
[Enter every prompt, don't change anything]   

$ ssh-copy-id user@machine-ip   
[Type user password when prompted]   

You are all setted up, run the following command:   
$ ssh user@machine-ip   
Verify that you can ssh without password
