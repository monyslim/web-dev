pipeline{
    agent any
    stages {
        stage("test"){
            steps{
                sh '''
                        echo "welcome to the test"

                    '''
            }
        }


         stage("production"){
            steps{
                sh '''
                        echo "welcome to the production. Added Jenkins"
                        ssh -o StrictHostKeyChecking=no -T -i /var/lib/jenkins/dev.pem ubuntu@ec2-13-41-80-68.eu-west-2.compute.amazonaws.com

                        sudo apt update -y

                        cd /var/www

                        sudo rm -rf html

                        git clone https://github.com/monyslim/web-dev.git html

                        

                    '''
            }
        }

    }
}