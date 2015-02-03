# マインスイーパー
このアプリはJS・jQueryで作られて、１５０行に限られた。

実装は以下のとおり。

0. 後で活用できるように、関数（openSurroundingBoxesとcalculateSurroundingMines）を定義する

1. JSのalert関数を使い、マス数と地雷数をユーザーに問う

2. マスを作成する。それぞれのマスは「boxij」というidを持たせる

  ・forループとユーザーからもらったマス数を使って実装する
  
  ・jQueryでそれぞれの列突き当たりのマスに「clear: both」を適用
  
3. 地雷数を使って、地雷の場所を決める

 ・0〜地雷数からの乱数を何個計算することで実装する
 
 ・jQueryで地雷の場所に「mine」クラスを追加する
 
4. マスが選択された時の機能を実装する

 ・「mine」クラスが付いたマスが選択された場合、ページ一面の地雷を赤に染める（負けを示す）
 
 ・「mine」クラスが付いていないマスが選択された場合、隣接する地雷数を計算して示す
 
 ・隣接する地雷数が０の場合、隣接するマスも開く（ページ一面の開かれたマスの隣接する地雷数を１０回もチェックすることで、それぞれの０に隣接するマスを再帰的に開く）
 
 ・クリック後、地雷が残っているかどうかチェックして、残っていない場合はページ一面の地雷を青に染める（勝ちを示す）

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

4. Implement functionality for when user selects a box

 ・If the user selects a box with "mine" class, color all mines red (signaling a loss)
 
 ・If the user selects a non-mine, calculate and display the number of adjacent mines
 
 ・If there are 0 adjacent mines, open all surrounding boxes recursively by iterating through all boxes of the page 10 times and clearing all necessary boxes each time through
 
 ・After each click, check if there are any mines left; if not, color all mines blue (signaling a win)
