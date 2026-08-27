# Ultimate Shift Controller

**Windows controller / keyboard / mouse remapper**  
**Current formal release: v3.0.4**

Ultimate Shift Controller (USC) is a **free, lightweight, portable input remapper for Windows** built for practical everyday use.

It combines **NORMAL / HYPER / ULTRA / ULTIMATE layered input**, live HUD feedback, keyboard and mouse remapping, virtual controller workflows, profiles, turbo, and — as of v3.0.4 — **Google Chrome on-device translation**.

> USC is no longer the early BETA project described here in March 2026.  
> The core system is now largely complete and released for normal use. Updates are still published when bugs are found or practical improvements are added.

## Download

- itch.io: https://lu-ciel.itch.io/ultimate-shift-controller
- Repository: https://github.com/Lu-ci-el/UltimateShiftController

## Guides

- 日本語・画像付き説明: [Instructions_jp.md](Instructions_jp.md)
- English illustrated guide: [Instructions_en.md](Instructions_en.md)
- 日本語・レイヤー運用例: [README_JP.md](README_JP.md)
- English layer workflow example: [README_en.md](README_en.md)

Video: https://www.youtube.com/watch?v=xKO9DV92bWc

![Ultimate Shift Controller](/USC.png)

---

# 日本語

## Ultimate Shift Controller とは

Ultimate Shift Controller は、**コントローラー・キーボード・マウスの複雑な入力を、人間が実際に扱いやすい形へ整理する**ために作ったWindows用入力ツールです。

もともとはHyperShiftのようなレイヤー入力を自分で作り始めたことがきっかけでした。

https://github.com/Lu-ci-el/HyperShiftController

そこから機能を拡張し続け、現在は単なるHyperShift風ツールではなく、4レイヤー入力、ライブHUD、仮想コントローラー、プロファイル、ターボ、入力状態の可視化、翻訳などをまとめた独立したツールになっています。

USCが重視しているのは、機能数を増やすことそのものではありません。

- ボタン不足を補う
- 指の負担を減らす
- 同時押しや多ボタン操作を扱いやすくする
- 今どのレイヤーなのか分かるようにする
- 実際に何を押して何が出力されているのか確認しやすくする
- 複雑な設定でも日常的に使い続けやすくする

といった、実際に使っている時の困りごとを減らすことを目的にしています。

## v3.0.4 の主なポイント

### 4つの入力レイヤー

- **NORMAL** — 通常状態
- **HYPER** — HYPER呼出中
- **ULTRA** — ULTRA呼出中
- **ULTIMATE** — HYPER + ULTRAを同時に押している間

同じ物理キーやボタンへ、レイヤーごとに異なる役割を持たせられます。

HYPER / ULTRAの論理呼出キーには **F13～F24** を使用できます。HYPER / ULTRA / ULTIMATEの入力側では左クリック・右クリックも割り当て可能です。

### ライブHUD

USCのHUDは装飾だけではなく、実際の操作確認に使うためのHUDです。

- 現在のレイヤー
- 押している入力
- ラベル / ボタン名
- 成立している入力状態
- 発火したショートカット
- 実際の出力

などを確認できます。

画像、透過画像、GIF、サウンド、フェード、色、サイズ、透明度、クリック透過なども設定できるため、入力確認だけでなく配信や視覚表現にも利用できます。

### キーボード / マウス / コントローラーのリマップ

- キー → キー
- マウス → キー / ショートカット
- コントローラー → キーボード
- コントローラー系出力のリマップ
- 修飾キーを含むショートカット
- 複数キー同時出力
- 条件付きターボ
- パススルー制御
- スティック / 軸 / デッドゾーン調整
- タブ / プロファイルによる整理

などに対応しています。

### Google Chromeの端末内翻訳

v3.0.4では、**64bit版Google Chromeの端末内翻訳機能**を利用した翻訳機能を搭載しています。

基本操作:

1. 外国語の文章を選択
2. 設定した翻訳起爆キーを押す
3. USCで設定している自分の言語へ翻訳
4. 返事を自分の言語で書いて選択
5. 再び起爆すると、直前の相手言語へ翻訳
6. 自動コピーONなら翻訳結果をClipboardへコピー
7. **自動貼り付けは行いません**

標準14言語に対応し、Chrome側で利用可能な追加言語はBCP-47指定で準備できます。

通常翻訳時にWeb翻訳サイトを開く方式ではありません。Chromeが所有する端末内翻訳モデルを利用し、USC側へChromeのProfile、TranslateKit、Language Pack、Model、Cacheをコピーしません。

※ 翻訳機能には64bit版Google Chromeと、Chrome側で利用可能な対象言語モデルが必要です。Microsoft EdgeへのFallbackはありません。

### 日本語IME補助

日本語UIでは、英数入力のままローマ字を打ってしまった時に、**変換キーを2回押して直前の半角英数列をかな入力へ打ち直す補助機能**も利用できます。

## 軽量・ポータブル

USCにはインストーラーはありません。

1. ZIPをダウンロード
2. 任意の書き込み可能な場所へ展開
3. `UltimateShiftController.exe` を起動

設定やプロファイルはUSCフォルダー内の `Settings` 以下で管理されます。

### 動作環境

- 64bit Windows
- Windows 10 / Windows 11
- .NET 8 Desktop Runtime (x64)
- キーボード / マウス
- 翻訳機能を使う場合: 64bit Google Chrome
- 仮想コントローラー機能を使う場合: 環境に応じてViGEmBus / HidHideなどの関連設定

## 仮想コントローラーを使用する場合の重要な注意

仮想コントローラーを使用する場合は、USCのHidHide設定で**ゲームから隠す物理コントローラーを選択し、HidHide自体も有効**にしてください。

物理コントローラーを選択しただけでは非表示になりません。

HidHideが無効のままだと、ゲームへ物理コントローラーとUSCの仮想コントローラーの両方から入力が送られ、**二重入力**になる場合があります。

設定後はUSCの押下ボタン表示を確認し、ボタンを1回押した時に同じ入力が2つ表示されていないか確認してください。

ゲーム側で仮想DS4を使用する場合は、USCが作成した **Wireless Controller** を選択してください。

### コントローラーが認識されない場合

特に仮想コントローラー、HidHide、他のリマップツールを併用している環境では、USCを**管理者として実行**すると改善する場合があります。

Xbox One系コントローラーで仮想コントローラーを使う場合も、認識しない時はこの方法を試してください。

### キャリブレーション時の注意

レイヤーの起爆キーに使っている物理ボタンは、通常のボタンではなくレイヤー切り替え用として処理されます。

また、NORMALレイヤーで元ボタンを別入力へ変換している場合、ゲームのキャリブレーションには元ボタンそのものではなく設定済みの出力が送られます。

キャリブレーション時は、必要に応じて該当Triggerを一時解除するか、該当NORMALタブを一時的にOFFにしてください。完了後は元の設定へ戻せます。

## 現在確認されている仮想コントローラーの問題

現在、USCを長時間タスクトレイへ格納したまま使用すると、一部環境で仮想コントローラー入力が反応しなくなる場合があります。

発生した場合は、まずUSCをタスクトレイから表示してください。

それでも復旧しない場合は、タスクマネージャーからUSCを終了し、再起動してください。

この問題は現在も既知問題として扱っています。

## 利用上の注意

USCは入力リマッピングツールです。

オンラインゲームや各種サービスで使用する場合は、それぞれの利用規約を確認してください。リマップ、ターボ、仮想コントローラーなどの扱いはゲームやサービスによって異なります。

他人の操作を妨害する目的、不正利用、迷惑行為には使用しないでください。

## 多言語・カスタマイズ

USCには**14種類の標準言語プリセット**があります。

多くのUI文字列はカスタマイズでき、独自言語ファイルやプロファイルを他のユーザーと共有することもできます。

## Support / 不具合報告

不具合報告:
https://github.com/Lu-ci-el/UltimateShiftController/issues

もしUSCが役に立ったと感じたら、支援も歓迎しています。

- Ofuse: https://ofuse.me/lost
- Ko-fi: https://ko-fi.com/lost2

もちろん無料で使ってもらうだけでも大丈夫です。便利だと思ったら、ほかの人にも紹介してもらえると嬉しいです。

---

# English

## What Ultimate Shift Controller is

Ultimate Shift Controller is a **free, lightweight, portable Windows input remapper** designed to make complex controller, keyboard, and mouse setups easier to use in real life.

It originally started while I was recreating HyperShift-style layered input, but it has grown far beyond that early project. USC is now a standalone tool combining four input layers, live HUD feedback, virtual controller workflows, profiles, turbo, input-state visibility, and translation.

The goal is not simply to have the longest feature list. USC is built to help with practical problems such as:

- not having enough buttons
- finger strain from repeated inputs
- awkward simultaneous inputs
- mistakes in dense multi-button layouts
- forgetting layered layouts
- not knowing which layer is currently active
- not knowing what input USC actually interpreted or sent

## Main features in v3.0.4

### Four practical layers

- **NORMAL** — default state
- **HYPER** — while the HYPER trigger is held
- **ULTRA** — while the ULTRA trigger is held
- **ULTIMATE** — while HYPER + ULTRA are held together

The same physical key or button can therefore perform different actions depending on the current layer.

HYPER and ULTRA logical triggers use **F13-F24**. Left and right mouse buttons can also be used on the input side of HYPER / ULTRA / ULTIMATE mappings.

### Live HUD

USC's HUD is designed for practical real-time feedback, not just decoration.

It can show:

- current layer
- currently pressed input
- labels / button names
- effective input state
- triggered shortcuts
- actual output

The HUD also supports images, transparent images, GIFs, sounds, fades, custom colors, resizing, opacity, and click-through behavior, so it can also be used for streaming or creative visual feedback.

### Keyboard / mouse / controller remapping

USC supports practical workflows including:

- key-to-key remapping
- mouse-to-key / shortcut mapping
- controller-to-keyboard mapping
- controller-style output remapping
- shortcuts with modifiers
- multi-key outputs
- conditional turbo
- passthrough control
- stick / axis / deadzone adjustments
- tabs and profiles

### Google Chrome on-device translation

v3.0.4 adds translation using **64-bit Google Chrome's on-device translation capability**.

Typical workflow:

1. Select foreign-language text
2. Press your configured translation ignition key
3. Translate it into your own USC language
4. Write your reply in your own language and select it
5. Trigger again to translate it back into the last successful conversation language
6. Optional auto-copy places the outgoing translation on the Clipboard
7. **USC never auto-pastes the result**

USC includes 14 built-in languages, and additional languages can be prepared individually with BCP-47 tags when supported by Chrome.

Normal translation does not work by opening a web translation site. USC uses Chrome-owned on-device translation models and does not copy Chrome Profile, TranslateKit, language packs, models, or cache into the USC folder.

Translation requires 64-bit Google Chrome and a supported Chrome-side model. There is no Microsoft Edge fallback.

## Portable setup

No installer is required.

1. Download the ZIP
2. Extract it to a writable folder
3. Run `UltimateShiftController.exe`

Profiles and related settings are managed under USC's own `Settings` folder.

### Requirements

- 64-bit Windows
- Windows 10 / Windows 11
- .NET 8 Desktop Runtime (x64)
- keyboard / mouse
- 64-bit Google Chrome for Translation
- additional virtual-controller drivers/settings such as ViGEmBus / HidHide when those features are used

## Important notice when using a virtual controller

When using a virtual controller, select the physical controller that should be hidden from games in USC's HidHide settings **and enable HidHide itself**.

Selecting the controller alone does not hide it.

If HidHide is disabled, the game may receive input from both the physical controller and USC's virtual controller, causing **double input**.

After setup, press a controller button once and check USC's pressed-button display. If the same input appears twice from one press, the physical controller may not be hidden correctly.

When using USC's virtual DS4 output, select **Wireless Controller** in the game's controller settings.

### If your controller is not detected

Try running Ultimate Shift Controller **as Administrator**. Some environments require elevated permissions, especially when virtual controller drivers, HidHide, or other remapping tools are installed.

This can also help with Xbox One controller setups using USC's virtual controller features.

### Controller calibration note

A physical button used as a layer trigger is processed as the layer trigger rather than as its original controller button.

Also, if a NORMAL-layer mapping converts a button into another input, the configured output is sent during calibration instead of the original button by itself.

Temporarily clear the relevant trigger or disable the relevant NORMAL tab before calibration, then restore the USC settings afterward.

## Known virtual controller issue

When USC remains minimized to the system tray for an extended period, some environments may experience virtual controller inputs that stop responding.

If this occurs, restore USC from the system tray first.

If that does not recover the input, close USC through Task Manager and restart it.

This is still treated as a known issue.

## Terms of use

USC is an input remapping utility. When using it with online games or services, check the rules of the game or service you are using. Remapping, turbo, and virtual controller behavior may be treated differently by different services.

Do not use USC to interfere with other users, abuse services, or perform prohibited activity.

## Languages and customization

USC includes **14 default language presets**.

Many UI strings can be customized, and custom language files and profiles can be shared with other users.

## Support / Bug reports

Bug reports:
https://github.com/Lu-ci-el/UltimateShiftController/issues

Support is also welcome if USC has been useful to you:

- Ofuse: https://ofuse.me/lost
- Ko-fi: https://ko-fi.com/lost2

Using the tool is already appreciated. If you find it useful, sharing it with other people helps too.


💸 Seriously, someone support me! / マジで誰かお布施くれｗｗ

🇯🇵 日本語 — ja-JP
マジで誰かお布施くれｗｗ 😂
USCの開発を続ける燃料になります！

🇺🇸 English — en-US
Seriously, someone please throw me a donation lol 😂
It helps keep USC development going!

🇬🇧 English — en-GB
Seriously, someone chuck me a donation 😂
It helps keep USC development going!

🇩🇪 Deutsch — de-DE
Ernsthaft, spendiert mir doch jemand eine kleine Spende 😂
Damit ich USC weiterentwickeln kann!

🇪🇸 Español — es-ES
En serio, que alguien me eche una donación 😂
¡Así puedo seguir desarrollando USC!

🇫🇷 Français — fr-FR
Sérieusement, quelqu’un peut me faire un petit don ? 😂
Ça m’aide à continuer le développement d’USC !

🇮🇹 Italiano — it-IT
Sul serio, qualcuno mi faccia una piccola donazione 😂
Mi aiuta a continuare lo sviluppo di USC!

🇰🇷 한국어 — ko-KR
진짜 누가 후원 좀 해줘요 ㅋㅋ 😂
USC 개발을 계속하는 데 큰 힘이 됩니다!

🇵🇱 Polski — pl-PL
Serio, niech ktoś dorzuci parę groszy 😂
To pomaga mi dalej rozwijać USC!

🇧🇷 Português — pt-BR
Sério, alguém manda uma doação aí kkk 😂
Isso ajuda a continuar o desenvolvimento do USC!

🇷🇺 Русский — ru-RU
Серьёзно, кто-нибудь, закиньте немного на поддержку 😂
Это поможет мне продолжать разработку USC!

🇹🇷 Türkçe — tr-TR
Cidden biri biraz destek atsın ya 😂
USC'yi geliştirmeye devam etmemi sağlıyor!

🇨🇳 简体中文 — zh-CN
真的，谁来赞助一下吧哈哈 😂
这能让我继续开发 USC！

🇹🇼 繁體中文 — zh-TW
真的，誰來贊助一下啦哈哈 😂
這能讓我繼續開發 USC！

Support / お布施はこちら 😂

Ofuse: https://ofuse.me/lost
Ko-fi: https://ko-fi.com/lost2
