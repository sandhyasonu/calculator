pipeline{
    agent any
    stages{
        stage('git checkout'){
            steps{
                 git credentialsId: 'gitaadd', 
                url: 'https://github.com/sandhyasonu/calculator.git'
                             }
        }
        stage('maven package '){
            steps{
                sh 'mvn clean package'
                                } 
                                
               }
               stage(' tomcat dev'){
            steps{
                echo "this need to be implemented"
                                } 
                                
               }
    }
}
