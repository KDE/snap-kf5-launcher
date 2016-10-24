cleanNode('master') {
  stage 'rake'
  git 'https://github.com/apachelogger/kf5-snap-env'
  sh 'rake'
  archiveArtifacts 'kde-frameworks-5-env_all.tar.xz'
}

def cleanNode(label, body) {
  node(label) {
    deleteDir()
    try {
      body()
    } finally {
      step([$class: 'WsCleanup', cleanWhenFailure: true])
    }
  }
}
