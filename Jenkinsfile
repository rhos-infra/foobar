#!/usr/bin/env groovy

node() {

    // we don't want any leftovers to influence our execution (like previous logs)
    step([$class: 'WsCleanup'])

    checkout scm

    stage('build') {
        sh "set > .envrc"
    }

    archiveArtifacts artifacts: '.envrc'

} // node
