# UltimateShiftController — Windows controller/input remapper (HidHide / ViGEmBus / virtual DS4/X360)

- English guide: [README_en.md](README_en.md)　New:2026/03/24 [Instructions](Instructions_en.md)
- Japanese guide: [README_JP.md](README_JP.md)  New:2026/03/24 [説明書](Instructions_jp.md)


https://www.youtube.com/watch?v=xKO9DV92bWc


![Normal mapping example](/USC.png)

# Ultimate Shift Controller

## About

### JP
Ultimate Shift Controller は、

https://github.com/Lu-ci-el/HyperShiftController

↑若干違うけど説明書　超絶バージョンアップしてるので・・・少し違うけどね！

HyperShift の仕組みを作っているうちに⋯
「これ、全部自分で作れば Ultimate Shift になるのでは？」  
と思ったのがきっかけで生まれました。

キー入力を自由に扱える環境を取り戻すために作った、  
個人開発のツールです。

ちなみにまだ **BETA** です。  
たぶんバグもあります。  
まあそのうち直す……と思います……。

ってのは2026年の3月までさ

もう大体できてる

たまにバグが見つかるので更新するで

xbox oneのコントローラー使ってる人で
仮想コントローラーを使う場合は

以下を試してね

コントローラーが認識されない場合は、Ultimate Shift Controller を「管理者として実行」してみてください。
仮想コントローラー、HidHide、他のリマップツールが入っている環境では、管理者権限での実行が必要になる場合があります。

If your controller is not detected, try running Ultimate Shift Controller as Administrator.
Some environments may require elevated permissions, especially when virtual controller drivers, HidHide, or other remapping tools are installed.

![Normal mapping example](/usc_256x256.png)

### EN
Ultimate Shift Controller was born from a simple thought:

While recreating HyperShift-style behavior,  
I realized — if I build everything myself, it becomes an Ultimate Shift.

This is a personal tool made to regain full control over key input.
---

## Support

もしこのツールが少しでも役に立ったと感じたら、  
お布施という形での支援も歓迎しています。

- Ofuse: https://ofuse.me/lost  
- Ko-fi: https://ko-fi.com/lost2

もちろん、使ってもらえるだけでも嬉しいです。
全然広まらないので・・・便利だったら広めて見てください。

# 仮想コントローラーを使用する場合の重要な注意

仮想コントローラーを使用する場合は、USCのHidHide設定でゲームから隠す物理コントローラーを選択し、HidHideを有効にしてください。

物理コントローラーを選択しただけでは非表示になりません。必ずHidHideを有効にする必要があります。

HidHideが無効のままだと、ゲームへ物理コントローラーとUSCの仮想コントローラーの両方から入力が送られ、ボタンが二重に反応する場合があります。

設定後は、USCの押下ボタン表示を確認してください。

コントローラーのボタンを1回押したときに、対応するボタン入力が1つだけ表示されることを確認してください。1回の押下で同じ入力が2つ表示される場合は、物理コントローラーが正しく隠されていない可能性があります。

ゲーム側で使用するコントローラーには、USCが作成した仮想コントローラーの「Wireless Controller」を選択してください。


# Important notice when using a virtual controller

When using a virtual controller, select the physical controller that should be hidden from games in USC’s HidHide settings, and then enable HidHide.

Selecting the physical controller alone does not hide it. HidHide must also be enabled.

If HidHide remains disabled, the game may receive input from both the physical controller and USC’s virtual controller, causing buttons to respond twice.

After applying the settings, check USC’s pressed-button display.

Press a controller button once and confirm that only one corresponding button input appears. If the same input appears twice from a single press, the physical controller may not be hidden correctly.

In the game’s controller settings, select **Wireless Controller**, which is the virtual controller created by USC.
