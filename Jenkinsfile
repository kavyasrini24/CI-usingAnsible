pipeline {
    agent any
        
         stage('Execute Maven') {
           steps {
             
                sh 'mvn package'             
          }
        }
        
        stage('Ansible Deploy') {
             
            steps {
    
               sh "ansible-playbook main.yml -i inventories/dev/hosts --user jenkins --key-file ~/.ssh/id_rsa"

               
            
            }
        }
    }

