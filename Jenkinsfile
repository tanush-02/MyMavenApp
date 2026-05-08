ipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/tanush-02/MyMavenPipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh 'chmod +x gradlew'
                sh './gradlew build'
            }
        }
    }

    post {
        success {
            echo 'Build Successful'
        }

        failure {
            echo 'Build Failed'
        }
    }
}

