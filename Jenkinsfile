pipeline {
   agent any
       stages {  
     stage('one') {
                   echo 'Hi ,this is yannick from virginia'
                   
                  }
               }
             stage('two'){
           
            steps {
                input('Do you want to procced?')
               }
                  } 
                 stage('three') {
                 when {
                       not{ 
                              branch "master"
                       }          
               }                         
               steps {  
                       echo "Hello"
                }      
          }     
               
