pipeline {
           agent any
           stages {
                stage("git-clone") {
                     steps {
                          git branch: 'master', credentialsId: 'test', url: 'https://github.com/Coderve/JenkinsWar.git' 
                     }
                }
   		stage("Build")
		{
		steps {
                          
				bat 'mvn clean install -Dmaven.test.skip=true'
		}
              }
           }
      }
