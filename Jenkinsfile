#!groovy

stage 'CLONE_MODERATOR_MODULE'
node {
 git 'https://github.com/exorcist007/ModeratorModule.git'
}
stage 'copy_artifact'
node{
//step([$class: 'CopyArtifact', fingerprintArtifacts: true, projectName: 'DeveloperModule/', selector: [$class: 'StatusBuildSelector', stable: false], target: '../ModeratorModule/repo'])
//step([$class: 'CopyArtifact', fingerprintArtifacts: true, projectName: 'DeveloperModule/', selector: [$class: 'SpecificBuildSelector', buildNumber: '1'], target: 'ModeratorModule/repo/'])
step([$class: 'CopyArtifact', fingerprintArtifacts: true, projectName: 'DeveloperModule/', selector: [$class: 'TriggeredBuildSelector', allowUpstreamDependencies: true, fallbackToLastSuccessful: true, upstreamFilterStrategy: 'UseGlobalSetting'], target: 'ModeratorModule/repo/'])

 
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
