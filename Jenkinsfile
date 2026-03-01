pipeline {
    agent any
    tools {
       maven "maven"
    }
    stages{
        stage('clone'){
            steps{
                echo "cloning code"
                git branch: 'test', url: 'https://github.com/mantu0tech/simple-java-app.git'
            }
        }
        stage('build'){
            steps{
                echo "cloning code"
                sh "mvn clean install"
            }
        }
        stage('artifact'){
            steps{
                echo "packing code"
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
    }
    
}
