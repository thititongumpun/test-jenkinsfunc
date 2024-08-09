pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    def files = findFiles(glob: 'deploy/*.sql')
                    def filesDir = files.join(',')
                    def filesArr = filesDir.tokenize(',')
                    println filesDir
                    println filesDir == ''
                    println filesArr.getClass()
                }
            }
        }
    }
}
