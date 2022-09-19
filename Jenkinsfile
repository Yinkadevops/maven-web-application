// Powered by Infostretch 

timestamps {

node () {

	stage ('Tesla - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '35564a1d-783a-477c-beea-8bd27555d76b', url: 'https://github.com/Yinkadevops/maven-web-application']]]) 
	}
	stage ('Tesla - Build') {
 	
// Unable to convert a build step referring to "com.cloudbees.jenkins.plugins.sshagent.SSHAgentBuildWrapper". Please verify and convert manually if required.		// Maven build step
	withMaven(maven: 'Maven 3.8.6') { 
 			if(isUnix()) {
 				sh "mvn clean
install " 
			} else { 
 				bat "mvn clean
install " 
			} 
 		}		// Maven build step
	withMaven(maven: 'Maven 3.8.6') { 
 			if(isUnix()) {
 				sh "mvn deploy " 
			} else { 
 				bat "mvn deploy " 
			} 
 		} 
	}
}
}