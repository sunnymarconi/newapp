node{
   stage('SCM Checkout'){
     git 'https://github.com/sureshatchi/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3.5.4', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Suresh''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'tosureshatchi@gmail.com'
   }
   
}
