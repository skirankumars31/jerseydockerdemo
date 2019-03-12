node() {

currentBuild.result = "SUCCESS"

    try {

       stage('Checkout'){

          checkout scm
       }

       stage('Run Docker'){

           bat "docker build -t myapp -f Dockerfile ."
       }

    }
    catch (err) {

        currentBuild.result = "FAILURE"
        throw err
    }

}