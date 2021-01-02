pipeline {
        agent any 
        environment {
            AWS_ACCESS_KEY_ID = credentials('aws-access-secret-id')
            AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
            }
	
        stages {
            stage('pkr inspect') {     
                steps {
		    sh 'echo $AWS_ACCESS_KEY_ID'
                    sh 'packer inspect packer/image.json'
                }
            }
            stage('pkr validate') {      
                steps {
                    sh 'packer validate packer/image.json'
                }
            }                
            stage('pkr build') {      
                steps {
                    sh 'packer build packer/image.json'
                }		    
            }               
				
        }
    }
