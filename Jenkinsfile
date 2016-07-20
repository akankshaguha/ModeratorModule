#!groovy
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
 step([$class: 'CopyArtifact', filter: '*.jar', fingerprintArtifacts: true, flatten: true, projectName: 'DeveloperModule/', selector: [$class: 'StatusBuildSelector', stable: false], target: 'ModeratorModule/'])


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
