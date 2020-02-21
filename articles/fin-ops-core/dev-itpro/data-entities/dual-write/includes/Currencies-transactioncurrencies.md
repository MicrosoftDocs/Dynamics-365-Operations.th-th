## <a name="currencies-to-transactioncurrencies"></a>สกุลเงินสำหรับ transactioncurrencies

เท็มเพลตนี้ซิงโครไนส์ข้อมูลระหว่างแอป Finance and Operations และ Common Data Service

ตัวกรองต้นทาง: ((CURRENCYCODE != "999"))

ฟิลด์ Finance and Operations | ชนิดของการแม็ป | ฟิลด์ Dynamics 365 อื่นๆ | ค่าเริ่มต้น
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
none | >> | exchangerate | 1
