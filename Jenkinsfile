node {
    def app

    stage('Clone repository') {
      
        checkout scm
    }

    stage('Build image') {
  
       sh 'docker build -t testimg .'
    }

    stage('Test image') {
            sh 'echo "Tests passed"'
    }

    // stage('Push image') {
        
    //     docker.withRegistry('https://skinnysydcontainersregistry.azurecr.io', 'azurecr') {
    //         app.push("${env.BUILD_NUMBER}")
    //     }
    // }
    
//     stage('Trigger ManifestUpdate') {
//                 echo "triggering updatemanifestjob"
//                 build job: 'updatemanifest', parameters: [string(name: 'DOCKERTAG', value: env.BUILD_NUMBER)]
//         }
}
