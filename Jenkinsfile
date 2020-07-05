pipeline{
    agent any
    tools {
  maven 'Maven3.6.3'
}
    stages{
    stage('Build'){
        steps{
        sh script: 'mvn clean package'
        }
    }
 stage('Upload to Nexus'){
 steps{
nexusArtifactUploader artifacts: [[artifactId: 'webapps', classifier: '', file: 'target/*.war', type: 'war']], credentialsId: '0d504266-cba7-408b-8e06-4b20fd606354', groupId: 'we.com', nexusUrl: '13.233.196.120', nexusVersion: 'nexus3', protocol: 'http', repository: 'harish-release/', version: '4.0-SNAPSHOT'
}
}
} 
} 
}
