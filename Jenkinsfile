pipeline {

    agent any

    stages {

        stage('Checkout') {

            steps {

                checkout scm

            }

        }

        stage('Build') {

            steps {

                sh 'mvn clean package'

            }

        }

    }

post {
	success{
	archiveArtifacts artifacts: 'target/*.jar'
	echo "Build Successfull"
}
}
}
 
