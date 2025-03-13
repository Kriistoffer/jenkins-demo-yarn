pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    def json = readFile(file: "test.json")
                    
                    json.eachLine { line -> 
                        echo "Printing.... ${line}"
                    }
                }
            }
        }
    }
}