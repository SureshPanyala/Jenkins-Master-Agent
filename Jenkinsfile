pipeline{

agent{

    label 'AGENT-1'

}

options{

    disableConcurrentBuilds()
    timeout ( time: 30, unit : 'MINUTES')
}

stages{

     stage('Build') {
            steps {
                sh "echo this is BUILD"
                sh "echo this is node version"
            }
        }
        stage('Test') {
            steps {
                sh "echo this is TEST"
                sh "sleep 15"
            }
        }
        stage('Deploy') {
            steps {
                sh "echo this is Deploy"
            }
        }



}

post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'I will say Hello when pipeline is success'
        }
        failure { 
            echo 'I will say Hello when pipeline is failure'
        }
    }


}