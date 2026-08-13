node {
    stage('Clone') {
        git branch: 'master', url: 'git@github.com:shilpapatanaik/onlinebookstore.git'
    }
     stage('Build') {
        bat 'mvn clean install'
    }
      stage('Test the war') {
                echo ("deploy contextPath: null, war: 'target/*.war''")
                
    }    
      stage('artifacts') {
        archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
                
    }
      
      stage('Deploy'){
           echo 'Deploy the project'
    }

}