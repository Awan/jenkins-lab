# jenkins-lab
Practice jenkins in local environment. 

### Requirements

docker-compose



### How to?

### Clone repo and run the jenkins container:

```bash
git clone https://github.com/Awan/jenkins-lab.git
cd jenkins-lab
docker-compose up -d
```

### Finalize the installation

Get root password:

```bash
docker logs jenkins-master
```

Go to http://localhost:8080 and login with the password you just got from logs.

After login, install suggested plugins.

In case you get some errors like: 

```
"An error occurred during installation: No such plugin: cloudbees-folder"
```

Edit and replace `https` with `http` in `/var/lib/docker/volumes/my-jenkins-project_jenkins_home/_data/hudson.model.UpdateCenter.xml`.
