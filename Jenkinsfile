node('testing') {
    stage('Initialize') {
        echo 'Initializing...'
        def node = tool name: 'Node-11.3.0', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
        env.PATH = "${node}/bin:${env.PATH}"
    }

    stage('Checkout') {
        echo 'Getting source code...'
        checkout scm
    }

    stage('Script') {
        echo 'Run node script.js'
        sh 'node script.js'
    }
}