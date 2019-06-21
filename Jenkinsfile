@Library('github.com/fabric8io/fabric8-pipeline-library@master') _

// pipeline {
//   agent { label "" }
//   stages {
//     stage('Build and Deploy to Dev') {
//       steps {
        
//         script{
//           // openshiftBuild bldCfg: 'flask-oc', buildName: '', checkForTriggeredDeployments: 'true', commitID: '', namespace: 'ysinjab-dev', showBuildLogs: 'true', verbose: 'false'
//                   openshift.withCluster() { openshift.withProject('ysinjab-dev') { 
//                     echo "Hello from project ${openshift.project()} in cluster ${openshift.cluster()}"
//                     openshift.startBuild('flask-oc')
//                   }}
        

// //          openshiftBuild(namespace:'ysinjab-dev', buildConfig: 'flask-oc',showBuildLogs:'true', waitTime: '3000000') 
//         }
//       }
//     }    
//   }
// }
mavenNode(dockerImage: 'docker:1.11.2') {
    container(name: 'docker') {
        sh 'docker build -t myorg/myimage .'
    }
}
