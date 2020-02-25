#!groovy
// Run docker build
properties([disableConcurrentBuilds()])

pipeline {
    agent { 
        label 'master'
        }
    
    options {
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        timestamps()
    }
    stages {
        stage("docker login") {
           
        }
        stage("create docker image") {
            steps {
                echo " ============== start building image =================="
                dir ('docker') {
                	sh 'docker build . '
                }
            }
        }
       
    }
}