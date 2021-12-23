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
        nexusArtifactUploader credentialsId: 'jenkins', groupId: 'com.maven.demo', 
            nexusUrl: 'localhost:8110', nexusVersion: 'nexus3', protocol: 'http', 
            repository: 'http://localhost:8110/repository/deployment/', version: '1.0.0'
    
}
