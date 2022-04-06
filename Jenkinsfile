pipeline {
    agent any
    stages{
        stage('gitcheckout') {
            steps {
                echo 'Hello World'
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/suppada/cluster.git']]])
            }
        }
        stage('eks') {
            steps{
                sh 'eksctl create cluster -f eks-cluster.yml --dry-run'
            }
        }
    }
}