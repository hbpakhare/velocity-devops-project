pipeline {

	agent {
					label {
						
							label "dev"
							customWorkspace "/mnt/project"
						
					}
	}
	
	environment {
						
						composeurl = "https://github.com/hbpakhare/velocity-devops-project.git"
						composedirname = "velocity-devops-project"
		}
	
	stages {
		
			stage ("CLONE-DOCKERC-FILE"){
			
				steps {     
				            sh "rm -rf *"
							sh "git clone ${composeurl}"
				}
			
			}
			
			stage ("RUN_COMPOSE"){
			
				steps {
				
							sh "cd ${composedirname} && sudo docker-compose up -d"
				}
			
			}
	
	}
}
