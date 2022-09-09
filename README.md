## 로컬에서 https띄우기
```javascript
// cmd에서 입력
npm install -g mkcert

// ca 생성
mkcert create-ca

// cert 생성
mkcert create-cert

npm i https, fs
```
import 하고 

```javascript
const options = {
  key: fs.readFileSync('./src/config/cert.key'),
  cert: fs.readFileSync('./src/config/cert.crt'),
};

https.createServer(options, app).listen(8000, () => {
  console.log('s mean success');
});
```

options 설정 이후 https createServer 로 https 8000포트로 발사
