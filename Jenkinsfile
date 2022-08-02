pipeline{
    agent any
    stages{
                stage('maven package '){
            steps{
                sh 'mvn clean package'
                                } 
                                
               }
               stage(' tomcat dev'){
            steps{
                sshagent(['tomcat']) {
    // copy war file to tomcat 
                    sh "scp -o StrictHostKeyChecking=no target/calculator*.war  ec2-user@54.213.99.225:/opt/tomcat/webapps/"
                     sh "ssh ec2-user@54.213.99.225 service tomcat stop"
                     sh "ssh ec2-user@54.213.99.225 service tomcat start"
                }
                                
                                } 
                                
               } 
    }
}
