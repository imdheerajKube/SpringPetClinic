pipeline{
    agent{label ''}
    tools{maven 'M3'}
    stages{
        stage('CheckOut'){
            steps{
                git branch:'main',url: 'https://github.com/imdheerajKube/SpringPetClinic.git'
                }
        }
        stage('Build'){
            steps{
            bat 'mvn compile'
        }
        }
        stage('Test'){
            steps{
                bat 'mvn test'
            }
        }
        stage('Package'){
            steps {
                bat 'mvn package'
            }
        }
        stage('Deploy'){
            steps {
                bat 'java -jar .//target//*.jar'
            }
        }    
        }
    }
