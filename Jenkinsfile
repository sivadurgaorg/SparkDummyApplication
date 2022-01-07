pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Building the code...."  
                sh "mvn clean"
            }
        }
          stage('Compile') { 
            steps {
                echo "Testing the code...." 
               sh "mvn clean compile"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing the code...." 
                sh "mvn clean test"
            }
        }
        stage('Package') { 
            steps {
                echo "Deploying the project...." 
                sh "mvn clean package"
            }
        }
    }
}
