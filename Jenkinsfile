pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    def files = findFiles(glob: 'deploy/*.sql')
                    def filesDir = files.join(',')
                    def filesArr = filesDir.tokenize(',')

                    if (filesArr.size() == 0) {
                      println 'empty array'
                    }
                }
            }
        }
    }
}
