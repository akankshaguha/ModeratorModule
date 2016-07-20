#!groovy

stage 'CLONE_DEVELOPER_MODULE'
node {
 git 'https://github.com/exorcist007/DeveloperModule.git'
}
stage 'CLONE_CLEAN_DEVELOPER_MODULE'
node {
   	bat 'gradle clean --info'
   
}
stage 'BUILD_DEVELOPER_MODULE'
node {
   	bat 'gradle build --info'
}
stage 'CREATE_ARTIFACT_DEVELOPER_MODULE'
node {
   
   	bat 'gradle jar --info'
   
}
stage 'CLONE_MODERATOR_MODULE'
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
}
stage 'CLEAN_MODERATOR_MODULE'
node {
   
   	bat 'gradle clean --info'
   
}
stage 'BUILD_MODERATOR_MODULE'
node {
  	bat 'gradle build --info'
}
