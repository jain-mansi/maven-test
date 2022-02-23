node{
  stage("git checkout"){
    checkout scm
    sh"ls -ltr"
  }
  stage("build"){
    sh'''
    mvn clean package
     
    '''
}
   stage("sonarqube"){
     withSonarQubeEnv("sonarqube"){
    sh'''
    mvn clean sonar:sonar
     
    '''
   }
     }
}

