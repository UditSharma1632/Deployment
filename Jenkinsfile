node {
    stage('Preparation') { // for display purposes
        // Get some code from a GitHub repository
        git 'https://github.com/UditSharma1632/jenkins.git'
        
    }
   
    stage('Executing Playbook') { 
                ansiblePlaybook (credentialsId: 'id_rsa', disableHostKeyChecking: true, 
                                 installation: 'ansible', inventory: 'inventory.inv', playbook: 'playbook.yml')
        
    }
    
}
