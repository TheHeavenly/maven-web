pipeline{
  agent any 
  tools {
    maven "maven3.8.5"
  }  
  stages {
    stage('1GetCode'){
      steps{
        sh "echo 'cloning the latest application version' "
        git branch: 'feature', credentialsId: 'gitHubCredentials', url: 'https://github.com/aramide80/maven-web-application'
      }
    }
    stage('3Test+Build'){
      steps{
        sh "echo 'running JUnit-test-cases' "
        sh "echo 'testing must passed to create artifacts ' "
        sh "mvn clean package"
      }
    }
    /*
    stage('4CodeQuality'){
      steps{
        sh "echo 'Perfoming CodeQualityAnalysis' "
        sh "mvn sonar:sonar"
      }
    }
    stage('5uploadNexus'){            
      steps{
        sh "mvn deploy"
      }
    } 
    stage('8deploy2prod'){
      steps{
        deploy adapters: [tomcat8(credentialsId: 'tomcat-credentials', path: '', url: 'http://54.157.234.56:8177/')], contextPath: null, war: 'target/*war'
      }
    }
}
  post{
    always{
      emailext body: '''Hey guys
Please check build status.

Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    }
    success{
      emailext body: '''Hey guys
Good job build and deployment is successful.

Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    } 
    failure{
      emailext body: '''Hey guys
Build failed. Please resolve issues.

Thanks
Landmark 
+1 437 215 2483''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'paypal-team@gmail.com'
    }
  } 
  */
}
}
