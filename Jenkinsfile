pipeline {
   agent any
stages {
   
   stage('image check'){
        steps{
                sh 'docker images'
             }
        }
   stage('image build'){
        steps{
                sh 'docker build -t apache2exam .'
                sh 'docker images'
             
             }
        }
   stage('dockerhub login'){
        steps{
                sh 'docker login -u subhadipdocker -p 7699676975'
             }
        }
   stage('image push'){
       steps{ 
            sh 'docker tag apache2exam subhadipdocker/subhadip:apacheexam'
            sh 'docker push subhadipdocker/subhadip:apacheexam'
            }
       }
   } 
}
