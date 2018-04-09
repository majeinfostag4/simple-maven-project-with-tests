node('master'){
  checkout scm
  
  def mvnHome
  mvnHome = tool 'M3'
  
  stage('Build'){
    sh '${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package'
  }
  
  stage('Result'){
    junit '**/target/surefire-reports/TEST-*.xml'
  }
}
