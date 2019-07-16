Pipeline{
    agent any 
          stages {
              stages('one'){
                  steps {
                        echo "Hi! My name is Ashif!!"
                   }
              }
              stages('Two'){
                  steps {
                        input("Do you want proceeed?!")
                   }
              }
              
              stages('Three'){
                  when {
                        not {
                          branch "master"
                        }
                       }
                  steps {
                        echo "Hello"
                   }
              }
              
          }
}
