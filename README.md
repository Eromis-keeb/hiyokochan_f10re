# hiyokochan_f10re ビルドガイド(簡易・ビルド経験者向け)

![9FD26103-95F8-4B8A-AB53-F37E3CD814FF_1_105_c](https://github.com/user-attachments/assets/98ff8c7e-a772-44c4-98ff-d9d73f96f4ac)


hiyokochan_f10reは4つのロータリーエンコーダー（一つはモード切り替え用）とAZ1UBALLによるポインティングデバイスを搭載した10個のキーのマクロパッドです
ファームウェアはVial対応です
vialのソフトウェアから自由にキーマップを変更可能です


### 必要な物



部品|個数
--|--
hiyokochan_f10re基板|x1
トッププレート|x1
RP2040-ZERO|x1
MX用スイッチソケット|x10
SK6812MINI-E |x16
OLED用ソケット |x1
高さ2.5mmコンスルー(4ピン分) |x1
SMDダイオード |x13
EC12互換ロータリーエンコーダ(プッシュスイッチ付き)※遊舎工房さんの高さ17.5mmの物を想定 |x4
AZ1UBALL |x1
ガスケットフォーム（1.5mm〜2mm) |x16
MXキースイッチ |x10
MXキーキャップ |x10




## 組み立て

LED→SMDダイオード→スイッチソケットの順ではんだ付けします

### LEDの取り付け

![D1438AEC-C123-4EE8-AD9F-28B62AF59C18_1_105_c](https://github.com/user-attachments/assets/b01ce70b-26af-452e-b86c-6f833be12e88)


LEDはGnd表記のある右上の位置とLED本体の先が欠けている部分を合わせるように設置し、表面のLight Sideに光る面が向くようになっているか確認の上ではんだ付けしてください

![4C1DD246-D908-45A1-B441-B565A9225C9D_1_201_a](https://github.com/user-attachments/assets/abda2830-7115-4a42-a6bf-e7282904eb4c)

赤丸の部分の欠けている部分と・・


![1E685349-B94A-4480-B06B-1E09D8CD7234_1_105_c](https://github.com/user-attachments/assets/e235d5ff-dd6e-4c39-9e30-6a863a82a41b)

緑枠のGND表記の欠けたような印刷の部分が合うように配置します

![121CD3D2-01D2-4998-93F1-4753CA7DBC22_1_105_c](https://github.com/user-attachments/assets/82a876e2-4903-47f9-bf64-5f3033610344)

私はGnd位置のパッドに予備はんだをしてそこを先につけていく事で向き間違いを防止しています


![AACD6369-66F6-41BE-AA8A-B672B2ACE389_1_105_c](https://github.com/user-attachments/assets/1d01bea9-b180-4298-98a7-03b3cce98f46)

LEDを置くとこのようになるはずです


![A0D3F910-CA83-40D4-AA16-E25D60798242_1_201_a](https://github.com/user-attachments/assets/942b001e-9ffa-49e1-a9d3-2f6d74604570)

表面から見るとこのように見えます
基板表面から見たときに欠けている部分が左上になっているのが正しい取り付け位置です。
裏面のLED1〜LED16の順番で付けていきます。


### SMD（ダイオード）の取り付け

SMDも同じ要領ではんだ付けしていきます。シルク上の線の入った印刷とSMD本体の線の入った向きを合わせるようにはんだ付けしてください

![DB4F116A-F9F5-444E-9EC8-A703ECAE511F_1_105_c](https://github.com/user-attachments/assets/007c5e54-941a-493c-9743-634721ed3d44)

赤枠の部分がSMD（ダイオード）の取り付け部分

![CCE193B6-B586-407E-80DA-1E26C4CD1A04_1_105_c](https://github.com/user-attachments/assets/2f34d51e-ba56-4fb3-bfbf-2a3016460cdc)

黄色枠の小さいダイオードを拡大すると・・・

![2DDC3A83-5CEF-4921-B0FC-9FF08C35F2C3_1_201_a](https://github.com/user-attachments/assets/03dcead0-b42c-49c8-963d-3cf0ec3464ec)

小さい赤枠内のように縦線がある部分があり・・


![0FC21235-EB95-45D9-B0EF-3D4A4D1A78A4_1_105_c](https://github.com/user-attachments/assets/eb1f0cc7-c559-4efe-9615-61ea2564b7fa)

基板側の印刷の赤枠内の縦線と向きを合わせて配置します

予備はんだも縦線がある方向にしておくと向きを間違いにくいです



![F4365F45-C6CC-42EE-AF02-16164902A7BC_1_105_c](https://github.com/user-attachments/assets/080fff23-a16a-40e8-b451-3bda3460f185)

緑枠内のようにはんだ付けします



### マイコン（RP2040-ZERO）の取り付け




![image](https://github.com/user-attachments/assets/f38c502a-88ec-41c0-98e9-c62e90bdf8ca)



![image](https://github.com/user-attachments/assets/03da02e9-dfe1-4ce2-82e7-f61ff2b2d355)

RP20400-zeroは写真のように基板表面から裏面にBOOTやRESETスイッチが向くように"表面"をはんだ付けしてください
事前にRP2040-ZEROに.uf2ファイル（ファームウェア）を書き込んでコンピューターに認識すさせてからはんだ付けするようにしてください


ファイルはコチラ→https://github.com/Eromis-keeb/hiyokochan_f10re/blob/8844423aac2b8ce7689a29006fab8ac0bf46c6d4/hiyokochan_f10re_vial.uf2






![491DFD50-61C6-4778-B75B-11053C33963A_1_105_c](https://github.com/user-attachments/assets/1f788524-1eb5-4ddd-80dc-1c58d3a804de)



### AZ1UBALLの台の取り付け


AZ1UBALLをマウントする為の”台”をOLED用ソケットを使って作ります。
AZ1UBALLは高さ2.5mmのコンスルーを使って基板に固定しますが、OLED用ソケットはコンスルーを付ける方とは”逆の”位置に裏面からはんだ付けしてください




![6D746D38-D1F0-493A-B5F5-37F72EFCED9E_1_105_c](https://github.com/user-attachments/assets/e08a0f56-c813-42a5-978a-5430d32cd9d2)
![58DC0DC5-51D2-4341-A366-CE6BC40F6838_1_105_c](https://github.com/user-attachments/assets/8244aff5-a5ba-4269-9f74-bfc0dca34d2e)

”台”の取り付け位置とコンスルー取り付け位置に注意してください。それぞれ”逆”の位置になります

AZ1UBALLはビルドガイドに従って組み立てておいてください。
https://github.com/palette-system/az1uball.git

尚、AZ1UBALLは取り付けなくてもマクロパッド自体は動作しますので必要ない場合は取り付けなくてもOKです



![A15033D6-D72B-43E2-932F-A9CADA71EAB5_1_105_c](https://github.com/user-attachments/assets/a49103af-08b4-4af1-bb82-3101559cfed7)
基板に装着するとこのような形になります



![06956E3E-A658-4070-9BC7-98FC12AD50D9_1_105_c](https://github.com/user-attachments/assets/876b67ed-1121-4759-beec-994c50483507)

青枠の部分にEC12互換のロータリーエンコーダーを基板裏面からはんだ付けしてください

![FDE5BDB6-5C1F-4694-B0D7-9129F3B9C376_1_105_c](https://github.com/user-attachments/assets/c78740a1-4c88-4b3e-a1a9-2385eae2639b)

その際、写真赤枠部分のツメをある程度広げてから取り付けると楽に出来ます

![37371505-1016-422E-8FFE-53DCCAFDED60_1_105_c](https://github.com/user-attachments/assets/27711cb3-f30a-4020-913d-aea81e40a16a)

取り付け後はこのようになります

![2EC1EAB3-4D0F-4524-B790-9449D35F4E4B_1_105_c](https://github.com/user-attachments/assets/7b8e3162-83a7-4c4f-9f8f-8279d12cdc30)

次にトッププレートにインジケーターバーを取り付けます

トッププレート裏側に接着剤や両面テープなどを使用して貼り付けてください
無くても動作に支障はありませんが、あるとインジケーターLEDが眩しくなくアニメーションを使用する場合滑らかに見える効果があります。

![116E7E8E-B808-45E3-BEBB-830073C7148D_1_105_c](https://github.com/user-attachments/assets/ef9fc64e-bf6d-4ec1-9a52-2ea4d124693a)

貼り付け後はこのようになります

![DF0AC707-5572-46AC-A611-AE481567ED2A_1_105_c](https://github.com/user-attachments/assets/9e62f0bf-da9f-4c00-9652-5e7c6d805b26)

トッププレートと基板を重ね、お好みのキースイッチとキーキャップを取り付けてください
その際、AZ1UBALLは取り外しキースイッチを取り付けた後でトッププレート上から装着してください

![39439403-A764-40AD-832C-F93E0323528F_1_105_c](https://github.com/user-attachments/assets/b3878848-305e-4204-a0d7-7ef9b22b80ea)


こここまで出来たらあとはお好みでロータリーエンコーダーノブを取り付けてガスケットフォームをトッププレートの耳に裏表両面に貼り付けてケースに取り付けて完成です。


![F0D8F3F9-89F0-4682-9CAE-9029C081E00D_1_105_c](https://github.com/user-attachments/assets/c946c44d-2759-459b-bbbb-0f01d391866e)


![6B84A406-9917-4934-BDF8-74563AA3C565_1_105_c](https://github.com/user-attachments/assets/89e8d769-3c1b-4b21-a95e-beebdca4ee98)


![414D99A4-E7B1-41A9-B2D1-4D92A5C9657E_1_105_c](https://github.com/user-attachments/assets/ca6e7654-5376-4dc7-81e4-bab141ee249b)



### ガスケットフォームについて

![814D0852-D050-4BB2-B3C5-7EF2CE7193E5_1_105_c](https://github.com/user-attachments/assets/cd8b4f6d-0eb8-47d3-95f1-23e971ee2097) 

ガスケットフォームについては写真のような物を使っていますが、このあたりは自由です
プレート下側は1.5mm以下、上側は2mmの厚みの物が個人的にはベストでした
尚、まったく使わない場合はケースの中でガタガタしますが一応使えます
片側だけ（上側）だけ貼るというのもアリかと思います




