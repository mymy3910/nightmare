# nightmare
すでに購入済みのチケット枚数・支払い済み額を算出して、
返礼品（1公演につき1セット）の申し込みを何点とするかで返金額を計算したい（概算）。

*************
　項目名　 
*************
//公演中止項目
・number_form         //各公演所持チケット枚数
・ticket_total_number //合計所持チケット枚数
・ticket_total_price  //合計支払い済み金額

//払い戻し・返礼品項目
・number_form_return  //返礼品申し込み数
・return_total_price  //合計返礼品申し込み額（ナイトメアへのお布施）
・refund_total_price　//払い戻し金額（自分へのお布施）

*************
　処理手順  
*************
1. number_formの入力値を取り出す
2. 1を数値として全て足し算を行う（合計する）
3. ticket_total_numberへ2を出力する
4. 2の結果に7000をかける
5. ticket_total_priceへ4を出力する

6. number_form_returnの入力値を取り出す
7. 6を数値として全て足し算を行う（合計する）
8. 7の結果に7000をかける
9. return_total_priceへ8を出力する
10. 4から8を引く。
11. 10をrefund_total_priceへ出力する

※7000はチケット代

*************
　 計算　　   
*************
2. ticket_total_number = number_formの合計　　　                     
4. ticket_total_price = ticket_total_number * 7000　　　　　　　　　  
8. return_total_price = (number_form_returnの合計) * 7000　　　　　 　
10. refund_total_price = (ticket_total_price) - (return_total_price)
