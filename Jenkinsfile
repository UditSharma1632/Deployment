node {
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git 'https://github.com/UditSharma1632/jenkins.git'
        
    }
    stage('Build and Package') {
                bat "mvn clean package"
    }
    
    stage('Deploy') {
                bat "mvn deploy"
    }
     
    stage('Nexus') {
        nexusArtifactUploader artifacts: [[artifactId: 'jenkins', classifier: '', file: 'target/jenkins-1.0.0.jar', type: 'jar']], 
            credentialsId: 'jenkins', groupId: 'com.maven.demo', nexusUrl: 'localhost:8110', nexusVersion: 'nexus3', 
            protocol: 'http', repository: 'nexus-repo', version: '1.0.0'
    }
    
}
