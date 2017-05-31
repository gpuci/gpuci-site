node ('website') {
    stage ('Checkout') {
        checkout scm
    }

    stage ('Build') {
        sh "mkdocs build"
    }

    stage ('Deploy') {
        sh "rsync -aqr site/ /var/www/gpuci/html/gpuci --delete"
    }
}
