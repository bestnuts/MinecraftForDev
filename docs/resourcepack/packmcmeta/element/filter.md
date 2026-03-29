# 설명
팩의 특정 경로를 제한하기 위해 필요합니다.  

# 포맷
```
filter : 필터
    block : 리스트로 담아둘 수 있습니다.
        namespace : 기본적으로 minecraft 를 네임스페이스로 사용합니다.
        path : 네임스페이스 위 경로입니다.
```

# 예시
`블록 텍스쳐 제한`
```
{
  "filter": {
    "block": [
      {
        "namespace": "minecraft",
        "path": "textures/block"
      }
    ]
  }
}
```