pipeline {
    agent any

    stages {
        stage('Maven Version - Check') {
            steps {
                echo "Maven Version - Check"
                sh 'mvn -v'
            }
        }
        
        stage('Jenkins Version - Check') {
            steps {
                echo "Jenkins Version - Check"
                sh 'jenkins --version'
            }
        }

        stage('Docker Version - Check') {
            steps {
                echo "Docker Version - Check"
                sh 'docker --version'
            }
        }

        stage('Kubernetes Version - Check') {
            steps {
                withKubeConfig([credentialsId: 'kube-config']) {
                echo "Kubernetes Version - Check"
                sh 'kubectl version --short'
               }
           } 
        }
    }
 }
