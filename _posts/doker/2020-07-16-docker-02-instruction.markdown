---
layout: post
title: "docker instruction"
date: 2020-07-16
categories:
  - "Docker"
description:
image: "../../../../../side/img/docker/docker.png"
image-sm: "../../../../../side/img/docker/docker.png"
---
<h2>Docker study 02</h2>

<h3>Dockerfile</h3>
	<ul>
		<li>FROM : 어떤 이미지를 기반으로 현재 이미지를 생성할지 결정 한다. 생략불가, 맨앞에 와야함, 기존 layer에서 부터 시작할 수 있는 명령어들 -> FROM <image> FROM <image>:<tag> FROM <image>@<digest></li>
		<li>MAINTAINER <작성자 정보> : 이밎를 생성한 사람의 정보이며, 형식은 자유이다.</li>
		<li>RUN <command> : FROM 에서 설정한 이미지 위에 스크립트 혹은 명령 실행해야 할 것들. 그러나 FROM으로 설정한 이미지에 포함된 /bin/sh 실행 파일이 없으면 사용불가능 하다.</li>
		<li>CMD ["<실행파일>","<매개 변수>","<매개 변수2>"]: 컨테이너가 시작되었을때 스크립트 혹은 명령 실행되는 것들(ex : docker run이나 docker start 명령 실행 될때 실행)</li>
		<li>ENTRYPOINT : 기본적으로 CMD와 기능과 동일하다 하지만 docker run명령에서 실행 파일의 하나의 매개 변수로 받아지게 된다. --entrypoint 옵션을 사요할 경우 Dockerfile에서 설정한 ENTRYPOINT는 무시한다.</li>
		<li>EXPOSE : </li>
	</ul>

<h3>Instruction</h3>

<figure>
	<ul>
		<li>docker build -t kkh/hello-world-python:0.0.2.RELEASE . : Dockerfile을 parse 해서 build 해준다
			<ul>
				<li>kkh/hello-world-python : image name</li>
				<li>0.0.2.RELEASE : tag</li>
			</ul>
		</li>
		<li>docker run -p 5000:5000 -d kkh/hello-world-python:0.0.2.RELEASE : build된 docker image를 container로 실행</li>>
	</ul>
</figure>
