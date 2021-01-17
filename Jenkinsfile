podTemplate {
    node(POD_LABEL) {
        stage('Run shell') {
            sh '''
              curl -u maksiess:6623ee389d5859c7bab0391ec118cc17546e7710  https://api.github.com/user/repos -d '{"name":"oneclick"}'
              '''
        }
    }
}

podTemplate {
    node(POD_LABEL) {
      stage("Test"){
        checkout scm
        sh 'bash script.sh'
      }
    }
}
