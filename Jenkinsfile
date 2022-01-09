node { 
 
 stage('clone') {
    
    git 'https://github.com/HaniOUKIL/projet_hocem.git'

 }
 
  stage('Build') {
    
      sh 'mvn clean install package'

 }
 
 stage('Deploy') {
    
     ansiblePlaybook become: true, inventory: 'hosts', playbook: 'copy.yml'

 }
 
    
}
