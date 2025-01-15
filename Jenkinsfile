pipeline {
    agent any
    tools {
        maven "Maven3"
        jdk "OracleJDK17"
    }
    
    environment{
         SNAP_REPO = 'vprofile-snapshot'
         NEXUS_USER = 'admin'
         NEXUS_PAASWORD = 'admin1234'
         RELEASE_REPO = 'vprofile-release'
         CENTRAL_REPO = 'vprofile-maven-central'
         NEXUSIP = '172.31.25.190'
         NEXUSPORT = '8081'
         NEXUS_GRP_REPO = 'Vpro-maven-group'
         NEXUS_LOGIN = 'nexuslogin'
    }
    

    stages {
        stages('Build'){
            steps {
                  sh 'mvn -s settings.xml -DskipTests install'
            }
        } 

    }
}
