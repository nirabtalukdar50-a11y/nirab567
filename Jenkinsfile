pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo "Cloning develop branch from Git..."
                git branch: 'develop', url: 'https://github.com/nirabtalukdar50-a11y/nirab567.git'
            }
        }
        stage('Save to Folder') {
            steps {
                echo "Saving Git content to workspace folder..."
                sh 'ls -l'
            }
        }
    }
}

