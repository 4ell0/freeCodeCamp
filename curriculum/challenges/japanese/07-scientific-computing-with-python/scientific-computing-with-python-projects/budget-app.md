---
id: 5e44413e903586ffb414c94e
title: 予算アプリ
challengeType: 10
forumTopicId: 462361
dashedName: budget-app
---

# --description--

<a href="https://replit.com/github/freeCodeCamp/boilerplate-budget-app" target="_blank" rel="noopener noreferrer nofollow">このプロジェクトには Replit スターターコードを使用します</a>。

-   Start by importing the project on Replit.
-   Next, you will see a `.replit` window.
-   Select `Use run command` and click the `Done` button.


# --instructions--

`budget.py` の `Category` クラスを完成させてください。 このクラスは *food* (食費)、*clothing* (服飾費)、*entertainment* (娯楽費) など、さまざまな予算のカテゴリーに応じてオブジェクトをインスタンス化できるようにする必要があります。 オブジェクトを作成する際に、カテゴリーの名前をオブジェクトに渡します。 クラスには、リスト型の `ledger` (帳簿) というインスタンス変数を持たせてください。 このクラスには次のメソッドも含める必要があります。

- A `deposit` method that accepts an amount and description. If no description is given, it should default to an empty string. The method should append an object to the ledger list in the form of `{"amount": amount, "description": description}`.
- A `withdraw` method that is similar to the `deposit` method, but the amount passed in should be stored in the ledger as a negative number. If there are not enough funds, nothing should be added to the ledger. This method should return `True` if the withdrawal took place, and `False` otherwise.
- A `get_balance` method that returns the current balance of the budget category based on the deposits and withdrawals that have occurred.
- A `transfer` method that accepts an amount and another budget category as arguments. The method should add a withdrawal with the amount and the description "Transfer to [Destination Budget Category]". The method should then add a deposit to the other budget category with the amount and the description "Transfer from [Source Budget Category]". If there are not enough funds, nothing should be added to either ledgers. This method should return `True` if the transfer took place, and `False` otherwise.
- A `check_funds` method that accepts an amount as an argument. It returns `False` if the amount is greater than the balance of the budget category and returns `True` otherwise. This method should be used by both the `withdraw` method and `transfer` method.

予算オブジェクトを出力するときは以下の項目を表示する必要があります。

- A title line of 30 characters where the name of the category is centered in a line of `*` characters.
- A list of the items in the ledger. Each line should show the description and amount. The first 23 characters of the description should be displayed, then the amount. The amount should be right aligned, contain two decimal places, and display a maximum of 7 characters.
- A line displaying the category total.

出力の例を次に示します。

```bash
*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96
```

`Category` クラスの他に、カテゴリのリストを引数に取る `create_spend_chart` という関数を (クラスの外で) 作成してください。 この関数は棒グラフとなる文字列を返す必要があります。

The chart should show the percentage spent in each category passed in to the function. The percentage spent should be calculated only with withdrawals and not with deposits. Down the left side of the chart should be labels 0 - 100. The "bars" in the bar chart should be made out of the "o" character. 各棒の高さは最も近い 10 に切り下げる必要があります。 The horizontal line below the bars should go two spaces past the final bar. Each category name should be written vertically below the bar. There should be a title at the top that says "Percentage spent by category".

この関数は最大 4 つのカテゴリでテストされます。

次の出力例を参考にして、出力の間隔を例と正確に合わせてください。

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

このプロジェクトの単体テストは `test_module.py` にあります。

## 開発

Write your code in `budget.py`. For development, you can use `main.py` to test your `Category` class. Click the "run" button and `main.py` will run.

## テスト

We imported the tests from `test_module.py` to `main.py` for your convenience. The tests will run automatically whenever you hit the "run" button.

## 提出

Copy your project's URL and submit it to freeCodeCamp.

# --hints--

Category クラスを作成し、すべてのテストを成功させる必要があります。

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
