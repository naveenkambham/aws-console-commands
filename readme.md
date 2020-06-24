#### Connecting to ec2 instance:

```
sudo chmod 400 /path/to/key.pem
ssh -i /path/to/key.pem ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com
```

#### To copy a directory from local machine to ec2 instance

```
sudo scp -i /path/to/key.pem -r /Users/directory path/ ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com:/home/ubuntu/directory path/
```

#### To copy a single file from local machine to ec2 instance

```
sudo scp -i /path/to/key.pem /Users/file path/ ubuntu@ec2-**-***-***-***.compute-1.amazonaws.com:/home/ubuntu/file path/
```

#### VIM editor for editing the code on ec2 from terminal 
###### Open the file using VIM:
```
vim  file
```
###### enter the edit mode by pressing 'i' key and use 'Esc' key to exit the edit mode

###### save the file by pressing ':', now the cursor reappear at the lower left. Type x and press "Enter" key to save the file
```
:x
```


###### discard changes by pressing "Esc" and exit the Vim by pressing ':q', follwed by "Enter" 
```
:q
```

#### To change the folder permissions
###### For drwxrwxr-x:
```
chmod 775  the_path_to_target
```
###### For drwxr-xr-x:
```
chmod 755  the_path_to_target
```

#### To create a screen and detach from it, usefull for running flask services in the backend

###### To start your program:
* Log in with ssh,
* Launch screen: ``` $ screen ```
* Start your program:$ ```python3 Loopruns.py```
* Detach from screen using key combination C-A(Ctrl+A) + D, (what's in your screen session will keep running)
* Log out from ssh
###### To check again your program execution:
* Log in with ssh (with the same user as before)
* Re-attach to an existing screen session using $ ```screen -r```

###### Kill all the screens 
```killall screen```

#### Running the process can also be done using process manager, pm2 which can restart the process automatically due to scheduled maintenance etc.  
###### Run the Flask API process using ```pm2 start python3 ml_flask_api.py```
###### Check the status using ```pm2 status```
###### Check the log files if there are any errors using ```pm2 logs```
###### Delete the process using ```pm2 delete process_name```

