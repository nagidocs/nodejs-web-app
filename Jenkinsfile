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
						sh 'whoami'
						echo "Building Artifact"
					}
			}
			stage('Deploy') {
					steps {
							sh 'sudo docker images'
							echo "Deploy Code"
					}
			}
   }
}
