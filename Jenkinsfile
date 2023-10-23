pipeline {
    agent any
    stages{
        stage('Build'){
        try{
            steps{
                script{
                   echo 'Jenkins build'
                      sh './gradlew assemble'
                }
            }
           }catch(exc){
            echo 'Something failed in build'
            throw
           }
            }
           }
            stage('Test'){
                steps{
                    echo 'Test okay'
                    script{
                        sh './gradlew test'
                    }
                }
        }
    }
