  
pipeline {
   agent any

   
   environment {

     
     SERVICE_NAME = "hello_microservice"
     REPOSITORY_TAG="${ORGANIZATION_NAME}-${SERVICE_NAME}:${BUILD_ID}"
   }   
   
   stages {
     
      stage('Preparation') {
         steps {
            cleanWs()
            git credentialsId: 'GitHub', url: 'https://github.com/pipeline-testing/project1.git'           
         }
      }

      stage('Clone application repo'){

         agent{
              docker {
                 image 'ansible_main_ansible'
                 reuseNode true
              }
         }

          steps{ 
                sh 'ansible-playbook application.yml  '
             
              
          }    
      }

      
      stage('Build Jar') {
          steps {
            sh './application/gradlew build -p ./application'
          }
      }

      stage('Run ansible'){

         agent{
              docker {
                 image 'ansible_main_ansible'
                 reuseNode true
              }
         }

          steps{ 
                sh 'ansible-galaxy collection install community.kubernetes'
                sh 'ansible-playbook demo.yml -e "image=$REPOSITORY_TAG" '
             
              
          }    
      } 
   }
}
