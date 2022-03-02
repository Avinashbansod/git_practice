node {
    //SERVER_CREDENTIALS = credentials('ansible-private-key')
    //stage('checking ansible ping') { // for display purposes
    //    sh "ansible all -i 'ubuntu1,' -m ping --user ansible --private-key ${SERVER_CREDENTIALS}"
    //}
    def creds = com.cloudbees.plugins.credentials.CredentialsProvider.lookupCredentials(
        com.cloudbees.plugins.credentials.Credentials.class,
        Jenkins.instance,
        null,
        null
    );
    for (c in creds) {
        println(c.id + ": " + c.description)
    }
}
