
# you can find Ansible Playbook for the Docker Installation in docker2.yaml file <br>
# In this Ansible playbook I followed below tasks to complete the Docker installation<br>

    ## Install docker packages
    ## Add Docker s official GPG key
    ## Verify that we have the key with the fingerprint
    ## Set up the stable repository
    ## Update apt packages
    ## Install docker
    ## Add remote “ubuntu” user to “docker” group
    ## Install docker-compose

    I use docker to setup jenkens on ec2 and use it here is steps <br>
    1-on ec2 run <br>
      docker pull jenkins/jenkins <br>
    2-to start jenkens run <br>
      docker run -p 8080:8080 -p 50000:50000 -v ~:/var/jenkins_home jenkins/jenkins <br>
    note: <br>
    In this command, the -p option maps the port 8080 on the host to port 8080 in the container, and the port 50000 on the host to port 50000 in the container. The -v option maps the host directory /your/home to the container directory /var/jenkins_home, which is used to store the Jenkins data. <br>
    3-in security group of the instance you must add custom TCP and the port you need to use it for the contaier here is 8080 <br>
    4-finally to expose jenkins use public key of instance and the port you provide for example (35.153.57.16:8080) <br>