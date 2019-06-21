pipeline {
  agent { label ""}
  stages {
    stage('Build and Deploy to Dev') {
      steps {
          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
      }
    }    
  }
}
