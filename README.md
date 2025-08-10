<p align="center"><font size="6"><b>暑修資料結構期中報告 11128004 林峻成 11124129 吳張傑</b></font></p>

<p align="center">資料結構 [Python--Stack] 的應用</p>


一、什麼是棧

棧是一個有序集合，根據其特性可以稱為「先進後出」或「後進先出」，其中添加或刪除都發生在同一端，這一端被稱為「棧頂」，與其對應的叫「棧底」。

棧的底部很重要，因為其底部儲存的資料是時間最長的，最近的添加項總是最先會彈出，這種排序原則有時被稱為「LIFO」。

二、棧

1. 棧的可用操作

      Stack() 創建一個空的棧。它不需要參數，並返回一個空棧。

      push(item) 將一個新項添加到棧的頂端。它需要 item 作為參數並不返回任何內容。

      pop() 從棧中刪除頂部項。它不需要參數並返回 item。棧被修改。

      top() 讓你查看頂部項，但不會刪除它。不需要參數。不能修改。

      isEmpty() 測試棧是否為空。不需要參數，並返回布林值。

      size() 返回棧中 item 數量。不需要參數，並返回一個整數。

      clear 清空棧，沒有返回值。


3. 利用 Python 的內置資料結構 List 實現堆疊全部操作
<img width="545" height="739" alt="二" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/2.png">
輸出結果
<img width="545" height="739" alt="二" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/2-%E7%B5%90%E6%9E%9C.png">


      
三.堆疊的使用示例



3-1 進制轉換


<img width="532" height="756" alt="三-1" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-1.png" />



輸出結果

<img width="1415" height="83" alt="三-1結" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-1%E7%B5%90%E6%9E%9C.png" />


說明：這是用 List 結構來實現的「棧」，同樣我們可以自己寫一個棧


3-2 自己寫堆疊

<img width="465" height="611" alt="三-2" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-2.png" />



輸出結果

<img width="830" height="191" alt="三-2結" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-2%E7%B5%90%E6%9E%9C.png" />

說明：

1.上面所定義的堆疊，是由 top 指針指向一個完整的 Node 實例

2.定義一個堆疊，使用指針控制其最頂端的位置



3-3 程式碼—將數學表達式轉成前序式

<img width="463" height="650" alt="三-3" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-3-1.png" />

<img width="864" height="749" alt="三-3-" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-3-2.png" />



輸出結果

<img width="783" height="72" alt="三-3結" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-3%E7%B5%90%E6%9E%9C.png" />

說明：

1.程式碼主要是將數學運算中的中序轉換成前序表示法

2.在程式中以堆疊方式來進行操作，有效儲存運算符號、運算元等資料類型與次序位置來進行計算，結果再以人性、直覺方式進行完成。


3-4 程式碼—後序表達式（逆波蘭式）

<img width="997" height="943" alt="三-4" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-4-1.png" />

<img width="539" height="826" alt="三-4-" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-4-2.png" />

<img width="539" height="826" alt="三-4-" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-4-3.png" />




輸出結果

<img width="539" height="826" alt="三-4-" src="https://github.com/Arno930610/Data-Structure-Report/blob/main/3-4%E7%B5%90%E6%9E%9C.png" />


說明：

1.程式碼是將中序數學運算轉換成了後序數學表示法

2.在程式中以堆疊方式來進行操作，模擬運算順序，遇到符號就依照堆疊的資料與次位置推進並進行計算（如堆疊「放」與「取」操作），結果再以人性、直覺方式完成

3.後序表達式適合用來做計算作業（執行中序轉後序 → 執行後序計算）




四.總結：

| 類別       | 中序表達式             | 前序轉換               | 後序轉換             |
|------------|------------------------|------------------------|----------------------|
| 表達形式   | `1 + (3 + 4) * 2`      | `+ 1 * + 3 4 2`        | `1 3 4 + 2 * +`      |
| 轉換方式   | 人類可讀，但難處理     | 先處理最外層，再向內遞迴 | 可用堆疊直接計算     |
| 計算難度   | 高                    | 中等                   | 最低                 |
| 適用範圍   | 一般數學              | 語法樹、遞迴計算         | 編譯器、計算器       |


資料參考"https://blog.51cto.com/essun/1941041"









