pipeline {
    agent any  // Runs on any available agent
    //  tools {
    //     maven 'maven_3.9.9'  // Use the Maven version configured in Jenkins
    // }
    environment {
        // NEXUS_URL = 'http://54.167.172.185:8081'  // Replace with your Nexus URL
        // NEXUS_REPO = 'maven-releases'            // Replace with your Nexus Repository name
        // NEXUS_CREDENTIALS_ID = 'nexus' // Jenkins credentials ID for Nexus
        // ARTIFACT_NAME = 'javaApp.jar'            // Name of the artifact
        MAVEN_HOME = tool 'maven_3.9.9'  // Replace with the name of your Maven installation in Jenkins
        PATH = "${MAVEN_HOME}/bin:${PATH}"
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
                sh 'mvn deploy'  // Example: Maven build command
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
}
