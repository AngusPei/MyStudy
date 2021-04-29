# Button知识点

## 构造Button按钮

```dart
                OutlinedButton(
                      onPressed: () => NavigatorUtils.goBack(context),
                      style: OutlinedButton.styleFrom(
                        primary: Theme.of(context).accentColor,
                        minimumSize: const Size(90, 40),
                        padding: EdgeInsets.symmetric(horizontal: 16),
                        shape: const RoundedRectangleBorder(
                          borderRadius: BorderRadius.all(Radius.circular(22)),
                        ),
                      ).copyWith(
                        side: MaterialStateProperty.resolveWith<BorderSide>(
                          (Set<MaterialState> states) {
                            /// 状态为按下时则显示主题色线框
                            if (states.contains(MaterialState.pressed)) {
                              return BorderSide(
                                color: Theme.of(context).primaryColor,
                                width: 1,
                              );
                            } else {
                              return BorderSide(
                                  color: Color(0xFFCFCFCF), width: 1);
                            }
                          },
                        ),
                      ),
                      child: Text(
                        '取消',
                        style:
                            TextStyles.textSize16.copyWith(color: Colors.black),
                      )),
                  Padding(
                    padding: const EdgeInsets.only(left: 35),
                    child: TextButton(
                        onPressed: okPressed,
                        style: ElevatedButton.styleFrom(
                          primary: Theme.of(context).primaryColor,
                          minimumSize: const Size(90, 40),
                          padding: EdgeInsets.symmetric(horizontal: 16),
                          shape: const RoundedRectangleBorder(
                            borderRadius: BorderRadius.all(Radius.circular(22)),
                          ),
                        ),
                        child: Text(
                          '确定',
                          style: TextStyles.textSize16
                              .copyWith(color: Colors.white),
                        )),
                  ),
```
