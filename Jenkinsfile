properties([
    buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '25')),
    [$class: 'BuildBlockerProperty',
     blockLevel: 'GLOBAL',
     blockingJobs: 'TemporaryTestMultibranch.*',
     scanQueueFor: 'NONE',
     useBuildBlocker: true],
    disableConcurrentBuilds()
])
timestamps {
  stage 'Everything'
  node('authy_node2') {
    checkout scm
    echo 'hi'
    echo 'beginning'
    sh 'pwd'
    sh 'sh endless_script.sh'
  }
}
