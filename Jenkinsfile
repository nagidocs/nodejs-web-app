// Jenkins multibranch pipeline CI pipeline.
pipeline {
   agent any
   stages {
      stage('init') {
          steps {
	      echo "Build/install dependencies..."
              sh 'npm install'
          }
      }	   
      stage('Test Code') {
          steps {
               	  echo "Test app..."
		  sh 'npm run test'
               
          }
      }
			stage('Build/Push Image') {
					steps {
						echo "Build and Push docker images"
							// sh """
						sh 'node --version'
						
						echo "Building Artifact"
					}
			}
			stage('Deploy') {
					steps {
							sh 'whoami'
							sh 'docker images'
							echo "Deploy Code"
					}
			}
   }
}
