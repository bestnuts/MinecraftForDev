# 설명
`플레이어 화면 기준 방향 벡터`
```
vec4 ndcPos = vec4(gl_FragCoord.xy / ScreenSize * 2.0 - 1.0, 0.0, 1.0);
vec4 temp = inverse(ProjMat) * ndcPos;
vec3 viewPos = temp.xyz / temp.w;
vec3 playerPos = viewPos * mat3(ModelViewMat);
vec3 rayDir = normalize(playerPos);
```