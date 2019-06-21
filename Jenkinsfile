@Library('github.com/fabric8io/fabric8-pipeline-library@master') _

pipeline {
  agent { label ""}
  stages {
    stage('Build and Deploy to Dev') {
      steps {
        approve {
      version = '0.0.1'
      console = 'http://fabric8.kubernetes.fabric8.io'
      environment = 'staging'
    }
        script{
          // openshiftBuild bldCfg: 'flask-oc', buildName: '', checkForTriggeredDeployments: 'true', commitID: '', namespace: 'ysinjab-dev', showBuildLogs: 'true', verbose: 'false'
                  openshift.withCluster() { openshift.withProject('ysinjab-dev') { 
                    echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                    openshift.startBuild('flask-oc')
                  }}
        

//          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
        }
      }
    }    
  }
}
