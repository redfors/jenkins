#!groovy
// Check ub1 properties
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
        stage("First step") {
            steps {
                sh 'ssh root@194.92.67.92 \'hostname\''
            }
        }
        stage("Second step") {
            steps {
                sh 'ssh root@194.92.67.92 \'uptime\''
            }
        }
    }
}