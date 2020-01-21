# 크롬 확장 기능 만들기 

### <https://opentutorials.org/module/2503/14051>



#### google chrome extension getting started

```json
// menifest.json

{
  "manifest_version": 2,
 
  "name": "write your app name",
  "description": "write your description",
  "version": "1.0",
 
  "browser_action": {
    // "default_icon": "icon.png",
    "default_popup": "popup.html"
  },
  "permissions": [
    "activeTab"
  ]
}
```

```html
<!-- popup.html -->

<!doctype html>
<html>
    <head>
        
    </head>
    <body>
        <h1>
            app name
        </h1>
    </body>
</html>
```



#### upload extension to chrome

- 크롬 브라우저 상단 우측 메뉴바 클릭 --> 도구 더보기 --> 확장 프로그램
- 우측 상단 개발자 모드 ON --> 압축해제된 확장 프로그램을 로드합니다.(Load unpacked extension...) --> `menifest.json` 이 포함된 디렉토리 업로드



#### JS File 작성 

```javascript
// 컨텐츠 페이지를 대상으로 코드를 실행해주세요.
chrome.tabs.executeScript({
    code: 'write js code you want to execute'
});
```

