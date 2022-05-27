def getDockerTag() {
 def tag = sh script: 'git rev-parse HEAD', returnStdout: true 
 return tag
}
pipeline{

	agent {
                docker {
                image 'maven'
                
                }
             }
      environment {
          Docker_tag = getDockerTag()
      }
        
        stages{

              stage('mycheckPoint'){
                  steps{
                      script{
			     sh 'echo $Docker_tag'
		  
                 	}
               	 }  
              }	

            }	       	     	         
}
