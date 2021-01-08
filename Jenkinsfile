pipeline {
    agent { 
        docker { 
            image 'maven:3.3.3' 
            // 2. Reusing the node (double-check that this doesn't happen automatically)
            reuseNode true
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean package'
            }
        }
        // 3. Add unit test
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        // 4. Break a test
        // 5. Publish the artifact to language specific repository
        // 6. Create Docker image
    }
}

// Other
// Security scan