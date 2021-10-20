## axios에 대하여

#### Axios는 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신 라이브러리이다

---

1. 요청 객체에 url이 있다
2. 써드파티 라이브러리로 설치가 필요
3. **XSRF** 보호를 해준다
4. **data** 속성을 사용
5. **data**는 **object**를 포함한다
6. **status**가 200이고 **statusText**가 '**OK**'이면 성공이다
7. 자동으로 **JSON** 데이터 형식으로 변환된다
8. 요청을 취소할 수 있고 타임아웃을 걸 수 있다
9. **HTTP** 요청을 가로챌 수 있다
10. **download** 진행에 대해 기본적인 지원을 한다
11. 좀 더 많은 브라우저에 지원된다

**별도의 설치가 필요하다는 단점**이 있지만 그것을 커버할 만한 fetch보다

**많은 기능 지원과 문법이 조금이나마 간소화 된다는 장점**이 있다

---

#### 설치 방법

- CDN 방식

```html
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

- NPM 방식

```bash
npm install axios
```

---

#### axios 응답 제어

- **.then** - 비동기 통신이 성공했을 경우, 콜백을 인자로 받아 결괏값을 처리 가능
- **.catch** - 오류를 처리 [<error>객체에서는 오류에 대한 주요 정보를 확인]

---

**axios.get(url[, config])** - 서버에서 데이터를 가져올 때 사용하는 메서드

**axios.post(url[, data[, config]])** - 서버에 데이터를 새로 생성할 때 사용하는 메서드

**axios.put(url[, data[, config]])** - 특정 데이터를 수정할 때 요청하는 메서드

**axios.delete(url[, config]])** - 특정 데이터나 값을 삭제할 때 요청하는 메서드

---

#### axios HTTP 요청 Config 옵션

- **method** - 요청을 할 때 사용할 요청 메서드<기본값은 get>
- **url** - axios 요청에 사용될 서버의 URL
- **baseURL** - 액시오스 인스턴스를 생성할 때, 인스턴스의 기본 URL 값을 정할 수 있는 속성
- **headers** - 헤더를 수정해서 보내야 할 때 사용
- **params** - HTTP요청에 붙일 URL파라미터를 의미
- **data** - HTTP요청 보디에 실어서 보낼 데이터를 의미<PUT, POST, DELETE, PATCH 등의 메서드에서 사용>
- **timeout** - HTTP요청을 보내고 응답을 받기까지의 제한 시간을 설정하는 속성<요청 시간이 지정된 값을 초과하면 에러 발생>
- **responseType** - 서버로부터 어떠한 데이터 형식으로 응답받을지 지정하는 것<옵션으로는 arraybuffer, document, json, text, stream이 가능, 기본값은 json>
