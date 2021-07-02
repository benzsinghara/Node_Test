import groovy.json.JsonSlurperClassic
import com.michelin.cio.hudson.plugins.rolestrategy.RoleBasedAuthorizationStrategy

def checkoutCodePipeLine(){
    // CheckOut pipeline code 
    pipeline_url= "https://github.com/benzsinghara/Node_Test.git"
    stage('ClonePipeLine') {
      // CHECKOUT CODE REPO
      checkout changelog: false, poll: false, scm: [
        $class: 'GitSCM',
        branches: [[name: '*/main']],
        doGenerateSubmoduleConfigurations: false,
        extensions: [
          [$class: 'CleanCheckout'],
          [$class: 'CloneOption', depth: 0, noTags: true, reference: '', shallow: true],
          [$class: 'SubmoduleOption', disableSubmodules: true, parentCredentials: false, recursiveSubmodules: false, reference: '', trackingSubmodules: false],
          [$class: 'RelativeTargetDirectory', relativeTargetDir: 'tmpdir']],
        submoduleCfg: [],
        userRemoteConfigs: [[credentialsId: 'gitlab-user-jenkinsci', url: pipeline_url]]
      ]
    }
  // LogRotator build 10
  properties([[$class: 'BuildDiscarderProperty', strategy: [$class: 'LogRotator', artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10']]]);
}