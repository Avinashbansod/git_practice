node {
    SERVER_CREDENTIALS = credentials('ansible-private-key')
    stage('checking ansible ping') { // for display purposes
        sh "ansible all -i 'ubuntu1,' -m ping --user ansible --private-key ${SERVER_CREDENTIALS}"
    }
    
}
