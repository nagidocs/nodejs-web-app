// Jenkins multibranch pipeline CI pipeline.
pipeline {
   agent any
   stages {
      stage('Test Code') {
          steps {
              //  sh """
               echo "Deploying Code"
          }
      }
			stage('Build/Push Image') {
					steps {
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
