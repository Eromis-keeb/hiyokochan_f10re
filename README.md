# hiyokochan_f10re ビルドガイド(簡易・ビルド経験者向け)

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






![image](https://github.com/user-attachments/assets/03da02e9-dfe1-4ce2-82e7-f61ff2b2d355)



LED→SMDダイオード→スイッチソケットの順ではんだ付けします





![image](https://github.com/user-attachments/assets/f38c502a-88ec-41c0-98e9-c62e90bdf8ca)



RP20400-zeroは写真のように基板表面から裏面にBOOTやRESETスイッチが向くように"表面"をはんだ付けしてください
事前にRP2040-ZEROに.uf2ファイル（ファームウェア）を書き込んでコンピューターに認識すさせてからはんだ付けするようにしてください






![491DFD50-61C6-4778-B75B-11053C33963A_1_105_c](https://github.com/user-attachments/assets/82d514f4-db1e-41fb-adc5-5ae765b2b872)

AZ1UBALLをマウントする為の”台”をOLED用ソケットを使って作ります。
AZ1UBALLは高さ2.5mmのコンスルーを使って基板に固定しますが、OLED用ソケットはコンスルーを付ける方とは”逆の”位置に裏面からはんだ付けしてください




![6D746D38-D1F0-493A-B5F5-37F72EFCED9E_1_105_c](https://github.com/user-attachments/assets/e08a0f56-c813-42a5-978a-5430d32cd9d2)
![58DC0DC5-51D2-4341-A366-CE6BC40F6838_1_105_c](https://github.com/user-attachments/assets/8244aff5-a5ba-4269-9f74-bfc0dca34d2e)

”台”の取り付け位置とコンスルー取り付け位置に注意してください。それぞれ”逆”の位置になります

AZ1UBALLはビルドガイドに従って組み立てておいてください。
https://github.com/palette-system/az1uball.git


![A15033D6-D72B-43E2-932F-A9CADA71EAB5_1_105_c](https://github.com/user-attachments/assets/a49103af-08b4-4af1-bb82-3101559cfed7)
基板に装着するとこのような形になります

