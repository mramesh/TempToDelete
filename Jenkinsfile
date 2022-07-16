pipeline {
    // agent {
    //     docker {
    //         image 'mcr.microsoft.com/playwright:v1.23.0-focal'
    //     }
    // }

    stages {
        stage('installing playwright') {
            steps {
                bat '''
                    npm i -D @playwright@test
                    npx playwright install
                '''
            }
        }
        stage('help') {
            steps {
                bat 'npx playwight test --help'
            }
        }
        stage('test') {
            steps{
                bat '''
                    npx playwright test --list
                    npx playwright test
                '''
            }
        }
    }
}