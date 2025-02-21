pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 5 ,unit:'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Hey World'
            }
        }
        stage('Test1'){
            steps{
                echo 'This is test'
                sh 'sleep 8'
            }
        }
    }

post{
    always{
        echo "This section runs always"
        deleteDir()
}
    success{
        echo 'This runs upon success'
}
    failure{
        echo 'This runs upon failure'
}
}
}