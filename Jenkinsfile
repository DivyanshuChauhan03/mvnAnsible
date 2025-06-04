pipeline{
	agent any
	tools{
		maven 'maven'
		}
	stages{
		stage('checkout'){
		steps{
		git branch:'main',url:'https://github.com/DivyanshuChauhan03/mvnAnsible'
		}
		}
		stage('build and test'){
		steps{
		sh 'mvm clean install'
		}
		}
		stage('deploy'){
		steps{
		sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
		}
		}
		}
		}
		
