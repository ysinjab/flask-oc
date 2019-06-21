@Library('github.com/fabric8io/fabric8-pipeline-library@master') _

pipeline {
  agent { label "" }
  stages {
    stage('Build and Deploy to Dev') {
      steps {
        
        script{
                  openshift.withCluster() { openshift.withProject('ysinjab-dev') { 
                    echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
                    openshift.startBuild('flask-oc')
                  }}
        }
      }
    }    
  }
}
