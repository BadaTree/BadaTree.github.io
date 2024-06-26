## 📌 Fork한 저장소에 잔디가 안 심어질 때

> [Git으로 시작하는 협업 및 오픈소스 프로젝트](https://www.youtube.com/playlist?list=PLRx0vPvlEmdD5FLIdwTM4mKBgyjv4no81) 를 공부하여 Git의 설치부터 활용 방법까지 단계별로 배워보자 ! 
<br>

### 1️⃣   Issue Definition   

---
아래처럼 Fork한 (다른 사람의 레퍼지토리를 내 레퍼지토리로 복제해온 것) 저장소에서 comit&push를 했을 때 변경이 반영되지만 잔디에 반영이 되지 않는 문제 발생.

왜 반영이 안 되는지 이유를 정확히 파악하고, 아래 해결 방법으로 Fork한 저장소에서 한 comit&push가 contribution에 반영되도록 해결해보자 !

<br>

### 2️⃣  Cause of Issue

---
일반적으로, 원본 저장소의 기여는 해당 저장소의 소유자 또는 관리자에 의해 확인되고 반영됩니다.  따라서 원래 저장소 주인에게 pull request로 기여하지 않는 이상 단순 commit 으로는 contribution이 인정되지 않는다.<br>즉, 주인이 따로 있는 저장소는 주인이 인정해주지 않는 이상 contribution으로 반영되지 않는다..

​



<br>

### 3️⃣  Solution

---

#### 1. Github에 새로운 저장소 생성

#### 2. Local(내 컴퓨터)에 기존저장소(Fork 때문에 잔디심기가 안됐던)를 bare clone 진행

~~~ bash
git clone --bare 기존저장소.git
~~~
- ##### "Bare clone(베어 클론)"은 Git 저장소를 복제할 때 일반적인 클론과는 다르게 저장소의 모든 내용을 복제하지만 작업 디렉토리(working directory)를 생성하지 않는 것을 말합니다. 따라서 베어 클론을 실행하면 저장소의 모든 파일과 히스토리가 복제되지만, 실제 파일들이 저장되는 작업 디렉토리는 생성되지 않습니다.

#### 3. 새롭게 생성한 저장소로 mirror push 진행

~~~bash 
git push --mirror 새롭게 생성한 저장소.git
~~~

#### 4. Local(내 컴퓨터)에 생성했던 기존저장소 삭제

```bash
cd .. rm -rf old-repository
``` 

- ##### "Mirror push(미러 푸시)"는 Git 저장소를 완전한 미러 형태로 복제하는 작업을 의미합니다. 이 작업은 저장소의 모든 커밋, 브랜치, 태그 등을 완벽하게 복제하여 다른 원격 저장소에 반영하는 것을 말합니다.


#### **몇 분 지나면 profile에서 기존의 Contribution까지도 가 심어진 것이 보인다 !** (참고 블로그 작성자님에 따르면.. 나는 계속 에러가 떠서 무대포 아래 방법으로 이전 커밋은 포기하고, 이후 contribution이라도 반영되도록 해결했다..)

​
>위 작업에서 에러가 뜨거나 귀찮다면..? 이전 변경에 대한 Contribution은 포기해야함..

##### 1. 새로운 저장소 생성

#### 2. fork한 저장소 안에 모든 내용을 새로운 저장소에 복붙 업로드 

#### 3. fork한 저장소 삭제 및 새로운 저장소 commit & push
<br>

### 4️⃣  References

---
[Fork한 저장소에 잔디가 안 심어질 때](https://yanghojun.github.io/LayTheForkedGarden/)<br>
[github 잔디밭 안 심어지는 현상 해결 및 이미 커밋한 내용 반영하기](https://wellbell.tistory.com/43)
<br>
