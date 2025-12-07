# 설명
`화면 흔들림을 제거합니다.`
```
mat4 projMat = ProjMat;
projMat[3].xy = vec2(0.0);
```