pipeline
{
    agent any 
     
    stages{
        
stage('simple Java Program') {
    steps {
         sh '''#!/bin/bash
                sudo yum install java-1.8.0-openjdk-devel  -y
                sudo java -version 
                sudo git clone https://github.com/mjmanas0699/java_code.git /var/lib/jenkins/workspace/job1
                sudo cp -rvf *.java  /
                sudo javac /*.java
                code=$(basename  /*.class  .class) #basename , it help to remove the suffix from file
                cd / && java $code 
         '''
    }
}
            
        }
    }  
