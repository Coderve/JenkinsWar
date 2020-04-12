pipeline{
   agent any
   /*def tomcatWeb = 'D:\\Auto_deployment\\apache-tomcat-9.0.30\\apache-tomcat-9.0.30\\webapps'
   def tomcatBin = 'D:\\Auto_deployment\\apache-tomcat-9.0.30\\apache-tomcat-9.0.30\\bin'
   def tomcatStatus = ''*/
   stages{
   stage('SCM Checkout'){
      steps {
     git 'https://github.com/Coderve/JenkinsWar.git'
   }
   }
   stage('Compile-Package-create-war-file'){
      // Get maven home path
      steps{
      def mvnHome =  tool name: 'Maven_Path', type: 'maven'
      bat "${mvnHome}/bin/mvn package"
      }
   }
/*   stage ('Stop Tomcat Server') {
               bat ''' @ECHO OFF
               wmic process list brief | find /i "tomcat" > NUL
               IF ERRORLEVEL 1 (
                    echo  Stopped
               ) ELSE (
               echo running
                  "${tomcatBin}\\shutdown.bat"
                  sleep(time:10,unit:"SECONDS") 
               )
'''
   }*/
   /*stage('Deploy to Tomcat'){
     bat "copy target\\JenkinsWar.war \"${tomcatWeb}\\JenkinsWar.war\""
   }*/
}
}
