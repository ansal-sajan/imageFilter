pipeline {
    agent none

    stages {
      //If you are running the pipeline from the SCM then you need not use the Checkout block
        /*stage("Checkout") {
            agent { label "SN1" }
            steps {
                git url: "https://github.com/ansal-sajan/imageFilter.git"
            }
        } */

        stage("Build") {
            agent { label "SN1" }
            steps {
                sh "mvn compile"
            }
        }

        stage("Unit test") {
            agent {label "SN1"}
            steps {
                sh "mvn test"
            }
        }
    }
}
