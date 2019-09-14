pipeline{
    agent any
stages{
    stage('SCM'){
        steps{git 'https://github.com/Vikash0110/Tomcat.git'}
    }
     stage('BUILD'){
        steps{bat label: '', script: 'mvn clean'
        bat label: '', script: 'mvn install'}
    }
     stage('Deploy'){
        steps{bat label: '', script: 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\Pipe\\target\\my-app.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'}
    }
}
}
