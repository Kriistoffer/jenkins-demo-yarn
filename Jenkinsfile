pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    // def json = readFile(file: "test.json")
                    def file = new FileReader('test.json')
                    
                    file.eachLine { line -> 
                        echo "Line: ${line}"
                    }
                }
            }
        }
    }
}