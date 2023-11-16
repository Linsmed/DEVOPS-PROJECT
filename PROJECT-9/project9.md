### Continous-Integration-Pipeline-For-Tooling-Website

#### DevOps Automation

- Automation is the use of technology to perform tasks with reduced human assistance. Automation helps us accelerate processes and scale environments, as well as build continuous integration, continuous delivery, and continuous deployment (CI/CD) workflows. There are many kinds of automation, including IT automation, business automation, robotic process automation, industrial automation, artificial intelligence, machine learning, and deep learning.

- Theoretically speaking, We could perform DevOps processes like Continuous Integration, Continuous Delivery and log analytics manually. But doing so would require a large team, a lot of time and a level of communication and coordination between team members that is just not realistic in most situations.

- Automation makes it possible to perform these processes using software tools and preset configurations.


#### Benefits of Automation in DevOps

- We have seen earlier releases, in the absence of automation taking years to get into the production and also recently with agile, be it lean, scrum or safe, and with a percentage of automation being improved, release timelines are brought down to few months or weeks.But automation is absolutely a must in order to make the releases as fast as possible in a few hours. So, I think it is impossible to make such quick and frequent releases unless we put in automation in place throughout the pipeline.

- So, quite obviously then, if we want to achieve the objectives of DevOps, high quality and value delivered to customers via frequent and fast deliveries, Automate everything is a must. Clearly, we know by now that automation removes manual errors, dependency on an individual, performs faster, and achieves accuracy thereby achieving consistency and reliability. Hence, automating everything enables the devops objective of high-quality delivery, enables frequent releases and faster releases.

#### In a nutshell, Automation,
- Removes manual errors
- Team members are empowered

- Dependency removed
- Latency removed
- Increases no of deliveries
- Reduces the lead time
- Increases frequency of releases
- Provides faster feedback
- Enables speed, reliability, and consistency.

![](../PROJECT-9/images/ci-cd.png)


#### Acording to Circle CI, Continuous integration (CI) is a software development strategy that increases the speed of development while ensuring the quality of the code that teams deploy. Developers continually commit code in small increments (at least daily, or even several times a day), which is then automatically built and tested before it is merged with the shared repository.

#### In this project, We are required to implement CI for Tooling Website using Jenkins.

- Below is the updated architecture of our infrastructure. Jenkins will be used for continous integration, and its data will be stored on a remote NFS server.

![](../PROJECT-9/images/archit.png)


#### Steps - Prepare the Jenkins server

- Dedicate a new virtual machine for Jenkins(ubuntu 20.04)

- Install JDK (since Jenkins is a Java-based application)


`sudo apt update
sudo apt install default-jdk-headless`

![](../PROJECT-9/images/jdk.PNG)

- Install Jenkins

`wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'
sudo apt update
sudo apt-get install jenkins`

### while trying to install jenkins with the above command ,I was getting error that jekins has no candidate or obsolete so I searched through stack overflow and use the command below to install jenkins

[commands to install jenkins](https://stackoverflow.com/questions/70541720/jenkins-has-no-installation-candidate-error-while-trying-to-install-jenkins-on)




- Make sure Jenkins is up and running

`sudo systemctl status jenkins`

![](../PROJECT-9/images/jenkins.PNG)



- Set Jenkins to listen on port 8080. Access this port with your browser to start configuration

- Login to our brower to configure the Jenkins server

`http://public-ip-address-jenkins-server:8080`

![](../PROJECT-9/images/jenkins%20site.PNG)


- We need to get a password has been written to the log /var/lib/jenkins/secrets/initialAdminPassword To ensure Jenkins is securely set up by the administrator.

` sudo cat /var/lib/jenkins/secrets/initialAdminPassword`

- We need to install the suggested plugins to make or Jenkins work effectively

- Create Admin user and passowrd for login.
![](../PROJECT-9/images/login.PNG)


![](../PROJECT-9/images/config-jenkins.PNG)

![](../PROJECT-9/images/jenkins-url.PNG)

![](../PROJECT-9/images/ready-jenkins.PNG)

![](../PROJECT-9/images/jenkins-dashboard.PNG)

![](../PROJECT-9/images/success.PNG)


- Login to NFS server and ensure the /mnt/opt is exported to allow the Jenkins server make use of the mount.

`sudo showmount -e 172.31.0.10`

