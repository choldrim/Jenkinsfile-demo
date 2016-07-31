node("master"){
    stage 'git'
    git url:'https://cr.deepin.io/only-for-test', branch:'master'

    stage 'build & package'
    echo "npm install"
    echo "node node_modules/gulp/bin/gulp.js build"
    echo "package ..."
    sleep 3

    stage "test"
    echo "deploy to testing environment, testing..."
    sleep 5

    input "测试通过，是否部署？"
    stage 'Deploy'
    echo "deploying"
    sleep 2

    echo "finish."
}
