# dj# Django

---

장고는 관리자 페이지가 구현이 되있기에 만들 필요 없음

### MVC / MTV 패턴

M → Model

T → Template

V → View

![image](https://user-images.githubusercontent.com/87698248/186065457-75314fe0-fa7c-4a25-9d32-4a9e8b83a112.png)

![image](https://user-images.githubusercontent.com/87698248/186065484-91311adb-a644-4fe8-8b8b-bcba27bf3add.png)

SQLlite → 장고 실치시 같이 깔림

SQLlite 사용 해도됨 대신 db설계를 파일로함

db를 db로 설계하는것이아닌, python으로 설계함 그후 내보냄

장고 3버젼

sqllite 버전 or mysql 버전

---

### Django 설치

서버는 자체 서버가 있기에 필요 없음

cmd → pip install django

![image](https://user-images.githubusercontent.com/87698248/186065501-961ab243-a420-4e1d-88b3-6879187efb56.png)

pip -m django - - version

---

### 프로젝트 생성

- file → new → other → pydev
    
    ![image](https://user-images.githubusercontent.com/87698248/186065525-da32dcf5-0a83-401b-82d9-83cdda6db433.png)
    

- 이상태로 두고 next
    
    ![image](https://user-images.githubusercontent.com/87698248/186065542-d88b73a2-3d1c-49ce-aae8-dc3e5a088deb.png)
    

- next
    
    ![image](https://user-images.githubusercontent.com/87698248/186065563-205e3fec-78df-4d7e-8452-38ecf7bf2f04.png)
    

- next
    
    ![image](https://user-images.githubusercontent.com/87698248/186065581-c14856a5-ab2a-43fc-9639-dabecdd26d0c.png)
    
    C:\AI\Workspace\DjangoEx\sqlite.db → 파일이 생성됨 그대로 쓸 예정
    

![image](https://user-images.githubusercontent.com/87698248/186065604-ba166fac-850c-470b-801c-7931bb6bb0ff.png)

[manage.py](http://manage.py) 에서 모든 세팅을 함

### 파일구조

- [manage.py](http://manage.py) → 프로젝트와 다양한 방법으로 상호작용 하는 커맨드라인 유틸리티
- [urls.py](http://urls.py) → 앱의 url 패턴 선언 사이트의 목차같은 개념
- [setting.py](http://setting.py) → 프로젝트의 환경 및 구성을 저장하는 공간
- [asgi.py](http://asgi.py) → 현재 ASGI-프로젝트를 서비스하기위한 웹 서버의 진입점
- [wsgi.py](http://wsgi.py) → 현재 WSGI-프로젝트를 서비스하기위한 웹 서버의 진입점

---

- db 세팅
    
    ![image](https://user-images.githubusercontent.com/87698248/186065630-c9f598a6-f538-4cc2-915c-ab2b78cb9e15.png)
    

db가 없기에 db를 생성해주어야함

모두 docs 에서 해주어야함

C:\AI\Workspace\DjangoEx → manage.py

![image](https://user-images.githubusercontent.com/87698248/186065647-eaa344dd-332e-4c15-bc44-1adb2355269a.png)

![image](https://user-images.githubusercontent.com/87698248/186065657-d061c79a-0a87-4438-b9df-b33a14e3cc56.png)

모든 설정은 manage.py로 할것임

잘알아 두어야함

관리자는 이미 만들어져있기에 계정만 만들면됨


- python [manage.py](http://manage.py) migrate
    
    ![image](https://user-images.githubusercontent.com/87698248/186073891-46f1f31a-343a-4d16-a50c-fbcf07095f40.png)
    
    ![image](https://user-images.githubusercontent.com/87698248/186073903-0d64fdcc-a076-4d8b-b970-bd388ac1b184.png)
    
    디비 생성 완료
    
    관리자는 페이지가 있음
    
    관리자는 쓸 수 있는데 암호를 만들어주어야함
    
    관리자는 웹 프로젝트의 대한 관리자임
    

- 관리자 계정 생성
    - python [manage.py](http://manage.py) createsuperuser
        - username : admin
        - email :
        - passwd : admin1234
        - repasswd : admin1234
        - y
    
    ![image](https://user-images.githubusercontent.com/87698248/186073925-50928eeb-d626-42a7-8e8a-25023507a05d.png)
    

바뀐 내용이 있을경우

1. python [manage.py](http://manage.py/) makemigrations
2. python [manage.py](http://manage.py/) migrate

로 변경을 해주면됨

- 장고 서버 시작
    
    python [manage.py](http://manage.py) runserver
    
    ![image](https://user-images.githubusercontent.com/87698248/186073940-f5a220ad-0ba7-49af-894a-6c5f058bbd11.png)
    
    ![image](https://user-images.githubusercontent.com/87698248/186073959-4327fc49-0f0b-467d-ae1f-aff0661b44fb.png)
    

장고 서버가 동작을함

cmd 창은 항상 켜져있어야함

- localhost:8000/admin
- 관리자 페이지 이동
    
    ![image](https://user-images.githubusercontent.com/87698248/186073985-a649d2f2-d8f6-4bf8-842f-a0b44bc12ff1.png)
    
    ![image](https://user-images.githubusercontent.com/87698248/186074007-c82792ec-a61d-4f68-a688-ea8a13e7ec1c.png)
    
### 어플리케이션 생성

- cmd → python [manage.py](http://manage.py/) startapp bookmark
    
    ![image](https://user-images.githubusercontent.com/87698248/186075429-65a1cfe0-6473-4bf2-a187-6554d90abc44.png)
    
    ![image](https://user-images.githubusercontent.com/87698248/186075443-41d0134b-0c6c-4307-8766-07c848a35386.png)
    
    생성 완료
    
전체 새팅을 걸어줌

- DjangoEx → [setting.py](http://setting.py) 기본 세팅값
    
    ```python
    # Application definition
    # 현재 설치되어있는 앱이 무엇인지
    INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        'bookmark', # 새로 추가해줌
    ]
    
    ----------------------
    
    LANGUAGE_CODE = 'ko-kr' # 한국어
    
    TIME_ZONE = 'Asia/Seoul' # 한국시간
    
    USE_I18N = True
    
    USE_TZ = True
    
    ------------------------
    # 디비를 다른것을 쓸거면 mysql로 변경해줌
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.sqlite3',
            'NAME': BASE_DIR / 'db.sqlite3',
        }
    }
    ```
    

새팅이 바뀌었기에 서버를 재시작 해주어야함

- 한국어 변경 확인
    
    ![image](https://user-images.githubusercontent.com/87698248/186074028-5869a0c2-9006-465b-8409-dadf14b22899.png)
    

기본 세팅 종료
