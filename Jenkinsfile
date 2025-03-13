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
                        lastLine > output.json
                    }

                    // def newFile = new File("output.json")
                    // newFile.write("${lastLine}")

                    // def output = readJson("${WORKSPACE}/output.json")
                    // echo "Printing total number of high vuln: ${output.data.vulnerabilities.high}"
                    echo "Printing the last line: ${lastLine}"
                    // list.eachLine { line -> 
                    //     echo "Line: ${line}"
                    // }
                }
            }
        }
    }
}