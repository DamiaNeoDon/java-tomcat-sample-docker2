pipeline {
    agent any
    tools {
        maven 'LokalnyMaven'
        jdk 'LokalnnyJDK'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage('Build Application123') {
            steps {
                sh 'mvn -f /pom.xml clean package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        stage('Build Application') {
            steps {
                sh 'mvn -f /pom.xml clean package'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }

=======

        }
        stage('Create tomcat docker image'){
          steps{
              sh 'pwd'
              sh 'ls -a'
              sh "docker build . -t tomcatsamplewebapp:${env.BUILD_ID}"
              }
        }
>>>>>>> 15f7655287b9ded67c44009d4e8609ddf1f14372
    }
}
