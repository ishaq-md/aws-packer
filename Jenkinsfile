pipeline {

     environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
    
   agent  any
  
    stages {
        stage('checkout') {
            steps {
                 script {
                        dir("aws-packer")
                        {
                            "https://github.com/ishaqmdgcp/aws-packer.git"
                        }
                    }
                }
            }

         stage('packer inspect') {
            steps {
               dir("") 
                {
                sh 'packer inspect aws.json'
            }
        }
    }

  }
}
