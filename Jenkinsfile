pipeline {
        agent any 

        stages {
            stage('pkr inspect') {     
                steps {
                    sh 'packer inspect /packer/image.json'
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
