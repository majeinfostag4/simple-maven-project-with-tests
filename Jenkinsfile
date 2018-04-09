node('master'){
  checkout scm
  
  def mvnHome
  
  stage('Build'){
    mvnHome = tool 'M3'
    sh '${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package'
  }
  
  stage('Result'){
    junit '**/target/surefire-reports/TEST-*.xml'
  }
}
