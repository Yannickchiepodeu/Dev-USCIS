pipeline {
   agent any
       stages {  
     stage('one') {
                   puts 'Hi ,this is yannick from virginia'
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
                       puts "Hello"
                  }      
               }     
   stage('four')  {
      parallel {
         stage('unite test') {
            steps {
               puts "running unit test...."
            }
         }
         stage('integration test') {
            agent {
               docker { 
                  reuseNode false
                  image 'ubuntu'
               }
            }
         steps {
            puts 'running the ingration test..'
         }
      }
   }
}
}
