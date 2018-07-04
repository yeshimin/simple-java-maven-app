pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
                sh 'cp target/my-app-1.0-SNAPSHOT.jar /home/ysm/YsmSpace/test.d/jenkins'
                sh 'cd /home/ysm/YsmSpace/test.d/jenkins && pwd && /home/ysm/YsmSpace/test.d/jenkins'
                sh 'pwd'
                sh 'java -jar my-app-1.0-SNAPSHOT.jar'
            }
        }
    }

    post {
        always {
            sh '''
                echo 'finish!!!!!!!!!'
            '''
        }
    }
}
