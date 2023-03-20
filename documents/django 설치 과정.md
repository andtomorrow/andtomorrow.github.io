# django 설치 과정
#web Mar 20, 2023 1:44 PM

## 1. 가상환경 설정
### 1-1. 생성
```shell
$ python -m venv venv
```
### 1-2. 활성화
```shell
$ source venv/bin/activate
```
	* VSCode의 경우 cmd palette 에서 interpreter 설정으로 지정하면 됨

## 2. django 설치
### 2-1. LTS 버전으로 설치 (현재 기준 3.2.18)
```shell
$ pip install django==3.2.18
```
### 2-2. 의존성 파일 생성
```shell
$ pip freeze > requirements.txt
```

## 3. 프로젝트 시작
### 3-1. 프로젝트 생성
```shell
$ django-admin startproject PROJECT_NAME .
```
### 3-2. 서버 실행, URL 접속
```shell
$ python manage.py runserver
```

## 4. git
### 4-1. `.gitignore`부터 작성
### 4-2. `git init`
```shell
$ git init
$ git remote add origin REMOTE_GIT
```