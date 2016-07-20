#!groovy
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
}

stage 'CLEAN_MODERATOR_MODULE'
node {
   
   	bat 'gradle clean --info'
   
}
node{
step([$class: 'CopyArtifact', projectName: 'DeveloperModule', selector: [$class: 'StatusBuildSelector', stable: false], target: 'C:\\JENKINS_HOME\\jenkins_home\\jobs\\ModeratorModule\\workspace\\repo'])
}
stage 'BUILD_MODERATOR_MODULE'
node {
  	bat 'gradle build --info'
}
stage 'TEST_MODERATOR_MODULE'
node {
  	bat 'gradle test --info'
}
