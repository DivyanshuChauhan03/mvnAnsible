pipeline{
	agent any
	tools{
		maven 'maven'
		}
	stages{
		stage('checkout'){
		step{
		git branch:'main',url:'https://github.com/DivyanshuChauhan03/mvnAnsible'
		}
		}
		stage('build and test'){
		step{
		sh 'mvm clean install'
		}
		}
		stage('deploy'){
		step{
		sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
		}
		}
		}
		}
		
