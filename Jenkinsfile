pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
		sh 'java -jar target/my-app-1.0-SNAPSHOT.jar'
            }
        }
	stage('xxxx') {
		sh 'ok.....'
	}
    }

    post {
        always {
            sh '''
                echo 'finish!!!!!!!!!'
            '''
            deleteDir()
        }
    }
}
