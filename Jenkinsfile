pipeline {
    agenty any 
    stages{
        stage('maven clean'){
            tools{
                maven 'M2_HOME'
            }
                sh 'mvn clean'
            }
        }
        stage('maven install'){
            steps{
                sh 'mvn install'
            }
        }
        stage('maven package'){
            steps{
               sh 'mvn package'
            }
        }
        
    }
}