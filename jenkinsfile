node{
    def WORKSPACE= "/var/lib/jenkins/workspace/spring-boot-deploy"
    def dockerImageTag = "springboot-deploy${env.BUILD_NUMBER}"

    try{
        stage("clone repo"){
            git url: 'https://github.com/yegecali/SpringCiCd.git'
        }
        stage("build docker"){
            dockerImage = docker.build("springboot-deploy${env.BUILD_NUMBER}")
        }
    }catch(e){
        return e
    }
}