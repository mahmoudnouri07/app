 pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            credentialsId: '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',
                            url: 'https://github.com/mahmoudnouri07/app.git']]])
                }
            }
        } 
        
        }
        
               stage('docker')
{
                  steps {
                         script{
                         sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml "
                                }
                        }
  }
        }
