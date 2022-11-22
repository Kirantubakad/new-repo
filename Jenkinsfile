pipeline{
    agent any

      stages{
         stage('git clone'){
            steps {
                git credentialsId: 'git_cred', url: 'https://github.com/Kirantubakad/mavenproject.git'
            
            }
        
         }
         stage('build maven'){
           steps{
              sh '''
          
               mvn clean install
            
              '''
             }
       }
    }
}
