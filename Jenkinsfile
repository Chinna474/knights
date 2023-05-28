
 pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
      git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/Chinna474/knights.git'
       }
 }

 stage('Execute Ansible'){
  steps{   
      ansiblePlaybook credentialsId: 'http://localhost:8080/', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
 }
    }
 }
}
