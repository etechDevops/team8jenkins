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
				echo "welcome to Etech Team8 Jenkins"
			}
		}
		stage('6-securitycheck'){
			steps{
				sh 'bash -x /var/lib/jenkins/workspace/jenkins-demo2/jenkinstest.sh'
			}
		}
	}
}