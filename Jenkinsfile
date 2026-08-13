node {
   stage('Clone') {
        git branch: 'Feature/2026.08.01',
            url: 'git@github.com:shilpapatanaik/onlinebookstore.git'
    }

    stage('Build') {
        bat 'mvn clean install'
    }

    stage('Check WAR') {
        bat 'dir target\\*.war'
    }

    stage('Archive Artifacts') {
        archiveArtifacts artifacts: 'target/*.war',
                         followSymlinks: false
    }

    stage('Deploy') {
        echo 'Deploy the project'
    }
}