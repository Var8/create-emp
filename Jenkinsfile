pipeline {

  agent any
 
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "***** Skip Munit Test******"
      }
    }

     stage('Deployment') {
    
      steps {
            bat 'mvn clean package deploy -Pdev -DmuleDeploy'
      }
    }
   
  }
}