pipeline {
  node('master'){
  stages {
    stage('Source') { 
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '9d351bb7-529f-4c21-99c3-efd5d84a9307', url: 'https://github.com/pratiandevops/Spring-boot_App']]])
      }
    }
    stage('Compile') { 
      tools {
        jdk 'jdk'
        maven 'MAVEN_HOME'
      }
      steps {
        powershell 'java -version'
        powershell 'mvn -version'
      }
    }
  }
}
