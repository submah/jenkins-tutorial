node ('master'){
    stage('Cloning From Git'){
            
            git changelog: false, poll: false, url: 'https://github.com/submah/maven-jenkins-job.git'
        }
    stage('Build with Maven'){
        sh 'mvn clean package'
        
    }    
    stage('Deplly to Tomcat'){
        deploy adapters: [tomcat8(credentialsId: '3516710f-9b6f-4da9-8bfd-b9e9a65f06dd', path: '', url: 'http://35.225.166.243:8090')], contextPath: 'pipeline', onFailure: false, war: '**/*.war'
        
    }
}	
