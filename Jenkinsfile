pipeline {
    agent {
        node {
            label 'master'
        }
    }
    stages {
        stage('terraform start') {
            steps {
                sh 'echo "started...." '
            }
        }
        stage('git clone') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/terraform/ && git clone https://github.com/yashas123456/terraform-jenkins'
            }
        } 
        stage('check files') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/terraform/terraform-jenkins'
            }
        }
        stage('terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'terraform plan'
            }
        }
    }
}
