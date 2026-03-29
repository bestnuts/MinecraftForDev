# 설명
팩의 버전을 정의할 수 있습니다.  
일부가 필수로 있어야 하는 항목입니다.  
최소 최대 혹은 지원할 메이저 버전을 정의합니다.  

# 포맷
```
pack_format : 팩의 메인 포맷입니다.
supported_formats : 지원하는 버전 구간입니다.
min_format : 지원하는 최소 버전입니다.
max_format : 지원하는 최대 버전입니다.
```

# 팁
format 을 지정할때 단일 정수 84 는 [84] [84, 0] 과 동등합니다.  
min_format 의 경우 첫 번째 정수는 메이저 두 번째 정수는 마이너입니다.  
max_format 의 경우 정수 하나를 지정하면 모든 마이너 버전으로 지정됩니다.  

# 예시
`1.21.11 지원`
```
{
  "pack": {
    "pack_format": 75,
    "supported_formats": [
      9,
      75
    ],
    "min_format": 9,
    "max_format": 75
  }
}
```