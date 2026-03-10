# 설명
`대상이 1인칭에서 렌더링되고 있는지 감지한다.`
```
bool ishand(mat4 projMat) {
    return abs(projMat[3][2] + 0.10005) < 0.00001;
}
```