# HelloNew（android-new）

一个标准的 **Android 原生应用**（Kotlin + Gradle），使用**公开密钥**签名，包名唯一。

## 关键信息

| 项 | 值 |
|----|----|
| 包名（唯一） | **`com.changwenting.hellonew`** |
| compileSdk / targetSdk | 35（Android 15） |
| minSdk | 24（Android 7.0） |
| 签名 | 公开密钥 `app/public.keystore`（密码 `public123`，随仓库提供） |

> 包名与其它工程（`com.example.secureapp`、`com.example.secureapp.public`）均不同，可在同一设备共存。

## 运行与打包

Android Studio 直接 Open 本目录；命令行：

```bash
./gradlew assembleDebug     # Debug APK
./gradlew assembleRelease   # 已用公开密钥签名的 Release APK，可直接安装
```

## 关于公开密钥

`public.keystore` 的密码与别名全部公开，任何人都能复现签名，**安全性等同 debug 包，不能用于上架**。

## 许可证

MIT
