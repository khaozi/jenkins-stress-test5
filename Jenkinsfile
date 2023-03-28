#!groovy
node('master') {

    stage('stage1: Git checkout main branch') {
        sh "cd jenkins-stress-test5 && git pull origin main"
    }

    stage('stage2: and delete old versions') {
        // sh "rm -rf ${WORKSPACE}@script/*/migrations"
        echo "copy and delete old versions"
    }

    stage('stage3: copy to target host'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "copy to target host"
    }

    //stage('Deploy:makemigrations') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml --tags='makemigrations' -e \"host=172.26.129.143\""
    //}
    //stage('Deploy:migrate') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='migrate' -e \"host=172.26.129.143\""
    //}
    stage('stage4: pre-restart check env'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "stage 4: pre-restart check env"
    }
    stage('stage5: pre-restart check md5sum'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "stage5: pre-restart check md5sum"
    }
    stage('stage 6: scp oldfiles to remote and calculations'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "stage 6: scp oldfiles to remote"
        sh "echo 'The sum of numbers from 1 to 100 is \$(seq 1 100 | paste -sd+ | bc)'"
    }
    stage('stage7: check remote md5sum'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "check remote md5sum "
    }
    stage('stage8: roll-upgrade'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "stage8: roll-upgrade"
    }
    stage('stage9: check configfile'){
        // sh "scp -r ${WORKSPACE}/backend/* root@172.26.129.143:/opt/test-platform/test-platform/backend/"
        echo "stage9: check config file"
    }
    stage('stage 10: Deploy:restart') {
        // sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='restart' -e \"host=172.26.129.143\""
        echo  "deploy restart test"
    }
    //stage('Deploy:curl_test') {
    //    sh "ansible-playbook ${WORKSPACE}/backend/test_platform.yml  --tags='curl_test' -e \"host=172.26.129.143\""
    //}
}

