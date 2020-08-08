---
layout: post
title: "How to write Dockerfile reasonable"
date: 2020-08-08
categories:
  - "Docker"
description:
image: "../../../../../side/img/docker/docker.png"
image-sm: "../../../../../side/img/docker/docker.png"
---
<h2>How to write Dockerfile reasonable</h2>

<h3>change</h3>
<figure>
  	<img src="../../../../../side/img/docker/before-nodejs-dockerfile.png" alt="first step"/>
	<img src="../../../../../side/img/docker/after-nodejs-dockerfile.png" alt="second step"/>
	<ul>
		<li>앞에 사진에선 모든 정보를 app dir에 copy한다. 그리고 npm install을 하게 된다. 이럴경우 만약 코드가 변경되었으면 npm install또한 다시 진행하게된다.</li>
		<li>package.json과 같이 버전 정보를 담고 있다면 자주 바뀌지 않는다.</li>
		<li>code는 자주 바뀌면서 배포가 돼기 때문에 cache check할때 먼저 package.json과 같이 자주 안바뀌는 정보를 먼저 탐색 후 cache가 동일할 경우 npm install을 다음에 안해도된다.</li>
	</ul>
</figure>