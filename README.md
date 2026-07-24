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

## キャリブレーション時の注意

コントローラーのボタンをレイヤーの起爆キーに設定している場合、そのボタンは通常のボタン入力ではなく、レイヤー切り替え用の起爆キーとして処理されます。

たとえば、レイヤーの起爆キーをL1に設定している場合、ゲーム側のキャリブレーションで元のL1を登録するには、レイヤーのL1起爆キー設定を一時的に解除してください。

NORMALレイヤーでコントローラーの単一ボタンを別の入力へ変換している場合も、元のボタンはそのまま出力されません。

たとえば、NORMALレイヤーでR2を「R2＋○」へ変換している場合、キャリブレーションには通常のR2単体ではなく、設定された複合入力が送られます。

キャリブレーションを行う際は、該当するレイヤーの起爆キー設定を一時的に解除するか、該当するNORMALレイヤーのタブを一時的にOFFにしてください。

キャリブレーション完了後は、元の設定へ戻して使用できます。


# Important notice when using a virtual controller

When using a virtual controller, select the physical controller that should be hidden from games in USC’s HidHide settings, and then enable HidHide.

Selecting the physical controller alone does not hide it. HidHide must also be enabled.

If HidHide remains disabled, the game may receive input from both the physical controller and USC’s virtual controller, causing buttons to respond twice.

After applying the settings, check USC’s pressed-button display.

Press a controller button once and confirm that only one corresponding button input appears. If the same input appears twice from a single press, the physical controller may not be hidden correctly.

In the game’s controller settings, select **Wireless Controller**, which is the virtual controller created by USC.


## Controller calibration note

When a controller button is assigned as a layer Trigger key, USC processes that button as the Trigger key used for layer switching instead of sending it as a normal controller button.

For example, if the layer Trigger key is assigned to L1, temporarily clear the layer’s L1 Trigger key assignment before registering the original L1 button in a game’s controller calibration screen.

The original button is also not sent by itself when a controller button is remapped to another input in the NORMAL layer.

For example, if R2 is remapped to **R2 + Circle** in the NORMAL layer, the configured combination is sent instead of the original R2 button by itself.

Before controller calibration, temporarily clear the relevant layer Trigger key assignment or temporarily disable the relevant tab in the NORMAL layer.

After calibration is complete, the original USC settings can be restored.


# 現在確認されている仮想コントローラーの問題

現在、USCを長時間タスクトレイへ格納したまま使用すると、仮想コントローラーの一部の入力が反応しなくなる場合があります。


この現象が発生した場合は、USCをタスクトレイから一度表示してください。

タスクトレイから表示すると、反応しなくなった入力が復旧します。


ゲームを仮想フルスクリーンで使用している場合など、タスクトレイを直接操作しにくい環境では、USCを表示するためのショートカットをあらかじめ登録してください。

問題が発生した場合は、そのショートカットを使用してUSCをタスクトレイから表示してください。


タスクトレイから表示しても復旧しない場合は、タスクマネージャーからUSCを強制終了し、再起動してください。


この問題は現在未修正です。

開発資金に余裕ができ次第、原因を調査し、可能であれば修正を行います。



# Known virtual controller issue

When USC remains minimized to the system tray for an extended period, some virtual controller inputs may stop responding.


If this occurs, restore USC from the system tray.

Restoring USC from the system tray should make the affected inputs work again.


When using a game in borderless fullscreen mode, or in another environment where accessing the system tray is difficult, register a shortcut for showing USC in advance.

If the issue occurs, use that shortcut to restore USC from the system tray.


If restoring USC does not resolve the issue, force-close USC through Task Manager and restart it.


This issue is currently unresolved.

When sufficient development funding becomes available, the cause will be investigated and a fix will be attempted if possible.
