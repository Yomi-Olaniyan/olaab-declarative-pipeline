pipeline{
    tools{
        jdk 'olaab-java'
        maven 'olaab-maven'
    }
	agent any
      stages{
           stage('Checkout'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/Yomi-Olaniyan/olaab-declarative-pipeline.git'
              }
          }
          stage('Compile'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
