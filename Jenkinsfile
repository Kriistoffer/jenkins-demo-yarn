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
                        int num = sh "wc -l test.json"
                        echo "${num}"
                        String line = readLine(json, num)
                    }
                }
            }
        }
    }
}