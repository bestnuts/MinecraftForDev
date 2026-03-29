# 설명
팩의 다중 버전을 지원하기 위해 필요한 정의입니다.  
버전 포맷을 알아야지 편하게 쓸 수 있습니다.  

# 포맷
```
overlays : 오버레이
    entries : 리스트로 담아둘 수 있습니다.
        directory : pack.mcmeta 가 있는 경로에서 지정
```

# 예시
`1.21.2 지원`
```
{
  "overlays": {
    "entries": [
      {
        "formats": [
          35,
          45
        ],
        "directory": "1_21_2",
        "min_format": 35,
        "max_format": 45
      }
    ]
  }
}
```