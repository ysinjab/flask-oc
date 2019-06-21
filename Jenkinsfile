pipeline {
  agent { label ""}
  stages {
    stage('Build and Deploy to Dev') {
      steps {
        script{
          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
        }
      }
    }    
  }
}
