pipeline {
    agent {"linux"}
    
    tools {nodejs 'node'}
    
    stages {
        stage('Checking Version') {
            steps {
                bat "npm version"
                bat "npm install"
                dir('client') {
                    bat "dir"
                    bat 'npm install'
                    bat 'npm run build'
                    bat 'npm i -g serve'
                    bat 'serve -s build'
                }
            }
        }
    }
}
