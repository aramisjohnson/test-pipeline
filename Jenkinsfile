

try {
        stage('Test Kubernete Install') {
            sh "./kubectl get pods"
        }
    }
}
catch (Exception e) {
    echo 'Failure encountered'

    node("ec2-stateful") {
        echo 'Cleaning up workspace'
        deleteDir()
    }

    exit 1
}