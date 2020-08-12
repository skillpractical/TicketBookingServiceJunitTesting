pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              /* bat "rmdir  /s /q TicketBookingServiceJunitTesting" */
               git credentialsId: 'git-creds', url: 'https://github.com/skillpractical/TicketBookingServiceJunitTesting.git'
               sh 'mvn clean package'
            }
        }
     }
}
