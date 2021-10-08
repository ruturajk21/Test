pipeline {
    agent any
    stages {
        stage('one') {
            steps {
                echo 'Hi I am ruturaj from Pune'
            }
        } 
        stage('two'){
                steps{
                   input('Do you want to continue?')
                }  
            }
            stage('three'){
                when{
                    not{
                          branch "master"
                    }
                }
                steps{
                   echo 'Hello'
                }
            }
            stage ('Four'){
                parallel{
                    stage('Unit Testing'){
                        steps{
                            echo 'Running the unit test cases'
                        }
                    }
                    stage('Integration testing'){
                        steps{
                            echo 'Running integration test cases'
                        }
                    
                    }
                }
            }
        }
   }
