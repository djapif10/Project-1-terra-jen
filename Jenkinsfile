pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                       git branch: 'KbixAug22-winners--branch', url: 'https://github.com/kehbixgit/Augustclass22/'

          }
        }
        
        stage ("terraform init") {
            steps {
                sh ('terraform init') 
            }
        }
         stage ("terraform Validate") {
            steps {
                echo "Terraform action is about to validate code"
                sh ('terraform validate') 
           }
        }
         stage ("terraform fmt") {
            steps {
               sh ('terraform fmt')
           }
        }
        stage ("terraform Apply") {
            steps {
                echo "Terraform action is about to apply"
                sh ('terraform apply --auto-approve') 
           }
        }
