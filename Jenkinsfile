pipeline{
	agent any 
	stages{
		stage('1-action1'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins-access', url: 'https://github.com/etechDevops/team8jenkins.git']])
			}
		}
		stage('2-action2'){
			steps{
				sh 'df -h'
			}
		}
		stage('3-action3'){
			steps{
				sh 'lsblk'
			}
		}
		stage('4-action4'){
			steps{
				sh 'lscpu'
			}
		}
		stage('5-welcome_message'){
			steps{
				echo "welcome to Jenkins pipeline security"
			}
		}
		stage('6-securitycheck'){
			steps{
				sh 'bash -x /var/lib/jenkins/workspace/jenkins-demo2/jenkinstest.sh'
			}
		}
		stage('7-parallel-job'){
			parallel{
				stage('1-firstparajob'){
					steps{
						sh 'cat /etc/passwd'
					}
				}
				stage('2-secondparajob'){
					steps{
						sh 'cat /etc/os-release'
					}
				}
			}
		}
		stage('8-endofjobs'){
			steps{
				echo "End of pipeline"
			}
		}
	}
}