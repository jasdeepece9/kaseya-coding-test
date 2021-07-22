properties([[$class: 'JiraProjectProperty'], [$class: 'ScannerJobProperty', doNotScan: false], gitLabConnection(''), [$class: 'GitlabLogoProperty', repositoryName: ''], parameters([string(defaultValue: '52.36.124.156', description: 'Enter the VM IP to connect to', name: 'VM_IP', trim: false), string(defaultValue: 'administrator', description: 'Enter the VM Admin User details with which you want to connect to VM', name: 'VM_Admin_User', trim: false), password(defaultValue: 'administrator', description: 'Enter the VM Admin User\'s Password for connecting to VM', name: 'VM_Password')])])

pipeline{
	agent any
	stages{
		stage('GIT Checkout'){
			steps{
				//Below command works for master Branch
				//git 'https://github.com/jasdeepece9/kaseya-coding-test'
				
				//Below command works for main Branch
				git branch: 'main', url: 'https://github.com/jasdeepece9/kaseya-coding-test'
			}
		}
		stage('Execute Ansible Playbook'){
			steps{
				//ansiblePlaybook extras: '--extra-vars ‘{“name”:“${VM IP}” “name”:“${VM Admin User}” “name”:“${VM Password}”}‘', installation: 'ansible', inventory: 'host.inv', playbook: 'windows.yml'
			    ansiblePlaybook installation: 'ansible', inventory: 'host.inv', playbook: 'windows.yml'
			}
		}
	}
}
