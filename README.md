# ChangeAppIcon
Change the App Icon

## 在项目中动态替换AppIcon，并使用RunTime去除更改成功后的提示框（Pass：更改后的提示框实在太丑了！）

![示例gif](https://github.com/GlassOfRedWinemm/ChangeAppIcon/blob/master/ChangeAppIcon/ChangeAppIcon/ChangeAppIcon.gif)

1、新建`Objective-C`项目

2、右键`Info.plist->Open As->Source Code`,复制一下代码放入：

```
    <key>CFBundleIcons</key>
    <dict>
        <key>CFBundleAlternateIcons</key>
        <dict>
            <key>boy.jpg</key>
            <dict>
                <key>CFBundleIconFiles</key>
                <array>
                    <string>boy.jpg</string>
                </array>
                <key>UIPrerenderedIcon</key>
                <false/>
            </dict>
            <key>girl.jpg</key>
            <dict>
                <key>CFBundleIconFiles</key>
                <array>
                    <string>girl.jpg</string>
                </array>
                <key>UIPrerenderedIcon</key>
                <false/>
            </dict>
        </dict>
        <key>CFBundlePrimaryIcon</key>
        <dict>
            <key>CFBundleIconFiles</key>
            <array>
                <string>boy.jpg</string>
            </array>
            <key>UIPrerenderedIcon</key>
            <false/>
        </dict>
        <key>UINewsstandIcon</key>
        <dict>
            <key>CFBundleIconFiles</key>
            <array>
                <string></string>
            </array>
            <key>UINewsstandBindingEdge</key>
            <string>UINewsstandBindingEdgeLeft</string>
            <key>UINewsstandBindingType</key>
            <string>UINewsstandBindingTypeMagazine</string>
        </dict>
    </dict>

```
3、在`ViewController.m`实现中实现代码即可，为避免提示框显示，使用RunTime去除提示框，说的只是一个思路，具体参考代码


