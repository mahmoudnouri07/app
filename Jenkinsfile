 pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            credentialsId: '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',
                            url: 'https://github.com/ahmedissiou/MyApp.git']]])
                }
            }
        } }}
