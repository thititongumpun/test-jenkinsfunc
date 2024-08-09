pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    def files = findFiles(glob: 'deploy/*.sql')
                    def filesDir = files.join(',')
                    println filesDir
                    println filesDir == ''
                    println filesDir.getClass()
                }
            }
        }
    }
}
