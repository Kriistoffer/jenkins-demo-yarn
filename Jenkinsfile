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
                    def lastLine

                    for (item in list) {
                        lastLine = item
                        // lastLine > output.json
                    }

                    echo "Printing the last line: ${lastLine}"

                    def myFile = new File("output.json").write(lastLine)
                    // myFile.write(lastLine)
                    // list.eachLine { line -> 
                    //     echo "Line: ${line}"
                    // }
                }
            }
        }
    }
}