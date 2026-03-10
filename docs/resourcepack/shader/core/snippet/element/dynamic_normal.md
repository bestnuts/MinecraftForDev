# 설명
`고정된 물체에 표면 밝기를 계산합니다.`
```
vec3 normal = mat3(ModelViewMat) * Normal;
vertexColor = minecraft_mix_light(Light0_Direction, Light1_Direction, normal, Color) * texelFetch(Sampler2, UV2 / 16, 0);
```
`프래그먼트에서 가능한 방법이지만 버전에 따라 그리고 유의미한 픽셀 손실이 있을 수 있습니다.`
```
vec3 getNormal(vec3 worldPos) {
    vec3 dx = dFdx(worldPos);
    vec3 dy = dFdy(worldPos);
    return normalize(cross(dx, dy));
}
```