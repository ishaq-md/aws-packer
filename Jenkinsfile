pipeline {

     environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
    
   agent  any
     
      stages {
        stage ('checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/ishaqmdgcp/gcp-packer.git'
            }
        }

         stage('packer inspect') {
            steps {
            
                sh 'packer inspect aws.json'
            }
    }

  }
}
