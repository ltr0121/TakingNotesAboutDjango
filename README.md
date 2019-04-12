# TakingNotesAboutDjango
-------
## Step 1. 작업 디렉토리 만들기
### 폴더 생성 
```bash
$ mkdir likelion7
``` 
### 폴더 이동
```bash
$ cd likelion7
``` 
### visual studio code로 열기 
```bash
$ code .
``` 
-------
## Step 2. 가상 환경 생성 & 장고 설치
### 가상 환경 생성
*프로젝트나 앱이 아닌 폴더 안에 만들기*
```bash
$ python -m venv myvenv
``` 
### 가상 환경 실행 
*Django 개발 시 가상 환경 반드시 켜기*
*프로젝트나 앱이 아닌 폴더 안에서 켜기*
```bash
$ source myvenv/Scripts/activate
``` 
### 가상 환경 끄기 
```bash
$ deactivate
``` 
### django 설치하기
```bash
$ pip install django
``` 
-----------
## Step 3. 프로젝트 생성
### 프로젝트 생성하기
```bash
$ django-admin startproject project_name
``` 
---------
## Step 4. app 만들기
### app 만들기
```bash
$ python manage.py startapp myapp
``` 
### settings.py에 app 선언
```python
INSTALLED_APPS=[
'myapp.apps.MyappConfig',
]
``` 
### 서버 켜기
```bash
$ python manage.py runserver
``` 
### templates 만들기
1. App 폴더 안에 templates 폴더 만들기
1. templates 폴더 안에 `home.html` 만들기
### views.py에 함수 만들기
```python
def home(request):
  return render(request, 'home.html')
``` 
### urls.py 작성하기
```python
import myapp.views

urlpatterns = [
  path('', myapp.views.home, name='home')
 ]
``` 
