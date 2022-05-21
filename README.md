# MOB-Hitbox
## 概要  
Minecraftの全てのMOBのヒットボックスを判定できます  
MCVer 「1.17.x」「1.18.x」 で動きます  
<br>
  
## 使い方  
  
ヒットボックスを判定したいMOBの「~-50 ~-50 ~-50」 の位置でpredicateを実行してください
<br>
  
## サンプルコマンド
  
- BulletというタグのMOBが、ヒットボックスが重なっているMOBにダメージを与える
	execute as @e[type=minecraft:armor_stand,tag=Bullet] at @s as @e[type=!minecraft:armor_stand,distance=..50] positioned ~-50 ~-50 ~-50 if predicate hitbox:hitbox run effect give @s minecraft:instant_damage 1 0 true
## 注意点
- magma_cube, slime のSizeは「0~10」まで判定できます。それ以外の値での場合**判定できません**
- phantom のSizeを変更した場合**判定がガバくなります**
- player の匍匐状態は**判定がガバくなります**
- Shulker のPeekは「0」「100」でのみ正確に判定できます。それ以外の値の場合**判定がガバくなります**
<br>
  
## 連絡  
バグ報告や聞きたいことなどがありましたら[Twitter](https://twitter.com/Hadume_Damui)へご連絡をください  
<br>
  
## 更新履歴  
- v1.0 (2022/5/21)  公開  
