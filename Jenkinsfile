pipeline{
     agent any
     stages{
         stage('checkout'){
            steps{
                git branch:'main',
                url:https://github.com/Ravichandra885/c11
            }
         }
         stage('Build')
         {
            steps{
                bat :'mvn clean package'
            }
         }
     
}
post{
     sucess{
        archiveArtifacts 'target/*.jar'
        echo 'build s'
     }
}
}