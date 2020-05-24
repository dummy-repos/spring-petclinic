node {
    stage('scm'){
        git 'https://github.com/dummy-repos/spring-petclinic.git'
    }

    stage('build'){
        sh 'mvn package'
    }
    
    stage('Sonar') {
        withSonarQubeEnv('SONAR-6.7.4') {
             sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
        }
    }
}
