#!groovy
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
step([$class: 'CopyArtifact', flatten: true, projectName: 'DeveloperModule/5/execution/node/32/ws/build/libs/', selector: [$class: 'TriggeredBuildSelector', allowUpstreamDependencies: true, fallbackToLastSuccessful: false, upstreamFilterStrategy: 'UseNewest'], target: '../ModeratorModule/repo/'])






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
