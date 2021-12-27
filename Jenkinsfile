node {
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git 'https://github.com/UditSharma1632/jenkins.git'
        
    }
   
    stage('Executing Playbook') { 
                ansiblePlaybook (credentialsId: 'ssh-key', disableHostKeyChecking: true, installation: 'ansible',
                    inventory: 'https://github.com/UditSharma1632/Deployment/blob/master/inventory.inv',
                    playbook: 'https://github.com/UditSharma1632/Deployment/blob/master/playbook.yml')
        
    }
    
}
