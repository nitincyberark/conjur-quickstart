// node{
//   stage('test'){
//      echo "Hello nitin"
//   }
// //   stage('git checkout'){
// //       git credentialsId: 'b82ea1ef-8b14-4d89-a45e-b30c04d4f996', url: 'https://github.com/nitincyberark/conjur-credential-plugin.git'
// //   }
// }

pipeline{
     agent any
  stages{
    stage("testing conjur cred from jenkisfile"){
      steps{
           echo "conjur secret db_password configured with host1 id"
         withCredentials([conjurSecretCredential(credentialsId: 'passwor_configured_with_host1_from_jenkinsfile', variable: 'CONJUR_SECRET')]) {
               sh "echo $CONJUR_SECRET | base64"
          }
      }
    }
  }

}
