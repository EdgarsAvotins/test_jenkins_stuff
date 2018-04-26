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
  checkout scm
  echo 'hi'
  echo 'beginning'
  sh 'pwd'
  sh 'adb logcat'
}
