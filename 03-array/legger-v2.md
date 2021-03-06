# รายรับรายจ่าย 2.0
ให้เขียนโปรแกรมเก็บรายรับจายจ่ายของแต่ละวันในสัปดาห์เป็นจำวนนวนเงินเต็มบาท โดยมีรูปแบบดังนี้  

## INPUT
รับจำนวนเงินที่เป็นรายรับและรายจ่ายในวันนั้นๆ จนครบ 1 สัปดาห์  

    -------Day-------  
    Enter income:
    Enter Expend:

โดยที่ Day ดังรูปแบบจะเปลี่ยนไปเรื่อยๆตามชื่อวันต่างๆในสัปดาห์ซึ่งมีลำดับดังนี้  Sun Mon Tue Wed Thu Fri Sat  

หมายเหตุ : กำหนดค่า input แต่ละตัวมีค่าไม่เกิน 10,000

## OUTPUT
สรุปรายรับรายจ่ายของสัปดาห์นั้นออกมาเป็นตารางโดยมีรูปแบบดังนี้

     ---------------------------------
    | day | income | expend | balance |     
     ----- -------- -------- ---------       
    | Sun | xxxxxx | xxxxxx | *xxxxxx |
    | Mon |        |        |         |		
    | Tue |        |        |         |
    | Wed |        |        |         |
    | Thu |        |        |         |
    | Fri |        |        |         |
    | Sat |        |        |         |
     ----- -------- -------- ---------
    |total|        |        |         |
     ---------------------------------
### โดยกำหนดให้
1. จำนวน x เท่ากับจำนวนหลักสูงสุดของเลขที่รับได้
2. \* คือเครื่องหมายดังนี้  
    -  หากวันนั้นรายรับมากกว่าราบจ่ายให้ใส่เครื่องหมาย +  
    - หากวันนั้นรายรับน้อยกว่ารายจ่ายให้ใส่เครื่องหมาย –  
    - หากรายรับเท่ากับรายจ่าย ไม่ต้องใส่เครื่องหมายใด ๆ
3. balance คิดเฉพาะในวันนั้น ๆ เท่านั้น
4. total คือบรรทัดที่รวมรายรับ รายจ่าย และยอดคงเหลือของทั้งสัปดาห์นั้น

## ตัวอย่างโปรแกรม
ตัวอย่างที่ 1  
```
-------Sun-------
Enter income: 250
Enter Expend: 40
-------Mon-------
Enter income: 80
Enter Expend: 71
-------Tue-------
Enter income: 65
Enter Expend: 140
-------Wed-------
Enter income: 240
Enter Expend: 45
-------Thu-------
Enter income: 190
Enter Expend: 90
-------Fri-------
Enter income: 175
Enter Expend: 240
-------Sat-------
Enter income: 0
Enter Expend: 0
 ---------------------------------
| day | income | expend | balance |
 ----- -------- -------- ---------
| Sun |    250 |     40 | +   210 |
| Mon |     80 |     71 | +     9 |
| Tue |     65 |    140 | -    75 |
| Wed |    240 |     45 | +   195 |
| Thu |    190 |     90 | +   100 |
| Fri |    175 |    240 | -    65 |
| Sat |      0 |      0 |       0 |
 ----- -------- -------- ---------
|total|   1000 |    626 |     374 |
 ---------------------------------
```

ตัวอย่างที่ 2  
```
-------Sun-------
Enter income: 1500
Enter Expend: 500
-------Mon-------
Enter income: 2500
Enter Expend: 4000
-------Tue-------
Enter income: 250
Enter Expend: 85
-------Wed-------
Enter income: 1450
Enter Expend: 1800
-------Thu-------
Enter income: 25
Enter Expend: 25
-------Fri-------
Enter income: 900
Enter Expend: 1200
-------Sat-------
Enter income: 900
Enter Expend: 400
 ---------------------------------
| day | income | expend | balance |
 ----- -------- -------- ---------
| Sun |   1500 |    500 | +  1000 |
| Mon |   2500 |   4000 | -  1500 |
| Tue |    250 |     85 | +   165 |
| Wed |   1450 |   1800 | -   350 |
| Thu |     25 |     25 |       0 |
| Fri |    900 |   1200 | -   300 |
| Sat |    900 |    400 | +   500 |
 ----- -------- -------- ---------
|total|   7525 |   8010 | -   485 |
 ---------------------------------
```
