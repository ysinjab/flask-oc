pipeline {
  agent { label ""}
  stages {
    stage('Build and Deploy to Dev') {
      steps {
        script{
          // openshiftBuild bldCfg: 'flask-oc', buildName: '', checkForTriggeredDeployments: 'true', commitID: '', namespace: 'ysinjab-dev', showBuildLogs: 'true', verbose: 'false'
                  openshift.withCluster() { openshift.withProject('ysinjab-dev') { 
                    echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                  }}

//          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
        }
      }
    }    
  }
}
