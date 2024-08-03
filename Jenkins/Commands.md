```
mike@jenkins-server:~$ ssh -i /home/mike/.ssh/jenkins_key -l mike -p 8022 jenkins-server help
```
-i flag is used to point to mike's private SSH key. Remember, we have already added the public key in the Jenkins configuration.   
-l is the login user which in our example is mike   
-p is the port which we found out in the previous step to be 8022   

safe restart
```
mike@jenkins-server:~$ ssh -i /home/mike/.ssh/jenkins_key -l mike -p 8022 jenkins-server  safe-restart
mike@jenkins-server:~$
```
installing plugins from cli
```
java -jar jenkins-cli.jar -s http://localhost:8085 -auth 'admin:Adm!n321' install-plugin cloudbees-bitbucket-branch-source
```
```
sudo service jenkins restart
```
