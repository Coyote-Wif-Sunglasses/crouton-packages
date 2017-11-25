**Disable "module_locking" for being able to load external modules on chromeos**

For being able to load modules outside /lib/modules from chromeos we will need to disable module_locking.
This can be done by changing the kernel flags. I wrote a little script that does this for you and also has the option to revert the changes.  
Open a **crosh** shell and follow on screen instructions:
```
$ cd ~/Downloads
$ curl https://raw.githubusercontent.com/divx118/crouton-packages/master/change-kernel-flags -o change-kernel-flags
$ sudo mkdir -p /usr/local/bin
$ sudo cp ~/Downloads/change-kernel-flags /usr/local/bin
$ sudo chmod +x /usr/local/bin/change-kernel-flags
$ sudo change-kernel-flags
```
When running `sudo change-kernel-flags -h` it will give you the usage. 
When you want to revert the changes so put back a backup kernel use -r  
`sudo change-kernel-flags -r`  

**Note:** You will need to repeat the above steps after each chromeos update.


=============================================================================

 
  
   
   



**Virtual box modules and the repo is currently broken https://github.com/divx118/crouton-packages/issues/45 the change-kernel-flags script to disable "module_locking" mentioned above still works**

