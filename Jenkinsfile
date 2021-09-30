pipeline {
    agent any
    tools {
  terraform 'terraform'
}
stages {
    stage('gitcheckout'){
        steps {
         git credentialsId: 'GitHub', url: 'https://github.com/galamsiva2020/Terraform-with-Jenkins.git'
        }
    }
    stage('Terraform Initialization'){
        steps {
            sh 'terraform init'
        }
    }
    stage('Terraform Showing Plan'){
        steps {
           sh 'terraform plan' 
        }
    }
    stage('Provisioning Resources'){
        steps {
            sh 'terraform apply --auto-approve'
           // sh 'terraform destroy --auto-approve'
        }
    }
}
}
