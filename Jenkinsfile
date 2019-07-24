node{
  stage('SCM Checkout'){
    git 'https://github.com/selvadevops/my-app'
  }
  stage('Compile-package'){
    def mvnHome = tool name: 'maventamil', type: 'maven'   
    sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''Hi,
    Welcome to Jenkins email alerts
    Thanks
    Tamil''', cc: 'selvamware@gmail.com', from: '', replyTo: '', subject: 'Jenkins job alerts - tamil', to: 'selvadevops@gmail.com'
   } 
}
