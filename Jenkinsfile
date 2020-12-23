
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
node {
 stage('checkout') {
  checkout scm
 }
 stage('deploy') {
  echo 'branch name ' + env.BRANCH_NAME
 
  if (env.BRANCH_NAME.startsWith("Feature_")) {
   echo "Deploying to Dev environment after build"
  } else if (env.BRANCH_NAME.startsWith("Release_")) {
   echo "Deploying to Stage after build and Dev Deployment"
  } else if (env.BRANCH_NAME.startsWith("master")) {
   echo "Deploying to PROD environment"
  }
 
  sh ""
  "chmod +x script.sh 
  . / script.sh ""
  "
 
 }
}
