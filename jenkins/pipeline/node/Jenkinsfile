#!groovy

@Library('jenkins-shared-lib')

def tools = new org.devops.tools()

String workspace = '/opt/jenkins/workspace'

pipeline {
    // 指定集群节点
    agent {
        node {
            label 'main'
            customWorkspace '${workspace}'
        }
    }
    // 选项
    options {
        timestamps() //日志会有时间
        skipDefaultCheckout() //删除隐式checkout scm语句
        disableConcurrentBuilds() //禁止并行
        timeout(time: 1, unit: 'HOURS') //流水线超市设置1h
    }
    // 声明全局变量
    environment {
        key = 'value'
    }
    // 流水线阶段
    stages {
        stage('Checkout') {
            steps {
                timeout(time: 5, unit: "MINUTES"){
//                     checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/liuzhaomax/maxblog-fe-main.git']]])
                    script{
                        tools.PrintMsg("我的共享lib")
                    }
                }
            }
        }
        stage('Update GitHub') {
            steps {
                echo 'Update GitHub - SUCCESS'
            }
        }
        stage('Change Node Version') {
            steps {
                echo 'Change Node Version - SUCCESS'
            }
        }
        stage('App Version') {
            steps {
                echo 'App Version - SUCCESS'
            }
        }
        stage('Lint') {
            steps {
                echo 'Lint - SUCCESS'
            }
        }
        stage('Build') {
            steps {
                echo 'Build - SUCCESS'
            }
        }
        stage('Static Analysis') {
            steps {
                echo 'Static Analysis - SUCCESS'
            }
        }
        stage('SonarQube') {
            steps {
                echo 'SonarQube - SUCCESS'
            }
        }
        stage('Nessus') {
            steps {
                echo 'Nessus - SUCCESS'
            }
        }
        stage('Build Image') {
            steps {
                echo 'Build Image - SUCCESS'
            }
        }
        stage('Git Tag') {
            steps {
                echo 'Git Tag - SUCCESS'
            }
        }
        stage('Package Config') {
            steps {
                echo 'Package Config - SUCCESS'
            }
        }
    }
}