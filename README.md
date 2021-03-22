# 6.6.-Troubleshooting

## Задача 1.

db.currentOp()
db.killOp()

Использовать составные индексы одного поля. 

## Задача 2.

Скорее всего это связано с механизмом удаления просроченных ключей

“Basically this means that if the database has many many keys expiring in the same second, and these make up at least 25% of the current population of keys with an expire set, Redis can block in order to get the percentage of keys already expired below 25%.”

## Задача 3.

Скорее всего что не успевает обработать запрос за отведенное время. 
Варианты предложены https://qna.habr.com/q/556032

## Задача 4.

не хватает памяти. 
сделать ревизию железа, попытаться оптимизировать базу. 
