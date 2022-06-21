pipeline {
    agent any
    
    tools {
        maven "Maven3"
    }

    stages {
        stage('Git Clone/Git Checkout') {
            steps {
                echo 'Hello World'
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/naveenvgit/hello-world.git']]])
            }
        }
        
        stage('Maven Build') {
            steps {
               sh 'mvn clean package'
            }
        }
    }
}

