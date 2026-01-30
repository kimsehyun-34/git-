# git- 필수 명령어
> 주의사항 : 명령어 중 `<>`괄호로 설명되는 경우 제거후 값 입력

## Git 필수명령어
-------------
> DB에서 가지고옴
 - `git pull` - Global DB에 있는 데이터를 작업영역으로 가지고옴 (merge 해줌)
 - `git clone <URL>` - 원격 DB와 로컬을 연결시킴 (깃헙 주소와 로컬 폴더를 처음 연결시킬 때만 사용)
-------------
> DB에 저장
 - `git add .` - 파일 스테이징에 등록 (작업영역의 자료를 스테이징영역에 저장)
 - `git commit -m "커밋메시지"` - add한 파일을 Local git DB에 저장시킴
 - `git push 깃저장소이름 브런치 이름` - commit한 파일들을 Global git DB(ex:github)에 등록
--------
> 롤백 방법
- `git log` : 커밋 히스토리 확인, 롤백하려는 커밋의 Hash확인
- `git reset --hard <커밋 해시>` : 입력한 포인트로 롤백
--------

## Git 요소
 - Pull requests : 수정된 코드를 보내고 수정을 요청함
 - Merge : 수정하지 않은 코드는 유지, 수정된 코드만 병합 (방식에 따라 종류가 많음)
 - Fork: 다른 Repository에 저장된 파일을 내 Repository로 복사해 오는것(수정할시 상위 저장소에 Pull requests 요청해야함)
   - 상위 사용자의 경우 Pull requests가 올경우 Merge 를 해야 수정이 완료됨
--------

## Git 코드
> 강제 push
```
git add .
git commit -m "<수정내용>"
git push origin main --force
```
--------
> 기존 원격 저장소 제거
```
git remote remove origin
```
> 새 원격 저장소 할당
```
git remote add origin <URL>
```
-------
> 스테이징 캐쉬삭제 (중복 add로 스테이징 영역이 부족할떄)
```
git rm -r --cached .
git add .
```
