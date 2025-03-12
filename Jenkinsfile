pipeline {
    agent any
    tools {
        nodejs 'nodejs-test'
    }
    stages {
        stage('测试nodejs') {
            steps {
                echo '测试nodejs...'
                // 这里可以是具体的构建命令，如sh 'mvn clean package'
                sh 'node -v'
            }
        }
        stage('测试pnpm') {
            steps {
                echo '测试pnpm...'
                // 这里可以是具体的构建命令，如sh 'mvn clean package'
                sh 'corepack enable && corepack prepare pnpm@latest --activate && pnpm -v'
            }
        }
    }
}
