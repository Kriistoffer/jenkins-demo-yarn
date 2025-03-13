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
                    // def list = new File("${WORKSPACE}/test.txt").text.readLines()
                    def list = readFile("${WORKSPACE}/test.txt").readLines()

                    for (item in list) {
                        echo "Printing... ${item}"
                    }
                    // list.eachLine { line -> 
                    //     echo "Line: ${line}"
                    // }
                }
            }
        }
    }
}