def greeting = 'HELLO FROM JENKINS WORLD';

node {
    stage('Git checkout') {
        git branch:'master', url:'https://github.com/DipenSolanki/pipe2.git'
    }
    stage('Execute Script') {
        sh 'chmod +x script.sh'
        sh 'sh script.sh'
    }
    stage('Notify via Email') {
        emailext body: 'BUILD IS GOOD', subject: 'BUILD PASS', to: 'sdipen1908@gmail.com'
    }
    stage('Print Environment Variables') {
       sh 'echo ${BRANCH_NAME}'
       sh 'echo ${BUILD_ID}'
       sh 'echo ${JOB_NAME}'
       sh 'echo ${greeting}'
    }
}
