node ('website') {
    stage ('Checkout') {
        checkout scm
    }

    stage ('Build') {
        sh "mkdocs build"
    }

    stage ('Deploy') {
        sh "rsync -a site/ /var/www/gpuci/html/"
    }
}
