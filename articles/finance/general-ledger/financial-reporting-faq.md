---
title: FAQ เกี่ยวกับการรายงานทางการเงิน
description: หัวข้อนี้แสดงรายการคำถามที่เกี่ยวข้องกับการรายงานทางการเงินที่ผู้ใช้รายอื่นมี
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070228"
---
# <a name="financial-reporting-faq"></a>FAQ เกี่ยวกับการรายงานทางการเงิน 

หัวข้อนี้แสดงรายการคำถามที่เกี่ยวข้องกับการรายงานทางการเงินที่ผู้ใช้รายอื่นมี 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>ฉันจะจํากัดการเข้าถึงรายงานโดยใช้ความปลอดภัยแบบแผนผังได้อย่างไร

สถานการณ์จำลอง: บริษัทสาธิต USMF มีรายงานงบดุลซึ่งไม่ต้องการให้ผู้ใช้รายงานทางการเงินทั้งหมดสามารถดูได้ใน D365 วิธีการ: คุณสามารถใช้ความปลอดภัยแบบแผนผังเพื่อจํากัดการเข้าถึงรายงานเดียว เพื่อให้ผู้ใช้บางรายเท่านั้นที่สามารถเข้าถึงรายงานได้ 

1.  ล็อกอินเข้าสู่ตัวออกแบบรายงานของโปรแกรมรายงานทางการเงิน

2.  สร้างข้อกำหนดแผนผังใหม่ (ไฟล์ | สร้าง | ข้อกำหนดแผนภูมิ) a.    ดับเบิลคลิกรายการ **สรุป** ในคอลัมน์ **ความปลอดภัยของหน่วย**
  i.    คลิก ผู้ใช้และกลุ่ม  
          1.    เลือกผู้ใช้หรือกลุ่มที่ต้องการเข้าถึงรายงานนี้ 
          
[![หน้าจอผู้ใช้](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![หน้าจอความปลอดภัย](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    คลิก **บันทึก**
  
[![ปุ่มบันทึก](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  ในข้อกำหนดของรายงานของคุณ ให้เพิ่มข้อกำหนดแผนผังใหม่

[![แบบฟอร์มข้อกำหนดแผนผัง](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  ขณะอยู่ในข้อกำหนดแผนผัง คลิก ตั้งค่า และภายใต้ "การเลือกหน่วยการรายงาน" เลือก "รวมหน่วยทั้งหมด"

[![แบบฟอร์มการเลือกหน่วยการรายงาน](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**ก่อนหน้า:** [![ภาพหน้าจอก่อนหน้า](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**หลังจาก:** [![ภาพหน้าจอหลังจาก](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

หมายเหตุ: สาเหตุของข้อความข้างต้นคือผู้ใช้ของฉันไม่มีสิทธิ์เข้าถึงรายงานนั้นหลังจากที่ใช้ความปลอดภัยของหน่วย



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>ฉันจะหาได้อย่างไรว่าบัญชีใดที่ไม่ตรงกับยอดดุลของฉันใน D365

เมื่อคุณมีรายงานที่ไม่ตรงกับสิ่งที่คุณคาดไว้ใน D365 ต่อไปนี้เป็นบางขั้นตอนที่คุณสามารถใช้ระบุบัญชีเหล่านั้นและส่วนแตกต่าง 

### <a name="in-financial-reporter-report-designer"></a>ในตัวออกแบบรายงานของโปรแกรมรายงานทางการเงิน

1.  สร้างข้อกำหนดของแถว a.    คลิก แก้ไข | แทรกแถวจากมิติ i.  เลือก MainAccount [![เลือกหน้าจอหลัก_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. คลิก ตกลง b.    บันทึกข้อกำหนดของแถว

2.  สร้างข้อกำหนดของคอลัมน์ใหม่     [![สร้างข้อกำหนดของคอลัมน์ใหม่](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  สร้างข้อกำหนดของรายงาน a.    คลิก การตั้งค่า และยกเลิกการเลือก [![แบบฟอร์มการตั้งค่า](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  สร้างรายงาน 

5.  ส่งออกรายงานไปยัง Excel

### <a name="in-d365"></a>ใน D365: 
1.  คลิก บัญชีแยกประเภททั่วไป | การสอบถามและรายงาน | งบทดลอง a.    พารามิเตอร์ i.  วันที่เริ่มต้น: เริ่มต้นปีบัญชี ii. วันที่สิ้นสุด: วันที่คุณสร้างรายงาน iii.    ชุดมิติทางการเงิน “ชุดบัญชีหลัก” [![แบบฟอร์มบัญชีหลัก](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    คลิก คำนวณ

2.  ส่งออกรายงานไปยัง Excel

ตอนนี้ คุณจะสามารถคัดลอกข้อมูลจากรายงาน FR Excel และไปยังรายงานงบทดลอง D365 และเปรียบเทียบคอลัมน์ "ยอดดุลการปิดบัญชี" ได้


[!INCLUDE[footer-include](../../includes/footer-banner.md)]