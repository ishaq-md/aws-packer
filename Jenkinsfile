pipeline {

     environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
    
   agent  any
           
        stages {
        stage ('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/ishaqmdgcp/aws-packer.git'
            }
        }

         stage('packer inspect') {
            steps {
                sh 'packer version'
                sh 'packer inspect aws.json'
            }
    }
             
         stage('packer build') {
           steps {
               
                sh 'packer build aws.json'
            }
    }

  }
}
