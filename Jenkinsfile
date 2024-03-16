pipeline {
        agent{
        label 'mens-slave'
        }
        stages {
            stage('Checkout') {
                steps {
                        checkout scm
                      }}
                stage('Build') {
                   steps {
                          sh ' /home/admin/apache-maven-3.9.6/bin/mvn install'
                         }}
                stage('Deployment'){
                    steps {
                        sh 'cp target/prod3.war /home/admin/apache-tomcat-9.0.86/webapps'
                        }}
}}

