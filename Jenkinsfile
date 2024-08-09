pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '8a9ffdb9-7d25-48ee-a88e-083d17c3c891', url: 'https://github.com/thititongumpun/test-jenkinsfunc']])
                    def files = findFiles(glob: 'deploy')
                    println files
                }
            }
        }
    }
}
