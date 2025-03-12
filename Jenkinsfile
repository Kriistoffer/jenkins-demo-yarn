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
                        json.split("\r?\n")[2]
                        echo "Printing... ${json}"
                    }
                }
            }
        }
    }
}