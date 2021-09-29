---
title: ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการแก้ไขปัญหาค่าฟิลด์ที่ไม่ถูกต้องใน TaxTrans
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 00424d98d5ff99123edf42ee19919d149e7a6abc
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488298"
---
# <a name="incorrect-field-value-in-taxtrans"></a>ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง

[!include [banner](../includes/banner.md)]

ถ้าค่าฟิลด์ใน **TaxTrans** ไม่ถูกต้อง ให้ใช้ข้อมูลในหัวข้อนี้เพื่อลองแก้ไขปัญหา

## <a name="overview-of-values"></a>ภาพรวมของค่า
รายการต่อไปนี้แสดงวิธี **TaxTrans** **TaxUncommitted** และ **TmpTaxWorkTrans** เป็นชุดข้อมูลที่คล้ายกัน แต่อยู่ในงานต่างกัน

  - **TaxTrans** เป็นผลลัพธ์ธุรกรรมภาษีที่ลงรายการบัญชีขั้นสุดท้ายที่ยังคงอยู่ในฐานข้อมูล
  - **TaxUncommitted** เป็นผลลัพธ์ภาษีที่คํานวณได้ระหว่างกลางที่ยังคงอยู่ในฐานข้อมูล (ถ้าเกี่ยวข้อง) ซึ่งจะใช้ในภายหลังในการลงรายการบัญชี
  - **TmpTaxWorkTrans** เป็นภาษีที่คํานวณชั่วคราวที่คํานวณได้ในตารางในหน่วยความจํา (ชนิดตาราง = InMemory)

หากคุณพบสาเหตุรากของคอลัมน์ **TaxTrans** ที่ไม่ถูกต้อง คุณจะพบสาเหตุรากของคอลัมน์ **TaxUncommitted** หรือ **TmpTaxWorkTrans** ที่ไม่ถูกต้องด้วย เนื่องจากแต่ละคอลัมน์คัดลอกจากกันและกัน

โดยทั่วไปในระหว่างการคํานวณภาษี **TmpTaxWorkTrans** จะมีการสร้าง แล้วระบบจะสร้าง **TaxUncommitted** ถ้าเกี่ยวข้อง ระหว่างการลงรายการบัญชีภาษี **TaxTrans** จะถูกสร้างขึ้น


## <a name="add-breakpoints"></a>เพิ่มจุดสั่งหยุด
หากต้องการเพิ่มจุดสั่งหยุด โปรดทำตามขั้นตอนต่อไปนี้ให้ครบถ้วน: 

1. เพิ่มส่วนขยายและจุดสั่งหยุดใน *insert()* และ *update()* ในส่วนขยายดังที่แสดงด้านล่าง

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. หรือคุณสามารถเพิ่มจุดสั่งหยุดโดยตรงเมื่อ **TaxUncommitted** ไม่ถูกรวมไว้

     - *TaxTrans.insert()* *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()* *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>การสร้างอีกครั้งและการดีบัก

หลังจากตั้งค่าจุดสั่งหยุดแล้ว การเปลี่ยนแปลงการยังคงอยู่ของข้อมูลทั้งหมดจะปรากฏในระหว่างการดีบัก เมื่อต้องการค้นหาสาเหตุรากของคอลัมน์ที่ไม่ถูกต้องของ **TaxTrans** **TaxUncommitted** หรือ **TmpTaxWorkTrans** ให้ตรวจทานและจดบันทึกรายการต่อไปนี้:

- จุดสั่งหยุดสุดท้ายที่คอลัมน์ถูกต้อง
- จุดสั่งหยุดแรกที่คอลัมน์ไม่ถูกต้อง
- สิ่งที่เกิดขึ้นระหว่างสองจุดดังกล่าว

## <a name="determine-whether-customization-exists"></a>ระบุว่ามีการเลือกเองอยู่หรือไม่
หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ยังไม่สามารถแก้ไขปัญหาได้ ให้ระบุว่ามีการเลือกเองอยู่หรือไม่ ถ้าไม่มีการกำหนดเอง โปรดติดต่อฝ่ายสนับสนุนของ Microsoft เพื่อขอความช่วยเหลือ

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

