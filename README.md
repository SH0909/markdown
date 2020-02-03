# markdown

# 1.마크다운에 대해서
## 1-1.마크다운의 정의
Markdown은 텍스트 기반의 마크업 언어로 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. github의 저장소 repository에 관한 정보를 기록하는 README.md는 github를 이용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운이다. 
## 1-2.마크다운의 장단점
### 장점
1.간결하다

2.다양한 형태로 변환이 가능하다

3.텍스트로 저장되기 때문에 용량이 적어 보관이 용이하다

4.지원하는 프로그램과 플랫폼이 다양하다
### 단점
1.표준이 없다

2.모든 HTML 마크업을 대신하지 못한다
***
# 2.마크다운 문법
## 2-1. Header
글머리는 1부터 6까지 있으며 숫자가 커질수록 글씨 크기가 작아진다. #의 개수로 숫자를 나타낸다

```
# This is a h1
## This is a h2
### This is a h3
#### This is a h4
##### This is a h5 
###### This is a h6
```
# This is a h1
## This is a h2
### This is a h3
#### This is a h4
##### This is a h5 
###### This is a h6

## 2-2.BlockQuote
```
> 블럭 인용문자를 사용한다

>This is a first
>>This is a second
```
>This is a first
>>This is a second

## 2-3.목록
### 순서있는 목록
순서 있는 목록은 숫자와 점을 사용한다 띄어쓰기가 필요하다.
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

### 순서없는 목록
*,+,-를 사용한다 들여쓰기에 따라 기호가 달라진다
```
* 첫번째
    * 두번째
        * 세번째
```
* 첫번째
    * 두번째
        * 세번째


## 2-4.코드
### 들여쓰기
Tab을 만나면 들여써진다. 한 줄 공백 간격이 필요하다.
```
This is a normal paragraph: 

    This is a code block.

end code block.
```
This is a normal paragraph: 

    This is a code block.

end code block.

### 코드블럭
* ```<pre><code>{}</code></pre> 이용하기```

```
<pre>
<code>
print("Hello world"!)
</code>
</pre>
```
<pre>
<code>
print("Hello world"!)
</code>
</pre>

* 코드블럭코드("```") 이용하기

```
print("Hello world!")
```
## 2-5.수평선
```
***
- - -
등을 사용하여 수평선을 나타낼 수 있다.
```
*** 
- - -

## 2-6.링크
### 참조링크
```
[link keyword][id]
[id]:url "title"
```
Link:[Google][Googlelink]

[Googlelink]:https://google.com "go google"

### 외부링크
```
[Title](link)
```
Link:[Google](https://google.com)
### 자동연결
일반적인 URL 혹은 이메일 주소
```
이메일:<address@example.com>
```
이메일:<address@example.com>

## 2-7.강조
*,_을 사용한다 취소선은 ~~을 사용한다
```
*hello*
_hello_
**hello**
__hello__
~~hello~~
```
*hello*

_hello_

**hello**

__hello__

~~hello~~

## 2-8.이미지
```
![Alt text](링크)
<img src="링크"> width,height 속성 사용 가능
```
<img src="https://pbs.twimg.com/media/DqLqEgCUwAAon8p.jpg" width="300px" height="300px"></img>

## 2-9.줄바꿈
줄 바꿈을 하기 위해서는 마지막 문장에서 3칸 이상 띄워써야 한다    
세칸 띄움~

### 출처
https://gist.github.com/ihoneymon/652be052a0727ad59601#11-%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4%EC%9D%B4%EB%9E%80

***
# 간단 깃헙 사용법
1. 사용자 정보 입력   
git config --global user.name "user name"   
git config --global user.email "user email"
2. 터미널에서 "git clone 주소"를 실행해 repository로부터 특정 프로젝트를 다운받는다
3. git add / git commit -m "message"/ git push : git에 push 하기
4. git pull 주소
```
push:local repository의 변경사항이 remote repository에 반영된다.
pull:remote repository 변경사항이 local repository에 반영된다.
```
5. git log: 현재 commit 상태 및 local repository 파일 확인
6. git checkout <checkout 해시값>: 로컬 변경 내용 되돌리기
7. git branch <branch_name>: branch 만들기
8. git branch: branch 리스트 확인
9. git checkout <branch_name>: branch 이동
10. merge(합치기)   
master branch로 이동 후 git merge <branch_name>
11. git branch -d <branch_name> : branch 삭제하기