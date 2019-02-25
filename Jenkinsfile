node{
    stage('SCM Checkout'){
        
        git 'https://github.com/senalishalika/JenkinsTraining'
    }
    stage('Initialize'){
        //def dockerHome = tool 'myDocker'
        def mavenHome  = tool 'myMaven'
        env.PATH = "${mavenHome}/bin:${env.PATH}"
        
    }
     stage('Compile'){
         def mavenHome  = tool 'myMaven'
         echo "${mavenHome}/bin/mvn clean compile"
    }
    
    stage('Testing Stage'){
         def mavenHome  = tool 'myMaven'
         echo "${mavenHome}/bin/mvn test"
    }
    
    stage('Deployment Stage'){
         def mavenHome  = tool 'myMaven'
         echo "${mavenHome}/bin/mvn deploy"
    }
   
}
