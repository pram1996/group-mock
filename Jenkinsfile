pipeline {

    agent {

          label 'slave'

    }
    
	stages {
	
	    stage ('install-apache'){
	 
              steps {
                 
                 sh 'sudo yum install-httpd -y'                    
					
                }					
	            
	      }
		  
		stage ('start -apache') {
           
               steps {

                  sh 'sudo service httpd start'  
                }			   
            }		   
	    stage ('deploy-index.html') {
		
		      steps {
			  
			      sh 'sudo echo " good morning " >> /var/www/html/index.html '
				  sh 'sudo chmod 777 -R /var/www/html/index.html'
			}
		}
	}
}	
