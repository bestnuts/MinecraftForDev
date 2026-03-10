# 설명
`시야각을 수정합니다.`
```
#define FOV 60.0
const float invTanHF = 1.0 / tan(radians(FOV / 2.0));
mat4 changeFov(mat4 projection) {
    if (projection[2][3] != 0.0) {
        float aspectInv = projection[0][0] / projection[1][1];
        projection[0][0] = invTanHF * aspectInv;
        projection[1][1] = invTanHF;
    }
    return projection;
}
```