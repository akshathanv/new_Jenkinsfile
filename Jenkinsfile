node{
  stage 'Checkout'
  git url: 'https://github.com/akshathanv/Jpetstore_maven.git'   
  // Clean any locally modified files and ensure we are actually on origin/master
  // as a failed release could leave the local workspace ahead of origin/master
  sh "git clean -f && git reset --hard origin/master"
}
  
  docker.image('maven:3.3.3-jdk-8').inside {
  sh 'mvn -B clean install'
}
