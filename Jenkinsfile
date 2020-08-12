pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              /* bat "rmdir  /s /q TicketBookingServiceJunitTesting" */
               bat "git clone https://github.com/skillpractical/TicketBookingServiceJunitTesting.git JavaApp14"
               sh 'mvn clean package'
            }
        }
     }
}
