pipeline {
  agent { label ""}
  stages {
    stage('Build and Deploy to Dev') {
      steps {
        script{
          openshiftBuild bldCfg: 'flask-oc', buildName: '', checkForTriggeredDeployments: 'true', commitID: '', namespace: 'ysinjab-dev', showBuildLogs: 'true', verbose: 'false'
//                   openshift.withCluster() { openshift.withProject(DEV_PROJECT) { }}

//          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
        }
      }
    }    
  }
}
