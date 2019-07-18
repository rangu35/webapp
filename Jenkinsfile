pipeline {
    agent any 
    stages {
        stage ('Compile stage') {
            steps {
            withMaven(maven : 'maven-3') {
                 sh 'mvn clean compile'  
            }
          }
        }
        
        stage ('Testing stage') {
            steps {
            withMaven(maven : 'maven-3') {
                 sh 'mvn clean test'  
            }
          }
        }
         
       stage ('Deploy stage') {
            steps {
            withMaven(maven : 'maven-3') {
                 sh 'mvn deploy'  
            }
          }
        }  
         
        }
    }
