
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
     ansiblePlaybook installation: 'ansible', inventory: 'dhost.inv', limit: 'http://localhost:8080', playbook: 'apache.yml'
 }
    }
 }
}
