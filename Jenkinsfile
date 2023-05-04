pipeline {
    agent any
    environment {
        PROJECT = "WELCOME TO K8S B18 BATCH - Jenkins Class"
    }
    stages {
     stage('Check The Kubernetes Access') {
        steps {
         sh 'aws eks --region us-east-1 update-kubeconfig --name ridiculous-painting-1683146421'
         sh 'kubectl get pods -A'
         sh 'kubectl get ns'
        }
      }
     stage('Deploy Voting App') {
        steps {
         sh 'aws eks --region us-east-1 update-kubeconfig --name ridiculous-painting-1683146421'
         sh 'ls -al'
         sh 'kubectl apply -f voting-with-ingress.yml'
         sh 'kubectl apply -f ingress.yml'
         sh 'kubectl get pods,svc,ingress'
        }         
     }
    }
}