# OpenCV_aar

## 打包aar流程
1.import model 官方openCV sdk
2.Gradle Task assemble
3.從build資料夾複製打包好的aar
注意是否缺少OpenCV Manager so檔

### 匯入aar
將aar檔放置專案\app\libs下
```gradle
android {
    repositories {
        flatDir {
            dirs 'libs'
        }
    }
}

dependencies {
       implementation(name: 'opencv-release', ext: 'aar')
 }
```