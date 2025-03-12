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
                        
                        def lines = json.readLines().trim()
                        def lastLine = lines.get(lines.size()-1)
                        echo "Printing lines... ${lines}"
                        echo "Printing lastLine... ${lastLine}"
                    }
                }
            }
        }
    }
}