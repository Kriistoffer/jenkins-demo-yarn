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
                    json.tokenize("\r?\n").last()

                    echo "Printing json... ${json}"
                }
            }
        }
    }
}