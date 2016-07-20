#!groovy
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
}
node{
step([$class: 'CopyArtifact', filter: '../repo/DeveloperProject.jar', projectName: 'DeveloperModule/', selector: [$class: 'StatusBuildSelector', stable: false], target: 'C:\\JENKINS_HOME\\jenkins_home\\jobs\\ModeratorModule\\repo'])

}
stage 'CLEAN_MODERATOR_MODULE'
node {
   
   	bat 'gradle clean --info'
   
}

stage 'BUILD_MODERATOR_MODULE'
node {
  	bat 'gradle build --info'
}
stage 'TEST_MODERATOR_MODULE'
node {
  	bat 'gradle test --info'
}
