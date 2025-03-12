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
                        
                        def lines = json.readLines()
                        def lastLine = lines.get(lines.size()-2)
                        echo "${lastLine}"
                    }
                }
            }
        }
    }
}