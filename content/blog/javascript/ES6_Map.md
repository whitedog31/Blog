---
title: ES6 Map
date: 2021-03-27 15:03:46
category: javascript
thumbnail: { thumbnailSrc }
draft: false
---

# Map

- 반복문을 돌며 배열 내의 원소를 1:1로 짝을 지어준다.
- 즉, 배열은 1:1로 짝을 지어 생성하되, `기존 배열을 변형을 가하지 않고 새로 생성한다`. -> immutable

```javascript
// 배열 선언
const oneTwoThree = [1, 2, 3]

// 배열 안에 원소를 순회 -> 1:1
let result = oneTwoThree.map((v, i) => {
  console.log('resutl', v)
  return v
})

// 콘솔에는 1, 2, 3이 찍힘
oneTwoThree // [1, 2, 3]
result // [1, 2, 3]
console.log(oneTwoThree, result)

// 비교 했을 경우 false 가 나옴 -> 이유는
// map 통해 나온 배열은 기존 배열과 다름 -> 다른 객체
// 즉, 새로운 배열을 생성

let compare = oneTwoThree === result
console.log(compare) // false
```

## Example2

- 배열 내의 모든 원소의 +1 하기

```javascript
// example2
const result2 = oneTwoThree.map((v, i) => {
  return v + 1
})

console.log(result2) // [2, 3, 4]
```

## Example3

- 2로 나누어 떨어지면 짝수, 그렇지 않으면 홀수

```javascript
const result3 = oneTwoThree.map((v, i) => {
  if (v % 2 === 0) {
    return 'Even'
  } else {
    return 'Odd'
  }
}, [])

console.log(result3)
```

# Refernce

제로초님 블로그 :
https://www.zerocho.com/category/JavaScript/post/5acafb05f24445001b8d796d
