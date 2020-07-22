pipeline
{
    agent any 
     
    stages{
        
        stage('Compile stage') {
            
            steps{
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
             }
            
        }
    }  
    stage ("Testing Stage")
    {
          steps{
              withMaven(maven : 'maven_3_5_0') {
                  sh 'mvn test'
             }
    }
} 
    stage ("Deploy  Stage")
    {
          steps{
              withMaven(maven : 'maven_3_5_0') {
                  sh 'mvn deploy'
             }
    }
}
} 
}
