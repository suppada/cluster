pipeline {
    agent any
    stages{
        stage ('git-checkout'){
            steps{
                sh 'eksctl create cluster -f eks-cluster.yml --dry-run'
            }
        }
    }
}