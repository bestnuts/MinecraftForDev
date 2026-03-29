# 설명
언어를 정의할 수 있습니다.  

# 포맷
```
language : 언어
  code : assets/<namespace>/lang/<language>.json
    name : 언어명
    region : 지역명
    bidirectional : 참일시 우측에서 좌측으로 읽는다. 
```

# 예시
```
{
  "language": {
    "ko_kr": {
      "name": "한국어",
      "region": "대한민국",
      "bidirectional": false
    }
  }
}
```