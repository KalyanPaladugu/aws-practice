##### Jenkins connection to aws free tiee account

- Need to create aws free account
- Go to EC2 server and launch instance
    - Name give `jenkin-server`
    - Application and OS images(Amazon Machine Image)
        - Select Amazon linux free tier language
    - Instance type 
        - t3.small --> free tier eligible
    - Key pair and AWS service access
        - Give name it will create two keys
            - Public key store in aws and private key will download to local computer
    - Netork settings
        - Create security group
        - give name and desc
        - Go to security group rule 2
            - Type all trifc
        - Config storage 15gb
        - File systems - none
    - Click on Launch instance
    - Then go to instace and check it it new instance is created or not
- Create local folder and paste downloaded privatekey and open git bash from same path
- Go to newly created instance in EC2 right click and click on connect
- Go to in SSH client(Git bash) and execute all commnds from `how to connect` tab one by one
- check `whoami` in server path
- Google jenkins on AWS check all prerequisite what we doneand Downloading and installing Jenkins by 7 commands 
- Execute final command to start jenkins [ec2-user ~]$ `sudo systemctl start jenkins`
- Go to EC2 instance and then in SSH client copy and paste DNs in browser and give extension`:8080`
- Unlock jenkins screen by type `sudo cat` given path in screen
- You will password and baste in aws screen
- click on install suggested plugins
- create first admin user by filling info and click on finish it will redirect jenkins dashboard

##### Day2 Job Creation

- Left side window we can see some builds failed try to execute `sudo mount -o remount,size=4G /tmp`
- Need to restart jenkins from begining
- Now create a job `job1` with `freestyle porject` initially
- Click on Build now 
    - Entire Build process will handle by `Build Executor Status`
- To create users we need to go setting icon right side of profile it will open Manage jenkins tab
- Then go to security and select users
- Theory of Least previliages(Giving permissions to users)
- To provide access to users got security and select security Realm as `jenkins own user database`
- Types of Authorization
    - Matrix based authorization
    - project based authorization
    - Role based authorization



