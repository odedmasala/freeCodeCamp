---
id: 5e44413e903586ffb414c94e
title: 預算應用
challengeType: 10
forumTopicId: 462361
dashedName: budget-app
---

# --description--

你將使用<a href="https://replit.com/github/freeCodeCamp/boilerplate-budget-app" target="_blank" rel="noopener noreferrer nofollow">我們在 Replit 的初始化項目</a>來完成這個項目。

-   Start by importing the project on Replit.
-   Next, you will see a `.replit` window.
-   Select `Use run command` and click the `Done` button.


# --instructions--

完成 `budget.py` 中的 `Category` 類。 它應該能夠根據不同的預算類別實例化對象，例如 *食物* 、 *服裝* 和 *娛樂* 。 創建對象時，它們以類別的名稱傳遞。 該類應該有一個名爲 `ledger` 的實例變量，它是一個列表。 該類還應包含以下方法：

- A `deposit` method that accepts an amount and description. If no description is given, it should default to an empty string. The method should append an object to the ledger list in the form of `{"amount": amount, "description": description}`.
- A `withdraw` method that is similar to the `deposit` method, but the amount passed in should be stored in the ledger as a negative number. If there are not enough funds, nothing should be added to the ledger. This method should return `True` if the withdrawal took place, and `False` otherwise.
- A `get_balance` method that returns the current balance of the budget category based on the deposits and withdrawals that have occurred.
- A `transfer` method that accepts an amount and another budget category as arguments. The method should add a withdrawal with the amount and the description "Transfer to [Destination Budget Category]". The method should then add a deposit to the other budget category with the amount and the description "Transfer from [Source Budget Category]". If there are not enough funds, nothing should be added to either ledgers. This method should return `True` if the transfer took place, and `False` otherwise.
- A `check_funds` method that accepts an amount as an argument. It returns `False` if the amount is greater than the balance of the budget category and returns `True` otherwise. This method should be used by both the `withdraw` method and `transfer` method.

打印預算對象時，它應顯示：

- A title line of 30 characters where the name of the category is centered in a line of `*` characters.
- A list of the items in the ledger. Each line should show the description and amount. The first 23 characters of the description should be displayed, then the amount. The amount should be right aligned, contain two decimal places, and display a maximum of 7 characters.
- A line displaying the category total.

下面是一個輸出示例：

```bash
*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96
```

除了 `Category` 類之外，創建一個名爲 `create_spend_chart` 的函數（在類之外），它將類別列表作爲參數。 它應該返回一個作爲條形圖的字符串。

該圖表應顯示在傳遞給函數的每個類別中花費的百分比。 花費的百分比應該只計算取款而不是存款。 圖表左側應該是標籤 0 - 100。 條形圖中的“條”應由“o”字符組成。 每個條形的高度應四捨五入到最接近的 10。 條形圖下面的水平線應該超過最後一個條形圖再多兩個空格。 每個類別名稱應垂直寫在欄下方。 頂部應該有一個標題，上面寫着“Percentage spent by category”。

此功能將使用最多四個類別進行測試。

仔細查看下面的示例輸出，並確保輸出的間距與示例完全匹配。

```bash
Percentage spent by category
100|          
 90|          
 80|          
 70|          
 60| o        
 50| o        
 40| o        
 30| o        
 20| o  o     
 10| o  o  o  
  0| o  o  o  
    ----------
     F  C  A  
     o  l  u  
     o  o  t  
     d  t  o  
        h     
        i     
        n     
        g     
```

此項目的單元測試在 `test_module.py` 中。

## 開發

在 `budget.py` 中編寫你的代碼。 對於開發，你可以使用 `main.py` 來測試你的 `Category` 類。 單擊“運行”按鈕，`main.py` 將運行。

## 測試

爲了你的方便，我們將測試從 `test_module.py` 導入到 `main.py`。 只要你點擊“運行”按鈕，測試就會自動運行。

## 提交

複製項目的 URL 並將其提交給 freeCodeCamp。

# --hints--

它應該創建一個 Category 類並通過所有測試。

```js

```

# --solutions--

```js
/**
  Backend challenges don't need solutions,
  because they would need to be tested against a full working project.
  Please check our contributing guidelines to learn more.
*/
```
