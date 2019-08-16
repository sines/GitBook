# 画面效果LUT素材制作流程

目前VRDesign中的画面效果（HDR，宝丽来等）通过后期（PostProcessVolume）完成

![&#x8BBE;&#x7F6E;LUT](../.gitbook/assets/image%20%286%29.png)

## LUT制作流程（参考）

### 1.截取一张VRDesign效果图在PhotoShop中打开

![VRDesign&#x7CBE;&#x54C1;&#x6848;&#x4F8B;&#xFF1A;&#x8F7B;&#x5962;1000&#x5BA2;&#x9910;&#x5385;](../.gitbook/assets/image%20%283%29.png)

### 2.在PhotoShop中选择合适的LUT

#### 1.在PhotoShop工具栏选择 图像-调整-颜色查找

![LUT&#x8BBE;&#x7F6E;](../.gitbook/assets/image.png)

#### 2.选择载入3D LUT

![PS&#x81EA;&#x5E26;&#x7684;LUT&#xFF0C;SoftWarming](../.gitbook/assets/image%20%284%29.png)

### 3.制作UE4使用的LUT纹理

#### 1.在PS中打开RGBTable16x1.jpg

![RGBTable16x1](../.gitbook/assets/image%20%287%29.png)

{% file src="../.gitbook/assets/rgbtable16x1.jpg" %}

#### 2.应用LUT到RGBTable16x1



![&#x5E94;&#x7528;LUT](../.gitbook/assets/image%20%285%29.png)

上图为了**突出对比效果**，应用了不同的LUT，在制作时请保持一致

#### 3.保存应用LUT后的纹理

![&#x4FDD;&#x5B58;&#x540E;&#x7684;LUT](../.gitbook/assets/image%20%289%29.png)

#### 4.在UE4中导入LUT

![&#x5BFC;&#x5165;&#x540E;&#x7684;Texture](../.gitbook/assets/image%20%282%29.png)

#### 5.设置Texture参数

![&#x8BBE;&#x7F6E;&#x53C2;&#x6570;](../.gitbook/assets/image%20%281%29.png)

![&#x4F7F;&#x7528;MoonLight&#x6548;&#x679C;&#x56FE;](../.gitbook/assets/image%20%288%29.png)

