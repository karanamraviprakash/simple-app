pipeline {
    agent any
    environment{
        PATH="/opt/maven/apache-maven-3.8.2/bin:$PATH"
    }
    options {
        buildDiscarder logRotator(daysToKeepStr: '5', numToKeepStr: '7')
    }
    stages{
        stage('Build'){
            steps{
                 sh script: 'mvn clean package'
                 archiveArtifacts artifacts: 'target/*.war', onlyIfSuccessful: true
            }
        }
       // stage('Upload War To Nexus'){
         //   steps{
           //     script{

             //       def mavenPom = readMavenPom file: 'pom.xml'
               //     def nexusRepoName = mavenPom.version.endsWith("SNAPSHOT") ? "simpleapp-snapshot" : "simpleapp-release"
                 //   nexusArtifactUploader artifacts: [
                        //[
                   //         artifactId: 'simple-app', 
                     //       classifier: '', 
                       //     file: "target/simple-app-${mavenPom.version}.war", 
                         //   type: 'war'
                   //     ]
                   // ], 
       //             credentialsId: 'null', 
         //           groupId: 'in.javahome', 
           //         nexusUrl: '3.109.174.42:8081', 
             //       nexusVersion: '1.0.0', 
               //     protocol: 'http', 
                 //   repository: nexusRepoName, 
                   // version: "${mavenPom.version}"
                   // }
            }
        }
    }
}
