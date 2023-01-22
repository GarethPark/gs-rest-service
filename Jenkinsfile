pipeline {
    agent any
        tools {
            jdk 'openjdk-171'
            maven 'maven-387'
          }
        stages {
            stage('Log JAVA_HOME') {
              steps {
                sh 'echo $JAVA_HOME'
                sh 'echo maven -version'
                sh 'echo java -version'
              }
            }
            stage('Check Maven Installation') {
                steps {
                    sh 'apt-get update && apt-get install maven -y'
                    sh 'mvn -version'
                }
            }
            /*stage('Checkout') {
                steps {
                    git branch: 'main', url:'https://github.com/GarethPark/gptheme'
                }
            }
            stage('Build') {
                steps {
                    sh './mvnw clean package'
                }
            }
            stage('Build Docker Image') {
                steps {
                    sh 'docker build -t your_username/your_spring_boot_app .'
                }
            }
            stage('Push to Docker Hub') {
                steps {
                    withDockerRegistry([credentialsId: 'dockerhub', url: 'https://index.docker.io/v1/']) {
                        sh 'docker push your_username/your_spring_boot_app'
                    }
                }
            }*/
        }





	/*agent none

	triggers {
		pollSCM 'H/10 * * * *'
	}

	options {
		disableConcurrentBuilds()
		buildDiscarder(logRotator(numToKeepStr: '14'))
	}

	stages {
		stage("test: baseline (jdk17)") {
			agent {
				docker {
					image 'harbor-repo.vmware.com/dockerhub-proxy-cache/library/adoptopenjdk/openjdk17:latest'
					args '-v $HOME/.m2:/tmp/jenkins-home/.m2'
				}
			}
			options { timeout(time: 30, unit: 'MINUTES') }
			steps {
				sh 'test/run.sh'
			}
		}

	}*/

	/*post {
		changed {
			script {
				slackSend(
						color: (currentBuild.currentResult == 'SUCCESS') ? 'good' : 'danger',
						channel: '#sagan-content',
						message: "${currentBuild.fullDisplayName} - `${currentBuild.currentResult}`\n${env.BUILD_URL}")
				emailext(
						subject: "[${currentBuild.fullDisplayName}] ${currentBuild.currentResult}",
						mimeType: 'text/html',
						recipientProviders: [[$class: 'CulpritsRecipientProvider'], [$class: 'RequesterRecipientProvider']],
						body: "<a href=\"${env.BUILD_URL}\">${currentBuild.fullDisplayName} is reported as ${currentBuild.currentResult}</a>")
			}
		}
	}*/
}
