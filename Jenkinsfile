pipeline {
   agent any
       stages {  
     stage('one') {
                   println 'Hi ,this is yannick from virginia'
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
                       println "Hello"
                  }      
               }     
   stage('four')  {
      parallel {
         stage('unite test') {
            steps {
               println "running unit test...."
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
            println 'running the ingration test..'
         }
      }
   }
}
}
