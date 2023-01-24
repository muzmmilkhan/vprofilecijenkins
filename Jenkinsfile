pipeline {
	agent any
	tools {
        jdk "openjdk15"
        maven "mvn"
    }
    environment {
        NEXUS_VERSION = "nexus3"
        NEXUS-USER = "admin"
        NEXUS-PASS = "admin123"
        NEXUS_PROTOCOL = "http"
        NEXUSIP = "172.31.11.32"
        NEXUSPORT = "8081"
        RELEASE-REPO = "vprofile-release"
        CENTRAL-REPO = "vpro-maven-central"
        SNAP-REPO = "vprofile-snapshot"
	    NEXUS-GRP-REPO  = "vprofile-grp-repo"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
    }
    stages{    
        stage('BUILD'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }         
        }	
    }
}
