pipeline {
        agent any 

        stages {
            stage('pkr inspect') {     
                steps {
                    sh 'packer inspect /image.json'
                }
            }
            stage('pkr validate') {      
                steps {
                    sh 'packer validate /image.json'
                }
            }                
            stage('pkr build') {      
                steps {
                    sh 'packer build /image.json'
                }
            }               
				
        }
    }
