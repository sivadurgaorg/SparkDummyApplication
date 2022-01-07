pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Building the code...."  
                bat "mvn clean"
            }
        }
          stage('Compile') { 
            steps {
                echo "Testing the code...." 
                bat "mvn clean compile"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing the code...." 
                bat "mvn clean test"
            }
        }
        stage('Package') { 
            steps {
                echo "Deploying the project...." 
                bat "mvn clean package"
            }
        }
    }
}
