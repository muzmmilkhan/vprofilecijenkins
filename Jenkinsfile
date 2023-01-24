pipeline {
	agent any
	tools {
        jdk "openjdk15"
        maven "mvn"
    }
    environment {
        NEXUS_VERSION = "nexus3"
        NEXUS_USER = "admin"
        NEXUS_PASS = "admin123"
        NEXUS_PROTOCOL = "http"
        NEXUSIP = "172.31.11.32"
        NEXUSPORT = "8081"
        RELEASE_REPO = "vprofile-release"
        CENTRAL_REPO = "vpro-maven-central"
        SNAP_REPO = "vprofile-snapshot"
	    NEXUS_GRP_REPO  = "vprofile-grp-repo"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
    }
    stages{    
        stage('BUILD'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }         
        }	
    }
}
