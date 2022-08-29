pipeline {

agent any 

stages {

stage('install-httpd') {

steps {

sh "yum install httpd -y"

}

}

stage ('service-httpd-start') {

steps {

sh "service httpd start"

}

}

stage ('cp-index-file') {

steps {

sh "cp -r index.html /var/www/html/"

}

}

stage('cp-dev-file') {

steps {

sh "cp -r dev.html /var/www/html/"

}

}

stage ('cp-qa-file') {

steps {

sh "cp -r qa.html /var/www/html/"

}

}

stage ('permission-html') {

steps {

sh "chmod -R 777 /var/www/html/"


}

}

stage('httpd-restart'){

steps {

sh "service httpd restart"

}

}

}

}

