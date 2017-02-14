# jenkins-dokku
dokku apps:create jenkins
sudo mkdir /opt/jenkins_home
sudo chmod 777 /opt/jenkins_home/
dokku docker-options:add jenkins deploy,run "/opt/jenkins_home:/var/jenkins_home"
git remote add dokku dokku@dokku.me:jenkins
git push dokku master

