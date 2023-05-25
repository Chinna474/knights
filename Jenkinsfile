
 pipeline{
 agent any
 stages{

 stage('code checkout'){
  steps{
      git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/Chinna474/jenkins-ansible.git'
       }
 }

 stage('Execute Ansible'){
  steps{   
      ansiblePlaybook credentialsId: 'ec2-34-216-167-240.us-west-2.compute.amazonaws.com', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dhost.inv', playbook: 'apache.yml'
 }
    }

}
