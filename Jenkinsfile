pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    def files = findFiles(glob: 'deploy/*.sql')
                    def filesArr = files.join(',').tokenize(',')

                    print files.getClass()
                    println filesArr.getClass()
                    if (filesArr.size() == 0) {
                      println 'empty array'
                    }
                }
            }
        }
        // stage('exception curl') {
        //   steps {
        //     script {
        //       try {
        //           response = sh(script: 'curl http://138.2.78.77:8084', returnStdout: true).trim()
        //           println response
        //       } catch (Exception e) {
        //           println 'error: ' + e
        //           error(e.toString())
        //       }
        //     }
        //   }
        // }
        // stage('validate yml') {
        //   steps {
        //     script {
        //       def content = readYaml file: 'binding-dev.yml'
        //       for (entry in content) {
        //         if (entry.key != 'source_topics') {
        //           println 'no key found'
        //         }

        //         println entry.value
        //       }
        //     }
        //   }
        // }
    }
}
