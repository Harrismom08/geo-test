pipeline {
    agent any 
    stages{
        stage('maven clean'){
            tools{
                maven 'M2_HOME'
            }
                sh 'mvn clean'
            }
        }
        stage('maven install'){
            stage{
                sh 'mvn install'
            }
        }
        stage('maven package'){
            steps{
               sh 'mvn package'
            }
        }
        
    }
