pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              /* bat "rmdir  /s /q TicketBookingServiceJunitTesting" */
               bat "git clone https://github.com/skillpractical/TicketBookingServiceJunitTesting.git JavaApp12"
               sh label: '', script: 'bat "mvn clean -f TicketBookingServiceJunitTesting"'
            }
        }
        stage('install') {
            steps {
                 sh label: '', script: 'bat "mvn install -f TicketBookingServiceJunitTesting"'
               }
        }
        stage('test') {
            steps {
                sh label: '', script: 'bat "mvn test -f TicketBookingServiceJunitTesting"'
              }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
