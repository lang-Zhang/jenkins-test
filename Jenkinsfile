pipeline {
  // agent {
  //   docker { image 'node:latest' } // 使用官方 Node.js Docker 镜像
  // }
    // tools {
    //     nodejs 'nodejs-test'
    // }
    stages {
        stage('创建工作目录') {
          agent none
          steps {
            sh 'mkdir base-frontend'
          }
        }
        stage('拉取代码') {
          parallel {
            stage('拉取base-frontend') {
              agent none
              steps {
                container('nodejs') {
                  sh 'docker version'
                  sh 'ls -an'
                  // dir('base-frontend') {
                  //   git(url: 'https://codeup.aliyun.com/6554702f31a848a7a756bd80/ids-base-frontend.git', credentialsId: 'git', branch: 'kbs', changelog: true, poll: false)
                  // }
                }
              }
            }
          }
        }

    }
}
