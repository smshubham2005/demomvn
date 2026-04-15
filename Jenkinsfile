pipeline{
agent any
tools{
maven 'MAVEN'
}
stages{
stage('Checkout')
{steps{
git branch: 'main',url: 'https://github.com/demomvn.git'}
}
stage('Build'){
steps{'mvn clean package'}
}
stage('Test'){
steps{'mvn test'}
}
stage('Run Application'){
steps{
'java -jar  /target/MyMavenApp-1.0-SNAPSHOT.jar'}
}}
post{
success{'yes'}
failure{'no'}
}
}
