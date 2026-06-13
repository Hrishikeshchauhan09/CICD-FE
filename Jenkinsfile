pipeline{
    agent any
    stages{
          stage('Build'){
            steps{
                sh 'npm install'
                }
            }  
        stage('build'){
        steps{
            sh 'npm run build'
            }
        }
         stage('Deploy'){
         steps{
            echo 'Deploying...'
            sh '''
            sudo cp -r dist/* /var/www/html/
            sudo systemctl restart nginx
            '''
        }
    }

    }
 }
