# QS Workshop SonarQube <!-- omit in toc --> 


## Contents <!-- omit in toc --> 

- [1. Overview](#1-overview)
- [2. Requirements](#2-requirements)
- [3. Workshop](#3-workshop)
  - [3.1. Setup SonarQube locally using docker-compose](#31-setup-sonarqube-locally-using-docker-compose)
  - [3.2. Create your project into SonarQube](#32-create-your-project-into-sonarqube)
  - [3.3. Run a static code analysis(SCA) using sonar-scanner against you project](#33-run-a-static-code-analysissca-using-sonar-scanner-against-you-project)
  - [3.4. Analyse the information derived from your source code quality analysis](#34-analyse-the-information-derived-from-your-source-code-quality-analysis)
  - [3.5. common best-practices regarding SCA and SonarQube](#35-common-best-practices-regarding-sca-and-sonarqube)

<br>

## 1. Overview

This workshop aims to guide your teams through the usage of SonarQube.
Thoughout this workshop we will learn the following subjects and abilities:

1. How to setup SonarQube locally using docker-compose
2. How to create your project into SonarQube
3. How to run a static code analysis(SCA) using sonar-scanner against you project
4. How to analyse the information derived from your source code quality analysis
5. What are the common best-practices regarding SCA and SonarQube

<br>

## 2. Requirements

You follow the workshop, you need to have this tools install on your computer:

* `docker`
* `docker-compose`

<br>

## 3. Workshop

### 3.1. Setup SonarQube locally using docker-compose


<br>

1. Clone the workshop GitHub project</b></summary>

```
git clone <repo-clone-url>
```

2. Move in the project and launch SonarQube

```
cd qs-workshop-sonarqube
docker compose -p workshop  -f source/etc/docker/docker-compose.yml up -d
```

3. Open the browser at [localhost:9000](localhost:9000)


<br>


### 3.2. Create your project into SonarQube

We have a SonarQube instance running on our local machine at [localhost:9000](localhost:9000). 
Let's create a **new project** on SonarQube to launch our first code scan.

<details><summary><b>Step 1: </b></summary>

</details>

<br>

<details><summary><b>Step 2:</b></summary>

</details>


<br>

### 3.3. Run a static code analysis(SCA) using sonar-scanner against you project

<details><summary><b>Step 1: </b></summary>

```
docker run \
    -e SONAR_HOST_URL="http://sonarqube:9000"\
    -e SONAR_LOGIN="<TOKEN>"\
    --net workshop_default\
    --rm -v "$(pwd):/app" \
    -it sonarsource/sonar-scanner-cli -Dsonar.projectKey=sites-ui -Dsonar.sources=/app

```

</details>

<br>

<details><summary><b>Step 2:</b></summary>

</details>

<br>

### 3.4. Analyse the information derived from your source code quality analysis

<details><summary><b>Step 1: </b></summary>

</details>

<br>

<details><summary><b>Step 2:</b></summary>

</details>


<br>

### 3.5. common best-practices regarding SCA and SonarQube

<details><summary><b>Step 1: </b></summary>

</details>

<br>

<details><summary><b>Step 2:</b></summary>

</details>






# 4. FAQ

sysctl -w vm.max_map_count=524288
sysctl -w fs.file-max=131072
