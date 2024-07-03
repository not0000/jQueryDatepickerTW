# jQueryDatepickerTW

## Demo 範例程式
https://codepen.io/not0000/pen/KvvGjr

## 程式來源
我在 Louis的隨手筆記 找到 民國年選擇器 DatePicker 2017年4月19日 星期三
http://softmenlouis.blogspot.com/2017/04/blog-post_74.html
這裡面有簡單介紹使用方法

用法跟Jquery Datepicker一樣
```$element.datepickerTW();```
在這邊有客製小功能：
```
splitMark: '/' // 分割年月日的標誌可自由設定年月日中間的分隔符號
yearPadZero: false年的部分(民國年)補滿3碼
```    
而真正的的程式碼註解則是寫 ```Created by EIJI on 2014/1/3.```
我不確定實際的版權歸屬如何，因此這邊僅記錄相關資訊，並寫下我理解的部分。

我在使用過程中，發現有一些小bug
1. 尚未製作比1911還小(民國前)的情況，所以如果民國年選到個位數，就會變成 1910 1911 1 2 3，選了1911，日期欄位回傳可能就真的會變成 民國1911年，因此不適用於製作可以選到民國年前的歷史文件，請留意。
1. 雖然有支援 dateFormat: 'yy-mm-dd' 的格式，可以調換 yy mm dd 的順序，但不能使用大寫的MM，如果用大寫的會變回英文月份
1. 如果是手動在input內輸入日期，而不是使用滑鼠點選民國年 datepicker 內的日期欄位，會造成下次再開啟時，自動切換回當天日期。 (西元年的無此問題)

如果還有發現其他問題，可以持續追加或是修正。
