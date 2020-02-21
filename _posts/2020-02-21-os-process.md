---
layout: post
title:  "프로세스 관리-01"
date:   2020-02-21
desc: "컴퓨터 구조 공부"
keywords: "Computer Structure"
categories: [Os]
tags: [Computer Structure, Operation System]
icon: 
---

# 프로세스의 개념
* 실행중인 프로그램: program in execution   
  디스크에 존재하던 프로그램이 메모리에 적재됨.   
  프로그램이 CPU를 할당받아서 기계명령(instruction)을 수행하고 있는 상태.   
* 일반적으로 JOB이라는 용어와 Process를 혼용하여 사용하기도 함.   
   
* 프로세스 문맥: 프로세스가 어떤 상태에서 수행되고 있는지를 정확히 설명하기 위해 필요한 정보와 그 프로세스의 주소공간(코드, 데이터스택 상태)을 비롯해 레지스터에 어떤 값을 가지고 있는지와 시스템 콜등을 통해 커널에서 수행한 일의 상태, PCB등을 포함.   
* 프로세스 문맥을 크게 세 가지로 분류하면   
  하드웨어 문맥, 프로세스의 주소공간, 커널 상의 문맥으로 나누어 볼 수 있다.   
  이때, 하드웨어 문맥은 CPU의 수행상태를 나타내는 것으로 프로그램 카운터 값과 각종 레제스터에 저장되고 잇는 값들을 의미한다.   
   
---   
   
# 프로세스의 상태
![프로세스의 상태 변화도](https://eunhyejung.github.io/assets/contents/content07.PNG)  
   
* 프로세스의 상태는 실행(running), 준비(ready), 봉쇄(blocked, wait, sleep) 세 가지로 구분 할 수 있다.   
  * 실행상태: 프로세스가 CPU를 보유하고 있고, 기계어 명령을 실행중인 상태.   
  * 준비상태: 프로세스가 CPU를 보유하면 당장 명령을 실행 할 수 있지만, CPU를 할당받지 못한 상태.
  * 봉쇄상태: 프로세스에게 CPU를 주어도 당장 명령을 실행할 수 없는 상태.
   

  
