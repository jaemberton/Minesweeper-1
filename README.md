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

# マインスイーパー
このアプリはJS・jQueryだけで作られて、１５０行に限られた。

実装は以下のとおり。

0. 後で活用できるように、関数（openSurroundingBoxesとcalculateSurroundingMines）を定義する

1. JSのalert関数を使い、マス数とマイン数をユーザーに問う

2. マスを作成する。それぞれのマスは「boxij」というidを持たせる。

  ・forループとユーザーからもらったマス数を使って実装する
  
  ・jQueryを使ってそれぞれのrow突き当たりのマスに「clear: both」を挿入
  
3. ユーザーからもらったマイン数を使って、マインの場所を決める

 ・0〜マイン数からの乱数を何個計算することで実装する
 
 ・jQueryでマインの場所に"mine"クラスを追加する
 
4. マスが選ばれる時の機能を実装する

 ・"mine"クラスが付いたマスが選択された場合、それぞれのマインを赤に染める（失敗を示す）
 
 ・"mine"クラスが付いていないマスが選択された場合、隣接するマイン数を計算してユーザーに示す
 
 ・隣接するマイン数が０の場合、隣接するマスを開く（ページ一面のマスが示している隣接するマイン数を１０回もチェックすることで、０に隣接するマスを再帰的に開ける）
 
 ・クリックの後、マインが残っているかどうかチェックして、もう残っていない場合はそれぞれのマインを青に染める（勝ちを示す）
