pipeline {
    agent any
    tools {
        maven "Maven3"
        jdk "OracleJDK17"
    }
    
    environment{
         SNAP_REPO = 'vprofile-snapshot'
         NEXUS-USER = 'admin'
         NEXUS-PAASWORD = 'admin1234'
         RELEASE-REPO = 'vprofile-release'
         CENTRAL-REPO = 'vprofile-maven-central'
         NEXUSIP = '172.31.25.190'
         NEXUSPORT = '8081'
         NEXUS-GRP-REPO = 'Vpro-maven-group'
         NEXUS-LOGIN = 'nexuslogin'
    }
    

    stages {
        stage('Build'){
            steps {
                  sh 'mvn -s settings.xml -DskipTests install'
            }
        } 

    }
}
