pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                bat 'mvn clean package'
            }       
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat9(alternativeDeploymentContext: '', 
                credentialsId: 'f70cd1b9-a6e8-4239-9209-c1a375d642e8', path: '', 
                url: 'http://localhost:8081/')], contextPath: 'javawebapppipeline', war: '**/java-web-project.war'
            }       
        }
    }
}
