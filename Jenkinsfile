pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 5 ,unit:'SECONDS')
        disableConcurrentBuilds()
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