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
     stage('Deploy Voting App with alb ') {
        steps {
         sh 'aws eks --region us-east-1 update-kubeconfig --name ridiculous-painting-1683146421'
         sh 'ls -al'
         sh 'kubectl delete -f voting-with-ingress.yml'
         sh 'kubectl delete -f ingress.yml'
         sh 'kubectl get pods,svc,ingress'
        }         
     }
    }
}