// Jenkins multibranch pipeline CI pipeline.
pipeline {
  environment {
    BUILD_NUM_ENV = currentBuild.getNumber()
  }

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
						sh 'docker build -t nodejs-web-app:v$BUILD_NUM_ENV .'
						echo "Building Artifact"
					}
			}
			stage('Deploy') {
					steps {
							echo "Deploy"                            
                            sh 'export IMAGE_TAG=v$BUILD_NUM_ENV && docker-compose up'						
					}
			}
   }
}
