
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
      ansiblePlaybook credentialsId: 'jenk', installation: 'ansible', inventory: 'dosth.inv', playbook: 'apache.yml'
 }
    }
 }
}
