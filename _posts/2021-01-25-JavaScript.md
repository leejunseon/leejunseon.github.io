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
  - 이벤트.preventDefault() : 이벤트의 Default를 막는다.
  - querySelector
    - css와 같은 방식으로 Element들 DOM에서 가져올 수 있음.
    - 자식 Element를 가져옴.
    - querySelector는 첫번째 것을 가져오고, querySelectorAll은 모든 것을 가져옴(list로 받아야함)
    - ex)  
      const form = document.querySelector(".js-form"),  
      input = form.querySelector("input");
  - createElement : 자바스크립트에서 새로운 element를 생성.
    - ex) document.createElement("li");
  - appentChild : 자식element를 생성
    - ex) li.appendChild(delBtn); //delBtn을 li의 자식엘리먼트로 넣음.
  - removeChild :자식element를 제거

    - ex)

            function deleteToDo(event){
              const btn = event.target;
              const li = btn.parentNode;
              toDoList.removeChild(li);
            }

  - JSON.stringify() : 자바스크립트 object를 string으로 바꿔줌.
    - ex)  
      const toDos = [];  
      JSON.stringify(toDos)
  - JSON.parse() : string을 자바스크립트 object로 바꿔줌.
    - ex)  
      const loadedToDos = localStorage.getItem(TODOS_LS);  
      const parsedToDos = JSON.parse(loadedToDos);
  - Array.forEach() : Array의 각 element마다 괄호안의 내용을 실행.

    - ex)

            const parsedToDos = JSON.parse(loadedToDos);
            parsedToDos.forEach(function(toDo){
              paintToDo(toDo.text);
            })

  - Array.filter() : Array의 각 element마다 괄호안의 내용을 실행하고, 결과값이 true인 element만으로 새로운 Array를 만듦.

    - ex)

          const cleanToDos = toDos.filter(function(toDo){
            return toDo.id !== parseInt(li.id);
          });
