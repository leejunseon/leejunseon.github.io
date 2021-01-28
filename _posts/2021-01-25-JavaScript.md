---
layout: post
title: "JavaScript"
subtitle: 정리
tags: [FrontEnd]
---

# JavaScript

- 이벤트 종류 : **mdn**(https://developer.mozilla.org/ko/) - JavaScript DOM Event 검색
- 변수와 상수
  - 변수 : let
  - 상수 : const
- String 처리

  - `와 ${} 사용 가능.
  - ex 1)  
    const minutes = date.getMinutes();  
    const hours = date.getHours();  
    clockTitle.innerText = \`${hours}:${minutes}\`;  
    ex 2)  
    const seconds = date.getSeconds();  
    clockTitle.innerText = \`${seconds<10?\`0${seconds}\`:\`${seconds}\`}\`;

- 자주 쓰이는 function
  - setInterval(함수, 시간) : 입력한 시간마다 함수 실행
- querySelector
  - css와 같은 방식으로 Element들 DOM에서 가져올 수 있음.
  - 자식 Element를 가져옴.
  - querySelector는 첫번째 것을 가져오고, querySelectorAll은 모든 것을 가져옴(list로 받아야함)
  - ex)  
    const form = document.querySelector(".js-form"),  
    input = form.querySelector("input");
