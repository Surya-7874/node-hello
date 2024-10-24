pipeline {
    agent any
    stages {
        stage("deploypipeline"){
            steps{
                sh 'npm start -h 0.0.0.0 &'
            }
        }
    }
    stage('Approval') {
        steps {
            script {
                  def deploymentDelay = input id: 'deploypipeline', message: 'Deploy to production?', submitter: 'admin', parameters: [choice(choices: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18', '19', '20', '21', '22', '23', '24'], description: 'Hours to delay deployment?', name: 'deploymentDelay')]
                  sleep time: deploymentDelay.toInteger(), unit: 'HOURS'
            }
        }
    } 


}
