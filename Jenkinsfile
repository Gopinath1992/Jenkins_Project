pipeline {
    agent any  // Runs on any available agent
     tools {
        maven 'maven_3.9.9'  // Use the Maven version configured in Jenkins
    }


    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'GitHub', url: 'https://github.com/Gopinath1992/Jenkins_Project.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                sh 'mvn clean package'  // Example: Maven build command
            }
        }

    //     stage('Test') {
    //         steps {
    //             echo "Running tests..."
    //             sh 'mvn test'  // Running unit tests
    //         }
    //     }

    //     stage('Deploy') {
    //         steps {
    //             echo "Deploying the application..."
    //             sh './deploy.sh'  // Example deployment script
    //         }
    //     }
    // }

    // post {
    //     success {
    //         echo "✅ Build Successful!"
    //     }
    //     failure {
    //         echo "❌ Build Failed!"
    //     }
    // }
}
