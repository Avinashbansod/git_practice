pipeline {
    agent any

    stages {
        stage('ansible check targets') {
            steps {
                echo 'ping ansible targets!'
                sh "export ANSIBLE_HOST_KEY_CHECKING=False"
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh-key-for-git', keyFileVariable: 'ANSIBLE_SSH_KEY', usernameVariable: 'ansible')]) {
                    sh "ansible all -i 'ubuntu1,' -m ping --user ansible --private-key ${ANSIBLE_SSH_KEY}"
                }
            }
        }
    }
}
