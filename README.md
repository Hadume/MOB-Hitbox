# MOB-s-Hitbox
## 概要  
Minecraftの全てのMOBのヒットボックスを判定できます  
MCVer 「1.17.x」「1.18.x」 で動きます  
  
このデータパックは「再配布」や「改変」が自由だよ！  
<br>
  
## 使い方  
ヒットボックスを判定したいMOBの「~-50 ~-50 ~-50」 の位置でpredicateを実行してください  
<br>
  
## サンプルコマンド  
- BulletというタグのMOBが、ヒットボックスが重なっているMOBにダメージを与える  
	execute as @e[type=minecraft:armor_stand,tag=Bullet] at @s as @e[tag=!Bullet,distance=..50] positioned ~-50 ~-50 ~-50 if predicate hitbox:hitbox run effect give @s minecraft:instant_damage 1 0 true  
<br>
  
## 注意点  
- magma_cube, slime の"Size"は「0~9」まで判定できます。それ以外の値での場合 **判定できません**  
- phantom の"Size"を変更した場合 **判定がガバくなります**  
- player の匍匐状態は **判定がガバくなります**  
- Shulker の"Peek"は「0」「100」でのみ正確に判定できます。それ以外の値の場合 **判定がガバくなります**  
- Shulker の"AttachFace"を変更した場合 **判定ガバくなります**
<br>
  
## 連絡  
バグ報告や聞きたいことなどがありましたら[Twitter](https://twitter.com/Hadume_Damui)へご連絡をください  
<br>
  
## 更新履歴  
- v1.0 (2022/5/21)  公開  
