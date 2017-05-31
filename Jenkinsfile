node ('website') {
    stage ('Checkout') {
        checkout scm
    }

    stage ('Build') {
        sh "mkdocs build"
    }

    stage ('Deploy') {
        sh "mkdocs gh-deploy"
    }
}
