---
layout: post
title: "docker instruction"
date: 2020-07-05
categories:
  - "Docker"
description:
image: "../../../../../side/img/docker/docker.png"
image-sm: "../../../../../side/img/docker/docker.png"
---
<h2>Docker study 01</h2>

<ul>
  <li>Docker</li>
  <li>Instuction</li>
</ul>

<h3>Docker</h3>
<figure>
  <img src="../../../../../side/img/docker/docker.png" alt="docker"/>
  <h4>definition</h4>
  <p>
  	linux 응용프로그램들을 소프트웨어 컨테이너 안에 배치시키는 일을 자동화하는 오픈 소스 프로젝트이다.
  </p>
  <h4>container</h4>
  <p>
  	격리된 공간에서 프로세스가 동작하는 기술이다.
  </p>
</figure>

<h3>Instruction</h3>

<figure>
	<ul>
		<li>docker --version : version check</li>
		<li>docker run -p 5000:5000 kkh/hello-world:0.0.1.RELEASE : 만약 hello-world project가 현재 내 images에 존재하면 그것을 실행시키고 아닐 경우 image를다운 받아서 실행한다(나의 컴퓨터의 5000번 port 사용, 실제 프로세스 port또한 5000이다)</li>
		<li>docker run -d -p 5001:5000 kkh/hello-world:0.0.1.RELEASE : 해당 이미지를 back ground에서 실행하게 해준다.</li>
		<li>docker container ls : 현재 실행 중인 docker container들의 정보를 보여준다.</li>
		<li>docker container stop 1acd06667b0f : 1acd06667b0f 의 container id 를 가지는 container을 실행을 멈춘다.</li>
		<li>docker container ls -a : 모든 실행 제거 log들을 보여준다</li>
		<li>docker pull mysql : download mysql container</li>
		<li>docker search mysql : mysql의 다운받을 수 있는 모든 container images들이 존재 한다.</li>
		<li>docker image history kkh/hello-world:0.0.1.RELEASE : 해당 image에 대한 layer정보를 보여준다.</li>
		<li>docker image inspect 100229ba687e : image에 대한 더 디테일한 정보를 볼 수 있다.</li>
		<li>docker image remove mysql : mysql image를 삭제하는 명령어</li>
		<li>docker container run -d -p 5000:5000 kkh/hello-world:0.0.1.RELEASE : 해당 이미지를 출력해준다.</li>
		<li>docker container stop CONTAINER_ID : CONTAINER_ID에 해당하는 container를 중단한다 -> container중지한다.</li>
        <li>docker container kill CONTAINER_ID : CONTAINER_ID에 해당하는 container를 중단한다 -> 즉시 바로 container 중단</li>
        <li>docker system df : docker가 디스크사용하는 내용을 보여준다</li>
        <li>docker system events : 이 명령어 실행 이후의 docker의 event log를 전부 출력</li>
        <li>docker system prune -a : 현재 실행중인 image 빼고 전부 제거</li>
        <li>docker run -d -p 5001:5000 -m 512m kkh/hello-world:0.0.1.RELEASE : 해당 이미지를 실행할 때 최대 512MB밖에 사용할 수 없음</li>
        <li>docker run -d -p 5001:5000 -m 512m --cpu-quota=5000 kkh/hello-world:0.0.1.RELEASE : (quota : 100,000 정도 존재)50,000정도의 CPU를 할당 할 수 있음 -> CPU의 50%만 사용</li>
	</ul>
</figure>
