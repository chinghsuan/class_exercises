# HW3 - Binary Search Tree（作業三！！）
* [我的程式碼](https://github.com/chinghsuan/class_exercises/blob/master/HW3/binary_search_tree_06170203.py)
* [我的學習歷程、流程圖、BST原理](https://github.com/chinghsuan/class_exercises/blob/master/HW3/binary_search_tree_%E5%AD%B8%E7%BF%92%E6%AD%B7%E7%A8%8B%E3%80%81%E6%B5%81%E7%A8%8B%E5%9C%96%E3%80%81BST%E5%8E%9F%E7%90%86_06170203.ipynb)
* [功能說明](#功能說明)
  * [新增](#新增)
  * [查詢](#查詢)
  * [刪除](#刪除)
  * [調整](#調整)
* [時間複雜度比較](#時間複雜度比較)
* [Reference](#Reference)

## 功能說明
### `新增`：
* **定義**：**`將指定的數值新增進入樹中`**。  
* **步驟**：  
```
1. 先判斷root是否為空，若為空則加入該insert值，若不為空則執行下述動作
2. 若該值大於root值，則繼續往右邊的子節點比較
3. 若該值小於root值，則繼續往左邊的子節點比較
4. 將值放入最後迴圈停留的位置
```

### `查詢`：
* **定義**：**`在樹中查找離root最近的指定數值的位置`**。  
* **步驟**：
```
1. 先判斷root是否為空，若為空則返回None，不為空，則執行下述動作
2. 當root不為空時，判斷需要尋找的目標值與root的值的大小比較，  
   當目標值大於root時，繼續往右邊子樹尋找，  
   反之，當目標值小於root時，繼續往左邊子樹尋找
3. 當root等於目標值時，返回該root
```
### `刪除`：
* **定義**：**`刪除樹中的所有指定數值，並重新排列成新的BST`**。  
* **步驟**：
```
1. 先將tree轉換為list結構
2. 將步驟1的list，用迴圈方式判斷，當值不等於目標刪除值時，新增該值到新的list中
3. 將步驟2的新的list，重新建構成新的一顆Tree
```
### `調整`：
**定義**：**`將樹中的所有指定數值改為新的指定數值，並重新排列成新的BST`**。  
**步驟**：
```
1. 先將原本的Tree轉換為list結構
2. 利用for迴圈與if判斷list中的值是否等於我們目標要更改的數值，若等於，則將該值替換成新的值
3. 將步驟2處理過後的list轉回Tree的結構
```
### 時間複雜度比較
|方法|平均Average|最差Worst|
|---|---|---|
|搜尋|O(log n)|O(n)|
|插入|O(log n)|O(n)|
|刪除|O(log n)|O(n)|

**空間複雜度**：
平均：O(n)
最差：O(n)

## Reference
http://alrightchiu.github.io/SecondRound/binary-search-tree-introjian-jie.html  
http://alrightchiu.github.io/SecondRound/binary-search-tree-searchsou-xun-zi-liao-insertxin-zeng-zi-liao.html  
