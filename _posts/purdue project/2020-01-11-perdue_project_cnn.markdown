---
layout: post
title: "CNN"
date: 2020-01-11
categories:
  - "Purdue-Project"
description:
image: "../../side/img/person/person.jpg"
image-sm: "../../side/img/purdue/airplane.jpg"
---
<h2>Convolutional Neural Networks</h2>

<ol>
  <li>Convolution</li>
  <li>Pooling</li>
  <li>Fully Connected</li>
</ol>

<h3>Convolution</h3>
<figure>
  <img src="../../../../../side/img/purdue/airplane.jpg" alt="airplane"/>
</figure>

<h3>R-CNN</h3>
<ul>
  <li>Detection System</li>
  <li>Using Region Proposal</li>
</ul>

<h2>YOLO</h2>
<h3>The YOLO Decection System</h3>
<ol>
  <li>resizes the input image to 448 x 448</li>
  <li>runs a single convolutional network on the image</li>
  <li>thresholds the resulting detections by the model's confidence</li>
</ol>

<h3>The detection way of YOLO</h3>
<ul>
  <li>이미지 pixel로부터 bounding box자료와 분류 과정을 single regression problem 으로 재정의</li>
  <li>이미지를 한번만 보고 Object가 무엇이고 어디 있는지를 알 수 있음</li>
  <li>image에서 작동하는 Single Convolution Network를 실행하여 물체의 bounding box와 bounding box안의 Objet가 무엇인지 동시에 예측</li>
</ul>

<h3>YOLO tade off</h3>
<ul>
  <li>분류 능력은 다른 분류시스템보다 떨어짐</li>
  <li>빠르게 object 식별하나, 작은 물체 검출이 힘듦 </li>
  <li>실험을 통하여 해당 내용과 관련된 trade off를 확인해야함</li>
</ul>

<h3>Unified Detection</h3>
<ul>
  <li>Component들을 single convolution network에 통합</li>
  <li>이미지로 얻은 feature들을 예측하고 탐지하는데 사용</li>
</ul>