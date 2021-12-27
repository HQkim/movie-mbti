# README(SSAFY)

진행상황: In progress

# 🎞 MOVIE 추천 PROJECT

---

### 프로젝트 목표

- 영화 정보 기반 추천 서비스 구성
- User MBTI 정보 기반 영화 추천 서비스
- 커뮤니티 게시판 서비스 구성
- Django, REST API, DataBase, HTML, CSS, JavaScript, Vue.js  등을 활용한 실제 서비스 설계
- 서비스 관리 및 유지 보수

### 개발 환경

- 언어
  
    Python, JavaScript
    
- 프레임워크
  
    Django, Vue.js
    
- 아키텍쳐
  
    Django REST API 서버 & Vue.js
    

---

## 1. 팀원 정보 및 업무 분담 내역

### 1-a. 김현규 (본인)

- Backend
- DRF사용 RESTful API 서버 로직 구현
- 기획 및 디자인

### 1-b. 장보일

- Frontend
- Vue 클라이언트 구현
- 기획 및 디자인

---

## 2. 목표 서비스 구현 및 실제 구현정도

### 2-a. 목표 서비스

1. 영화 조회 서비스 
    - 추천영화 목록 (장르별)

1. 상세 영화 정보 서비스 
    - 유저 영화 평점 및  댓글 입력 기능

1. MBTI 별 추천 영화 서비스
    - MBTI 별 많은 댓글이 달린 영화 순서로 목록 조회 기능
    - 영화 검색 기능
    
2. 프로필 제공 서비스 
    - 나의 MBTI조회
    - 받은 좋아요 개수
    - 내가 쓴 게시글 수
    
3. 회원 정보 수정 서비스
    - ID 및 비밀번호  수정
    - MBTI 정보 수정
    
4. 게시판 서비스 
    - 게시글 상세 조회
    - 게시글 댓글 및 좋아요 기능
    

### 2-b. 실제 구현 서비스

1. 영화 조회 서비스 
    - 추천영화 목록 (장르별)
1. 상세 영화 정보 서비스 
    - 유저 영화 평점 및  댓글 입력 기능
1. MBTI 별 추천 영화 서비스
    - MBTI 별 많은 댓글이 달린 영화 순서로 목록 조회 기능
2. 프로필 제공 서비스 
    - 나의 MBTI조회
    - 받은 좋아요 개수
    - 내가 쓴 게시글 
5. 게시판 서비스
    - 게시글 상세 조회
    - 게시글 댓글 및 좋아요 기능


### 2-c. 추후 구현할 서비스

1. MBTI 추천 영화 서비스
    - 활동 정도(댓글, 게시글, 게시글 좋아요 받은것 등)에 따른 영화 랭킹 추천 서비스
    
 2.  게시글 작성 서비스 

- 유저 사진 업로드 기능

 3.  프로필 서비스

- 유저간 팔로우 및 팔로잉 기능

4. MBTI 검사 기능 서비스

- MBTI 설문검사를 진행 할 수 있는 페이지 작성

5. 회원정보 수정 서비스

- ID 및 비밀번호  수정
- MBTI 정보 수정

## 3. 데이터베이스 모델링(ERD)

![ERD.png](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/ERD.png)

## 4. 필수 기능

### 회원가입

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled.png)

- 위와 같이 Modal을 통해서 회원가입을 진행

### 로그인 / 로그아웃

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%201.png)

- Modal을 통해서 로그인 진행
- JWT 토큰 인증 사용

### 영화 장르에 다른 디스플레이

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%202.png)

- 장르 값을 Vue의 props를 통해 하위 component들에 전달해 주면 이에 해당하는 영화들만 보이도록 설

### 영화 상세 페이지 및 댓글

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%203.png)

- 영화 제목, 줄거리, 평점 정보를 보여줌
- 영화에 대한 코멘트를 평점과 함께 작성하고 이에 대한 삭제를 할 수 있음

### MBTI 추천영화 페이지

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%204.png)

- MBTI 타입 Vue props를 통해서 하위 component들에 전달해주면 이에 해당하는 영화들만 보이게끔 지정

### 게시판

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%205.png)

- 게시판에 글을 불러올 때, 게시글을 쓴 유저의 usernam, mbti, 작성일자를 보여줌
- 게시판에 달린 코멘트의 개수도 출력

### 게시글 작성

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%206.png)

- 게시글 제목, 영화 제목, 내용 및 MBTI 타입을 넣어서 게시글을 작성

### 게시글 상세 페이지 댓글 기능

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%207.png)

- 게시글의 제목, 영화 제목, 내용이 보여짐
- 게시글에 대한 댓글을 생성하고 삭제할수 있음

### 게시글 수정 및 삭제

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%208.png)

- 게시글 제목, 영화 제목, 내용 및 MBTI 타입을 넣어서 게시글을 수정할 수 있음

### 프로필

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%209.png)

- 유저의 MBTI, 게시글 좋아요 받은 개수, 쓴 개시글의 수를 표현

### 탑메뉴(로그인 버튼)와 네브바(햄버거 버튼) 구현

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2010.png)

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2011.png)

- 탑메뉴: 가장 최상단에 로그인이 되어 있으면 프로필/로그아웃 버튼을, 로그인이 안되어 있으면 로그인/회원가입 버튼을 보여줌
- 네브바: 창의 크기가 줄어들면 네브바가 햄버거 버튼의 드롭다운 방식으로 바뀌도록 설정

## 5. 진행 중 오류와 배운점

### 5-1. save() missing 1 required positional argument 'self' 오류

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2012.png)

![error_1119_1.png](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/error_1119_1.png)

- 처음에 어디서 오류가 났는지 계속 고민하다가 해결하지 못함
- 다시 한 번 확인을 해보니 Article이 아니라 article인자를 전달 해야함
- 사소한 부분에서 실수가 자칫 큰 오류를 일으킬 수 있다는 사실을 배울 수 있었다.

### 5-2.  모델 관계(1:N, N:M)에서 related_name의 관련 오류

```python
# movies/models.py
class Comment(models.Model):
    RANK_CHOICES = [
        (1, '1'),
        (2, '2'),
        (3, '3'),
        (4, '4'),
        (5, '5'),
        (6, '6'),
        (7, '7'),
        (8, '8'),
        (9, '9'),
        (10, '10'),
    ]    
    content = models.TextField()
    movie = models.ForeignKey(Movie, on_delete=models.CASCADE, related_name='comments')
    user = models.ForeignKey(settings.AUTH_USER_MODEL, on_delete=models.CASCADE, related_name="user_movie_comments")
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)
    rank = models.PositiveIntegerField(choices=RANK_CHOICES, default=5)

    def __str__(self):
        return f'{self.content}'
```

```python
# movies/serializers.py
class MovieSerializer(serializers.ModelSerializer):

    class CommentSerializer(serializers.ModelSerializer):
        class Meta:
            model = Comment
            fields = ('id', 'content', 'updated_at', 'rank',)

    comments = CommentSerializer(many=True, read_only=True)
    class Meta:
        model = Movie
        fields = ('id', 'title', 'release_date', 'vote_count', 
        'popularity', 'vote_average', 'overview', 'poster_path', 'genres', 'comments',)
```

```python
# movies/views.py
@api_view(['GET'])
@permission_classes([AllowAny])
def movie_detail(request, movie_pk):
    movie = get_object_or_404(Movie, pk=movie_pk)
    serializer = MovieSerializer(movie)
    return Response(serializer.data)
```

- model에서 1:N관계에서 related_name을 설정 안해줬을 때 위의 serializer와 같이 설정하고 views.py를 불러오는 url로 Get요청을 했을 때 comments data가 오지 않는 오류가 발생
- 어던 부분에서 에러가 발생한 것인지 고민하다가 model의 related_name과 serializer의 "comments"를 똑같이 설정해 주어야 오류가 발생하지 않고 data를 받을 수 있다는 사실을 알게 되었다.

### 5-3. 댓글 Create 과정에서 오류 발생

```python
@api_view(['POST'])
def comment_create(request):
    print(request.data.get("movie_id"))
    serializer = CommentSerializer(data=request.data)
    print(serializer)
    if serializer.is_valid(raise_exception=True):
        serializer.save(user=request.user, movie_id=request.data.get("movie_id"))
        return Response(serializer.data, status=status.HTTP_201_CREATED)
```

1. 에러 발생
   
    `django.db.utils.IntegrityError: NOT NULL constraint failed: movies_comment.movie_id`
    
2. 처음 프론트에서 데이터를 잘못 넣어준 줄 알아서 헤매다가 위처럼 serializer와 request.data를 찍어봤다.
3. 결국 movie_id는 data=request.data일때는 ReadOnly여서 들어가지 않고 user처럼 [serializer.save](http://serializer.save) 할 때 넣어 줬어야 했다.
4. 근데 여기서 또 request.data.movie_id로 넣어줬는데 안들어가서 request.data.get으로만 불러올 수 있다고함. request.data.movie_id로 접근하니 다음과 같은 에러 발생 `AttributeError: 'QueryDict' object has no attribute 'movie_id'`
5. 즉  다시 말해movie = request.data.get("movie_id")로 넣으니 안되고  위의 사진과  같이 movie_id로 넣어줘야 잘 작동한다.

### 5-4. CORS 관련 오류 발생

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2013.png)

- 브라우저의 CORS 정책에 의한 오류가 발생함
- 요청한 리소스에 Access-Control-Allow-Orgin 헤더가 없기 때문에 차단된 것 (기본적으로 SOP-Same-Origin Policy를 준수하기 떄문)
- 따라서 서측에서 해당 설정을 진행해 주었다. 장고에서 제공하는 APP을 통해 문제를 해결한다.
    1. pip install django-cors-headers 설치후 settings.py에 등록 및 MIDDLEWARE에 추가. 
    2. CORS_ALLOWALL_ORIGINS을 TRUE 값으로 설정
    3. 다음과 같이 Response Headers를 확인하여 * 모양 확인!

이번 오류에서도 위와같은 시도를 통해 문제를 해결할 수 있었다.

 

### 5-5. movie index 페이지를 제외한 페이지에서 새로고침시에 레이아웃 스타일링이 깨지는 현상 발생

(**새로고침 전)**

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2014.png)

**(새로고침 후)**

![Untitled](README(SSAFY)%20939ecad928b3467f99f33b1f6e7c7e62/Untitled%2015.png)

**에러 원인**

- 기존에 템플릿의 css와 js파일을(bootstrap포함) `public/index.html`에 <link>태그와 <script>태그로 넣어줬었다. 
처음부터 알아보고 하지 않고 감으로 index.html이 처음 불러와지는 페이지니깐 여기에 css와 js파일을 불러오면 모든 페이지에 적용이 되겠지 하고 안일하게 생각했다.
그런데 위와 같이 홈페이지가 아닌 페이지에서 새로고침을 했을 때 폰트와 동작이 모두 적용이 안되는 사태가 발생했다.
- 근본적인 원인은 프로젝트를 시작할 때 더 구체적인 업무 Flow를 기획하지 않고 시작했던 것이 에러의 시작이었던 것 같다. 사용하는 template의 bootstrap 버전이 무엇인지, vue에서 어떻게 사용되어야 하는지에 대한 계획 없이 ppt 슬라이드의 템플릿을 적용하는 것처럼 쉽게만 생각했던 것이 이 에러의 시작이었다.

**해결 및 배운점**

- 위와 같이 index.html에 css와 js를 적용하는 것이 아니라 `src/main.js에` 에 import 해야 한다!! 그리고 bootstrap과 jqeury를 npm을 통해 설치를 해주고 똑같이 import 해주었다. 현재 우리의 template이 bootstrap 4.1.3과 jquery 3.3.1로 되어 있어서 이에 맞추어서 npm으로 설치해 주었다.
  
    (jquery)
    
    `npm install --save jquery@3.3.1` 
    
    `import $ from 'jquery`
    
    (bootstrap)
    
    `npm i --save bootstra@4.1.3`
    
    `import 'bootstrap'`
    `import 'bootstrap/dist/css/bootstrap.min.css'`
    
- 정말 힘들고 슬펐지만, 이 에러 덕분에 많은 것을 알게 되었다.  먼저, vue 에서 새로고침을 하면 props로 부모 컴포넌트에서 내려오던 css가 초기화 된다는 것,(이때 props 데이터는 새로고침시에 초기화 됨) 을 알게 되었다.  또한 bootstrap을 적용하기 위해서 는 다양한 모듈을 import 해야하고 이것들을 손쉽게 관리 하기 위해 scss로 사용한다는 것을 알 수 있었다. (scss는 기회가 주어진다면 추후에 활용을 해보도록 하겠다.)
