pipeline {
    agent any 
    tools{
        maven "M2_HOME"
       }
       stages{
        stage ('maven clean'){
            steps{
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
        
                stage('upload artifact'){
            steps{
               sh 'nexusArtifactUploader artifacts: [[artifactId: 'biomedical', 
               classifier: '', file: 'target/bioMedical-0.0.2-SNAPSHOT.jar', 
                type: 'jar']], credentialsId: 'NexusID', groupId: 'QA', 
                nexusUrl: '198.58.119.40:8081/repository/sharont-repo', nexusVersion: 'nexus3', 
                protocol: 'http', repository: 'sharont-repo', version: '002'
        }
    }
       }

}