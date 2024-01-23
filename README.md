1.	What is Jenkins?
Jenkins is an open source automation tool written in Java programming language that allows continuous integration.
Jenkins builds and tests our software projects which continuously making it easier for developers to integrate changes to the project, and making it easier for users to obtain a fresh build.
It also allows us to continuously deliver our software by integrating with a large number of testing and deployment technologies.
Jenkins offers a straightforward way to set up a continuous integration or continuous delivery environment for almost any combination of languages and source code repositories using pipelines, as well as automating other routine development tasks.
With the help of Jenkins, organizations can speed up the software development process through automation. Jenkins adds development life-cycle processes of all kinds, including build, document, test, package, stage, deploy static analysis and much more.
Jenkins achieves CI (Continuous Integration) with the help of plugins. Plugins is used to allow the integration of various DevOps stages. If you want to integrate a particular tool, you have to install the plugins for that tool. For example: Maven 2 Project, Git, HTML Publisher, Amazon EC2, etc.
For example: If any organization is developing a project, then Jenkins will continuously test your project builds and show you the errors in early stages of your development.
Possible steps executed by Jenkins are for example:
•	Perform a software build using a build system like Gradle or Maven Apache
•	Execute a shell script
•	Archive a build result
•	Running software tests
2.	Work Flow:
 
History of Jenkins
Kohsuke Kawaguchi, who is a Java developer, working at SUN Microsystems, was tired of building the code and fixing errors repetitively. In 2004, he created an automation server called Hudson that automates build and test task.
In 2011, Oracle who owned Sun Microsystems had a dispute with Hudson open source community, so they forked Hudson and renamed it as Jenkins.
Both Hudson and Jenkins continued to operate independently. But in short span of time, Jenkins acquired a lot of contributors and projects while Hudson remained with only 32 projects. Then with time, Jenkins became more popular, and Hudson is not maintained anymore.
What is Continuous Integration?
Continuous Integration (CI) is a development practice in which the developers are needs to commit changes to the source code in a shared repository at regular intervals. Every commit made in the repository is then built. This allows the development teams to detect the problems early.
Continuous integration requires the developers to have regular builds. The general practice is that whenever a code commit occurs, a build should be triggered.
Continuous Integration with Jenkins
Let's consider a scenario where the complete source code of the application was built and then deployed on test server for testing. It sounds like a perfect way to develop software, but this process has many problems.
o	Developer teams have to wait till the complete software is developed for the test results.
o	There is a high prospect that the test results might show multiple bugs. It was tough for developers to locate those bugs because they have to check the entire source code of the application.
o	It slows the software delivery process.
o	Continuous feedback pertaining to things like architectural or coding issues, build failures, test status and file release uploads was missing due to which the quality of software can go down.
o	The whole process was manual which increases the threat of frequent failure.
AD
It is obvious from the above stated problems that not only the software delivery process became slow but the quality of software also went down. This leads to customer dissatisfaction.
So to overcome such problem there was a need for a system to exist where developers can continuously trigger a build and test for every change made in the source code.
This is what Continuous Integration (CI) is all about. Jenkins is the most mature Continuous Integration tool available so let us see how Continuous Integration with Jenkins overcame the above shortcomings.
Let's see a generic flow diagram of Continuous Integration with Jenkins:
AD
 

 
Let's see how Jenkins works. The above diagram is representing the following functions:
o	First of all, a developer commits the code to the source code repository. Meanwhile, the Jenkins checks the repository at regular intervals for changes.
o	Soon after a commit occurs, the Jenkins server finds the changes that have occurred in the source code repository. Jenkins will draw those changes and will start preparing a new build.
o	If the build fails, then the concerned team will be notified.
o	If built is successful, then Jenkins server deploys the built in the test server.
o	After testing, Jenkins server generates a feedback and then notifies the developers about the build and test results.
o	It will continue to verify the source code repository for changes made in the source code and the whole process keeps on repeating.
Advantages and Disadvantages of using Jenkins
Advantages of Jenkins
o	It is an open source tool.
o	It is free of cost.
o	It does not require additional installations or components. Means it is easy to install.
o	Easily configurable.
o	It supports 1000 or more plugins to ease your work. If a plugin does not exist, you can write the script for it and share with community.
o	It is built in java and hence it is portable.
o	It is platform independent. It is available for all platforms and different operating systems. Like OS X, Windows or Linux.
o	Easy support, since it open source and widely used.
o	Jenkins also supports cloud based architecture so that we can deploy Jenkins in cloud based platforms.
Disadvantages of Jenkins
o	Its interface is out dated and not user friendly compared to current user interface trends.
o	Not easy to maintain it because it runs on a server and requires some skills as server administrator to monitor its activity.
o	CI regularly breaks due to some small setting changes. CI will be paused and therefore requires some developer's team attention.
Jenkins Architecture
Jenkins follows Master-Slave architecture to manage distributed builds. In this architecture, slave and master communicate through TCP/IP protocol.
Jenkins architecture has two components:
o	Jenkins Master/Server
o	Jenkins Slave/Node/Build Server
 

Jenkins Master
Main Jenkins server is the Master and its job is to handle:
•	Scheduling build jobs
•	Dispatching builds to the slaves for the actual execution
•	Monitoring the slaves (possibly taking them online and offline as required)
•	Recording and presenting the build results
•	Executing build jobs directly
Jenkins Slave
A Slave is a Java executable that runs on a remote machine. The following are the characteristics of a Jenkins Slave:
•	It hears requests from the Jenkins Master instance.
•	A Slave can run on a variety of operating systems.
•	The job of a Slave is to “obey” the Master, that is, execute build jobs dispatched by it.
•	You can either configure a project to always run on a particular (type of) Slave machine or simply let Jenkins pick the next available Slave.
 
The above diagram is self explanatory. It consists of a Jenkins Master which is managing three Jenkins Slaves.

What is Continuous Delivery Pipeline?
In a Jenkins Pipeline, every job has some sort of dependency on at least one or more jobs or events.
 

The above diagram represents a continuous delivery pipeline in Jenkins. It contains a collection of states such as build, deploy, test and release. These jobs or events are interlinked with each other. Every state has its jobs, which work in a sequence called a continuous delivery pipeline.
A continuous delivery pipeline is an automated expression to show your process for getting software for version control. Thus, every change made in your software goes through a number of complex processes on its manner to being released. It also involves developing the software in a repeatable and reliable manner, and progression of the built software through multiple stages of testing and deployment.


JenkinsFile
Jenkins Pipeline can be defined by a text file called JenkinsFile. You can implement pipeline as code using JenkinsFile, and this can be defined by using a DSL (Domain Specific Language). With the help of JenkinsFile, you can write the steps required for running a Jenkins Pipeline.
The benefits of using JenkinsFile are:
o	You can make pipelines automatically for all branches and can execute pull requests with just one JenkinsFile.
o	You can review your code on the pipeline.
o	You can review your Jenkins pipeline.
o	This is the singular source for your pipeline and can be customized by multiple users.
JenkinsFile can be defined by using either Web UI or with a JenkinsFile.
Pipeline syntax
Two types of syntax are used for defining your JenkinsFile.
o	Declarative
o	Scripted
AD
Declarative:
Declarative pipeline syntax offers a simple way to create pipelines. It consists of a predefined hierarchy to create Jenkins pipelines. It provides you the ability to control all aspects of a pipeline execution in a simple, straightforward manner.
Scripted:
Scripted Jenkins pipeline syntax runs on the Jenkins master with the help of a lightweight executor. It uses very few resources to convert the pipeline into atomic commands.
Both scripted and declarative syntax are different from each other and are defined totally differently.
AD
Why Use Jenkins Pipeline?
Jenkins is a continuous integration server which has the ability to support the automation of software development processes. You can create several automation jobs with the help of use cases, and run them as a Jenkins pipeline.
AD
Here are the reasons why you should use Jenkins pipeline:
o	Jenkins pipeline is implemented as a code which allows several users to edit and execute the pipeline process.
o	Pipelines are robust. So if your server undergoes an unpredicted restart, the pipeline will be automatically resumed.
o	You can pause the pipeline process and make it wait to continue until there is an input from the user.
o	Jenkins Pipelines support big projects. You can run many jobs, and even use pipelines in a loop.
Jenkins Pipeline Concepts
Pipeline: This is the user-defined block, which contains all the processes such as build, test, deploy, etc. it is a group of all the stages in a JenkinsFile. All the stages and steps are defined in this block. It is used in declarative pipeline syntax.
pipeline{  
}  
Node: The node is a machine on which Jenkins runs is called a node. A node block is used in scripted pipeline syntax.
node{  
}  
Stage: This block contains a series of steps in a pipeline. i.e., build, test, and deploy processes all come together in a stage. Generally, a stage block visualizes the Jenkins pipeline process.
Let's see an example for multiple stages, where each stage performs a specific task:
AD
pipeline {  
    agent any  
    stages {  
            stage ('Build') {  
                ...  
            }  
            stage ('Test') {  
                ...  
            }  
            stage ('QA') {  
                ...  
            }  
            stage ('Deploy') {  
                ...  
            }  
            stage ('Monitor') {  
                ...  
            }  
    }  
}  
Step: A step is a single task that executes a specific process at a defined time. A pipeline involves a series of steps defined within a stage block.
pipeline {  
    agent any  
    stages {  
            stage ('Build') {  
                steps {  
                        echo 'Running build phase...'  
                }  
            }  
    }  
}  

Jenkins Pipeline
In Jenkins, a pipeline is a collection of events or jobs which are interlinked with one another in a sequence.
It is a combination of plugins that support the integration and implementation of continuous delivery pipelines using Jenkins.
In other words, a Jenkins Pipeline is a collection of jobs or events that brings the software from version control into the hands of the end users by using automation tools. It is used to incorporate continuous delivery in our software development workflow.
A pipeline has an extensible automation server for creating simple or even complex delivery pipelines "as code", via DSL (Domain-specific language).
A sample Scripted pipeline
node{
stage('Compile'){
			steps {
				echo "Compiled Successfully!!";
			}
		}

	stage('JUnit') {
			steps {
				echo "JUnit Passed Succesfully!";
			}
		}

	stage('Quality-Gate') {
			steps {
				echo "SonarQube Quality Gate passed succesfully!!";
						/*sh exit ("1");*/
			}
		}

	stage('Deploy') {
			steps {
				echo "Pass!";
			}
		}
	}
A sample Groovy script Declarative pipeline
pipeline {
	agent any
	stages {
		stage('Git-Checkout'){
					steps {
						echo "Checking out from Git Repo";
						}
				}

		stage('Build') {
					steps {
						echo "Building the checkedout project!";
						}
				}

		stage('Unit-Test') {
					steps {
						echo "Running JUnit tests";
					}
				}
		stage('Quality-Gate') {
					steps {
						echo "Verifying Quality Gates";
					}
				}

		stage('Deploy') {
					steps {
						echo "Deploying to stage environments for more tests";
					}
				}
		}
	
		post {
			always {
					echo 'This will always run'
				}
			success {
					echo 'This will run only if successful'
				}
			failure {
					echo 'This will run only if failed'
				}
			unstable {
					echo 'This will run only if the run was marked as unstable'
				}
	    		changed {
					echo 'This will run only if the state of the pipeline has changed'
					echo 'For example, if the pipeline was previously failing but is now successful'
				}
   		 }
}


A MASTER-SLAVE Groovy script Declarative Pipeline

pipeline {
	agent none
	stages {
		stage('Non-parallel Stage'){
			agent {
				label "built-in";
				}

			steps {
					echo 'This stage will be executed first';
				}
		}

		stage('Run Tests') {
			parallel {
				stage('Test on Windows') {
					agent {
						label "slave_node1";
					}

					steps {
						echo "Task1 on Agent";
					}
				}

				stage('Test on Master') {
					agent {
							label "built-in";
						}	
					steps {
						echo "Task1 on Master";
					}
				}

				
			}
		}
}
}













Benefits of Ansible
•	Free: Ansible is an open-source tool.
•	Very simple to set up and use: No special coding skills are necessary to use Ansible’s playbooks (more on playbooks later).
•	Powerful: Ansible lets you model even highly complex IT workflows. 
•	Flexible: You can orchestrate the entire application environment no matter where it’s deployed. You can also customize it based on your needs.
•	Agentless: You don’t need to install any other software or firewall ports on the client systems you want to automate. You also don’t have to set up a separate management structure.
•	Efficient: Because you don’t need to install any extra software, there’s more room for application resources on your server.

Ansible playbooks

Ansible Playbooks offer a repeatable, reusable, simple configuration management and multi-machine deployment system, one that is well suited to deploying complex applications. If you need to execute a task with Ansible more than once, write a playbook and put it under source control. Then you can use the playbook to push out new configuration or confirm the configuration of remote systems.
Playbooks can:
declare configurations
orchestrate steps of any manual ordered process, on multiple sets of machines, in a defined order
launch tasks synchronously or asynchronously


Playbook syntax
Playbooks are expressed in YAML format with a minimum of syntax. 
A playbook is composed of one or more ‘plays’ in an ordered list. The terms ‘playbook’ and ‘play’ are sports analogies. Each play executes part of the overall goal of the playbook, running one or more tasks. Each task calls an Ansible module.
EXAMPLE 1

---
- hosts: all
  tasks:
    - name: Print message
      debug:
        msg: Hello Ansible World



EXAMPLE 2

---
- hosts: all
  vars:
    - username: sammy
    - home: /home/sammy   
  tasks:
    - name: print variables
      debug:
        msg: "Username: {{ username }}, Home dir: {{ home }}"

The vars section of the playbook defines a list of variables that will be injected in the scope of that play. All tasks, as well as any file or template that might be included in the playbook, will have access to these variables.


Playbook execution
A playbook runs in order from top to bottom. Within each play, tasks also run in order from top to bottom. Playbooks with multiple ‘plays’ can orchestrate multi-machine deployments, running one play on your webservers, then another play on your database servers, then a third play on your network infrastructure, and so on. At a minimum, each play defines two things:
•	the managed nodes to target, using a pattern 
•	at least one task to execute

EXAMPLE 3
In this example, the first play targets the web servers; the second play targets the database servers.
---
- name: Update web servers
  hosts: webservers
  remote_user: root

  tasks:
  - name: Ensure apache is at the latest version
    ansible.builtin.yum:
      name: httpd
      state: latest

  - name: Write the apache config file
    ansible.builtin.template:
      src: /srv/httpd.j2
      dest: /etc/httpd.conf

- name: Update db servers
  hosts: databases
  remote_user: root

  tasks:
  - name: Ensure postgresql is at the latest version
    ansible.builtin.yum:
      name: postgresql
      state: latest

  - name: Ensure that postgresql is started
    ansible.builtin.service:
      name: postgresql
      state: started
Your playbook can include more than just a hosts line and tasks. For example, the playbook above sets a remote user for each play. This is the user account for the SSH connection.

EXAMPLE 4 



What is Ansible Inventory?
Ansible can work with multiple systems in your infrastructure at the same time. In order to work with multiple servers, Ansible needs to establish connectivity to those servers. This is done with SSH for Linux and PowerShell remoting for windows that would make Ansible agentless. Agentless means you don’t need to install any additional software on the Target machines to be able to work with Ansible. One of the major disadvantages of other automation tools is that you need to install and configure agents on the Target machines before you can invoke any kind of automation. Now the information about these Target systems is stored in a file called an inventory file. If you don’t create a new inventory file Ansible uses its default inventory file located at /etc/ansible/hosts.
Ansible Modules

Modules (also referred to as “task plugins” or “library plugins”) are discrete units of code that can be used from the command line or in a playbook task. Ansible executes each module, usually on the remote managed node, and collects return values. In Ansible 2.10 and later, most modules are hosted in collections.

Ansible modules are standalone scripts that can be used inside an Ansible playbook. A playbook consists of a play, and a play consists of tasks. These concepts may seem confusing if you're new to Ansible, but as you begin writing and working more with playbooks, they will become familiar There are some modules that are frequently used in automating everyday tasks; those are the ones that we will cover in this article.
 
Ansible has three main files that you need to consider:
•	Host/inventory file: Contains the entry of the nodes that need to be managed
•	Ansible.cfg file: Located by default at /etc/ansible/ansible.cfg, it has the necessary privilege escalation options and the location of the inventory file
•	Main file: A playbook that has modules that perform various tasks on a host listed in an inventory or host file
Module 1: Package management
There is a module for most popular package managers, such as DNF and APT, to enable you to install any package on a system. Functionality depends entirely on the package manager, but usually these modules can install, upgrade, downgrade, remove, and list packages. The names of relevant modules are easy to guess. For example, the DNF module is dnf_module, the old YUM module (required for Python 2 compatibility) is yum_module, while the APT module is apt_module, and so on.
Example 1:
- name: install the latest version of Apache and MariaDB
  dnf:
    name:
      - httpd
      - mariadb-server
    state: latest


This installs the Apache web server and the MariaDB SQL database.
Example 2:

- name: Install a list of packages
  yum:
    name:
      - nginx
      - postgresql
      - postgresql-server
    state: present


This installs the list of packages and helps download multiple packages.
Module 2: Service
After installing a package, you need a module to start it. The service module enables you to start, stop, and reload installed packages; this comes in pretty handy.
Example 1:

- name: Start service foo, based on running process /usr/bin/foo
  service:
    name: foo
    pattern: /usr/bin/foo
    state: started
This starts the service foo.
Example 2:	

- name: Restart network service for interface eth0
  service:
    name: network
    state: restarted
    args: eth0
This restarts the network service of the interface eth0.
Module 3: Copy
The copy module copies a file from the local or remote machine to a location on the remote machine.
Example 1:

- name: Copy a new "ntp.conf file into place, backing up the original if it differs from the copied version
  copy:
    src: /mine/ntp.conf
    dest: /etc/ntp.conf
    owner: root
    group: root
    mode: '0644'
    backup: yes

Module 4: Debug
The debug module prints statements during execution and can be useful for debugging variables or expressions without having to halt the playbook.
Example 1:

- name: Display all variables/facts known for a host
  debug:
    var: hostvars[inventory_hostname]
    verbosity: 4
This displays all the variable information for a host that is defined in the inventory file.

