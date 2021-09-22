pipeline{
    agent any
    environment{
        PATH="/opt/maven/apache-maven-3.8.2/bin:$PATH"
    }
    stages{
        
        stage('build'){
            steps{
                sh "mvn clean install package"
            }
    
        }
                
                
            }  
}
