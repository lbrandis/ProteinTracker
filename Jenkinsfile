node {
    stage('Build') {
        echo 'Checkout....'
        checkout(
            [$class: 'GitSCM', 
             branches: [[name: '*/master']], 
             doGenerateSubmoduleConfigurations: false, 
             extensions: [], 
             submoduleCfg: [],  
             userRemoteConfigs: [[url: 'https://github.com/lbrandis/ProteinTracker']]
            ])
        
        echo 'Building....'

        sh 'mvn clean install'


    }
    stage('Test') {
        echo 'Testing....'
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}
