node ('website') {
    stage ('Checkout') {
        checkout scm
    }

    stage ('Build') {
        sh "ls -l"
        sh "find ."
    }

    stage ('Deploy') {
        sh "echo deploy"
    }
} 
