# 설명
namespace 와 path 를 이용해 원하는 파일을 효과적으로 불러옵니다.  

# 포맷
```
namespace : 에셋 위 폴더명
path : 네임스페이스 위 경로
```

# 팁
namespace 에 minecraft 는 생략 가능하며 생략시 무조건 minecraft 로 불러오려 합니다.  

# 예시
`유니코드 폰트 예시`
```
tellraw @s {text:"텍스트",font:"minecraft:uniform"}
```