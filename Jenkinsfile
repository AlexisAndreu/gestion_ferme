node {

stage('SCM'){
 git 'https://github.com/AlexisAndreu/gestion_ferme'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.11:9000/ -Dsonar.login=75a1cad17e57c90e1b2fc6e434f35181ab7a3e29"
    }
}
