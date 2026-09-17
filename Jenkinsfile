pipeline {
 agent any
 stages {
 stage('Checkout') {
 steps {
 git branch: 'main',
 url: 'https://github.com/vaishnavik2024a-hash/ass7_p3.git'
 }
 }
 stage('Parallel Checks') {
 parallel {
 stage('Frontend Check') {
 steps {
 bat 'python frontend_check.py'
 }
 }
 stage('Backend Check') {
 steps {
 bat 'python backend_check.py'
 }
 }
 }
 }
 stage('Summary') {
 steps {
 echo 'Frontend and Backend examination checks are complete.'
 }
 }
 }
}
