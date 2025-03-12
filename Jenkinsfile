pipeline {
   agent any
    tools {
        nodejs "nodejs"
    }
    stages {
        stage("NODE") {
            steps {
                script {
                    dir("src") {
                        def json = readFile(file: "test.json")
                        json.trim().split("\r?\n")
                        echo "Printing... ${json.size()}"
                    }
                }
            }
        }
    }
}