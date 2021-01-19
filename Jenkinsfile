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
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.11:9000/ -Dsonar.login=77f3861e4e1fb6918faeb0e3a47046b40bf42278"
    }
}
