pipeline {
    agent any

    stages {
        stage('initialize') {
            steps {
                sh 'terraform init -no-color'
            }
        }
        stage('format the code') {
            steps {
               sh 'terraform fmt -no-color'
            }
        }
         stage('validate') {
            steps {
                sh 'terraform validate -no-color'
            }
        }
     stage('plan') {
            steps {
                sh 'terraform plan -no-color -destroy'
            }
        }
    }        
}
