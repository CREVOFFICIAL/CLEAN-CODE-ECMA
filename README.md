# CLEAN-CODE-ECMA
> ryanmcdermott의 clean-code-javascript 저장소 내용을 학습하며 정리한 내용입니다.
[_link_](https://github.com/ryanmcdermott/clean-code-javascript)

* 스타일 가이드가 아닙니다. 읽기 쉽고 재사용 가능하며 리팩토링 가능한 소프트웨어를 만드는 가이드입니다.

## 목차
1. [Variables](#variables)
2. [Functions](#functions)
3. [Objects and Data Structures](#objects-and-data-structures)
4. [Classes](#classes)
5. [SOLID](#solid)
6. [Testing](#testing)
7. [Concurrency](#concurrency)
8. [Error Handling](#error-handling)
9. [Formatting](#formatting)
10. [Comments](#comments)

## **Variables**

### 의미가 있고 발음하기 쉬운 변수 이름을 사용합시다.

**나빠요**
```javascript
const yyyymmdstr = moment().format("YYYY/MM/DD");
```

**좋아요**
```javascript
const currentDate = moment().format("YYYY/MM/DD");
```

### 동일한 유형의 변수에 동일한 어휘 사용합시다.

**나빠요**
```javascript
getUserInfo();
getClientData();
getCustomerRecord();
```

**좋아요**
```javascript
getUser();
```

### 검색이 가능한 이름을 사용합시다.

우리는 우리가 쓰는 것보다 더 많은 코드를 읽을겁니다.
코드를 읽기 좋고 검색 가능하게 작성해야 합니다.

**나빠요**
```javascript
// 86400000가 뭔가요..?
setTimeout(blastOff, 86400000);
```

**좋아요**
```javascript
const MILLISECONDS_IN_A_DAY = 86400000;
setTimeout(blastOff, MILLISECONDS_IN_A_DAY);
```


