pipeline {
  agent none;
	parameters {
  booleanParam defaultValue: true, description: 'is this build true', name: 'Debug_Build'
}
  stages {
    stage ('BUILD STAGE1 1') {
	    agent any;
      steps {
	      echo "This Build is ${params.Debug_Build}"
        sh 'sleep 5;'
      }  
    }  
      	   stage ('BUILD STAGE 2') {
		   agentany;
      steps {
        echo "$Job_Name"
        sh 'sleep 5;'
      }  
    }  
	   
    stage ('BUILD STAGE 3') {
	    agent {
			   label 'C_Test'
		   }
      steps {
	      echo "Disk size is"
	      
        sh '''
	df -h
	      'sleep 5;'
	      '''
      }  
    } 
	  stage ('BUILD STAGE 4') {
	  agent any;
	  steps {
		  echo "Process running on background"
		  sh '''
		  ps -ef
		  '''
	  }
  }
  }		  
  } 
	  
