pipeline {
    agent any 
    tools{
       maven 'maven384'
    }
    stages {
        stage('Build') { 
            steps {
                echo "Building the code...."  
                sh "cd SparkWordCount & mvn clean"
            }
        }
          stage('Compile') { 
            steps {
                echo "Testing the code...." 
               sh "cd SparkWordCount & mvn clean compile"
            }
        }
        stage('Test') { 
            steps {
                echo "Testing the code...." 
                sh "cd SparkWordCount & mvn clean test"
            }
        }
        stage('Package') { 
            steps {
                echo "Deploying the project...." 
                sh "cd SparkWordCount & mvn clean package"
            }
        }
    }
}
