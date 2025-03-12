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
                    json.split("\r?\n")
                    def lastLine
                    // def lines = json.split("\r?\n")
                    // lines = json.readLines()
                    // def lastLine = lines.get(lines.size()-1)
                    // echo "Printing lines... ${lines}"
                    // echo "Printing lastLine... ${lastLine}"
                    new File("${WORKSPACE}/test.json").eachLine { line -> 
                        lastLine = line
                    }

                    echo "Printing lastline.... ${lastLine}"
                }
            }
        }
    }
}