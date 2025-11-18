node {
    stage('Checkout') {
        git 'https://github.com/akhilnaik04/java-web-app'
    }

    stage('Build') {
        bat 'mvn clean'
        bat 'mvn install'
    }

    stage('Test') {
        bat 'mvn test'
    }

    stage('Archive') {
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
    }
}
