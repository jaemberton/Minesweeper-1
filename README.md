# Minesweeper

This Minesweeper program was written entirely in Javascript and jQuery and in its entirety comprises under 150 lines.

The implementation is as follows:

0. Define 2 functions, openSurroundingBoxes and calculateSurroundingMines, to be used later.
 
1. Prompt user for the dimensions and number of mines with JavaScript alert functions

2. Add boxes to container, each with id "boxij" (where i,j are coordinates)

  ・Implement with a nested for loop using the dimensions given by the user
  
  ・Insert carriage returns by adding "clear: both" to boxes at row ends using a jQuery statement

3. Generate mine locations using the number of mines given by the user

  ・These are calculated by computing unique random numbers from 0 to the number of boxes

  ・A "mine" class is added to selected mine locations with a jQuery statement

4. 

# マインスイーパー
このアプリはJS・jQueryだけで作られて、１５０行に限られた。

実装は以下のとおり。

0. 後で活用できるように、関数（openSurroundingBoxesとcalculateSurroundingMines）を定義する

1. JSのalert関数を使い、マス数とマイン数をユーザーに問う

2. マスを作成する。それぞれのマスは「boxij」というidを持たせる。

  ・forループとユーザーからもらったマス数を使って実装する
  
  ・jQueryを使ってそれぞれのrow突き当たりのマスに「clear: both」を挿入
  
3. ユーザーからもらったマイン数を使って、マインの場所を決める
4. 
  ・ユーニークな
