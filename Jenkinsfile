pipeline{
    agent any
    stages{
        stage('SCM checkout')
        {
          
            steps{
                git branch: 'main', url: 'https://github.com/abhishekpn99/myansible.git'
            }
        }
        stage('Ansible playbook')
        {
            steps{
                ansiblePlaybook credentialsId: 'private-key1', disableHostKeyChecking: true, installation: 'myansible', inventory: 'de.inv', playbook: 'playbook1.yml'
            }
        }
    }
}
