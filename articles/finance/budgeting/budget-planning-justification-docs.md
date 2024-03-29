---
title: เอกสารเหตุผลการวางแผนงบประมาณ
description: เอกสารเหตุผลให้ข้อมูลสำหรับผู้ที่ร้องของบประมาณเพื่ออธิบายว่าเหตุใดงบประมาณที่ระบุจึงเป็นสิ่งจำเป็น
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711784"
---
# <a name="budget-planning-justification-documents"></a>เอกสารเหตุผลการวางแผนงบประมาณ

[!include [banner](../includes/banner.md)]

เอกสารเหตุผลให้ข้อมูลสำหรับผู้ที่ร้องของบประมาณเพื่ออธิบายว่าเหตุใดงบประมาณที่ระบุจึงเป็นสิ่งจำเป็น 

เท็มเพลตแผนงบประมาณถูกสร้างโดยผู้จัดการงบประมาณใน Microsoft Word และถูกมอบหมายไปยังกระบวนการวางแผนงบประมาณปัจจุบัน จากนั้นเจ้าของงบประมาณสามารถเปิดเท็มเพลต และกรอกข้อมูลโดยอัตโนมัติใน Word โดยยึดตามคำของบประมาณของพวกเขา แล้วจึงสามารถเพิ่มข้อความเพิ่มเติมหรือข้อมูลก่อนที่จะบันทึกและแนบเอกสารเหตุผลส่วนบุคคลของตนไปยังแผนงบประมาณของพวกเขา

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>ตั้งค่า Add-in ของสำนักงาน Microsoft Dynamics สำหรับ Microsoft Word

1.  เปิดเอกสาร Microsoft Word ใหม่
2.  คลิก **แทรก** บน ribbon แล้วคลิก **ร้านค้า**
3.  ค้นหา Add-in ของสำนักงาน Microsoft Dynamics และคลิก **เพิ่ม**
4.  ใน Word ในบานหน้าต่างด้านขวา คลิก **เพิ่มข้อมูลเซิร์ฟเวอร์**
5.  พิมพ์หรือวาง URL ของเซิร์ฟเวอร์ และคลิก **ตกลง**

##### <a name="define-the-justification-template-in-microsoft-word"></a>กำหนดเท็มเพลตการจัดเต็มแนวของย่อหน้าใน Microsoft Word

1.  คลิก **ออกแบบ** ใน Add-in ของสำนักงาน Microsoft Dynamics หลังจากที่คุณได้ลงชื่อเข้าใช้
2.  สำหรับข้อมูลส่วนหัว ใช้ปุ่ม **เพิ่มฟิลด์**
3.  เลือกแหล่งข้อมูลเอนทิตี BudgetPlanJustification และคลิก **ถัดไป** **หมายเหตุ:** เอนทิตี้นี้เป็นสิ่งจำเป็นสำหรับเอกสารเหตุผลใด ๆ เอนทิตีอื่นๆ สามารถใช้ได้ แต่การอัพโหลดกลับไปยัง Microsoft Dynamics 365 Finance จะล้มเหลว ถ้าเอนทิตีนี้ไม่ได้ถูกรวมด้วย
4.  เพิ่มป้ายชื่อ BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter และ DocumentNumber และค่าในเอกสาร Word **หมายเหตุ:** คุณสามารถใช้ป้ายชื่อแบบกำหนดเองของคุณเอง แทนป้ายชื่อมาตรฐานได้ ถ้าจำเป็น
5.  คลิก **ทำ** เพื่อทำให้ส่วนหัวเสร็จสมบูรณ์
6.  สำหรับรายละเอียดระดับรายการของยอดเงินในแผนงบประมาณ คลิก **เพิ่มตาราง**
7.  เลือกแหล่งข้อมูลเอนทิตี BudgetPlanJustification อีกครั้ง และคลิก **ถัดไป**
8.  เพิ่มฟิลด์สำหรับ EffectiveDate, ScenarioName, AccountDisplayValue และ AccountingCurrencyExpenseAmount **หมายเหตุ:** ถ้ามีข้อคิดเห็นที่จะเพิ่มในรายการแผนงบประมาณแต่ละรายการ สามารถเพิ่มลงในตารางได้ที่นี่
9.  เพิ่มคำแนะนำเพิ่มเติมให้แก่ผู้ใช้ และดำเนินการการจัดรูปแบบหรือการกำหนดลักษณะใดๆ ที่จำเป็นลงในเอกสาร
10. บันทึกเอกสารลงในเครื่องคอมพิวเตอร์ของคุณ และปิดแฟ้มก่อนที่จะดำเนินการต่อ

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>ตั้งค่าระบวนการวางแผนงบประมาณที่จะใช้เท็มเพลตเหตุผล

1.  ไปที่ **การจัดงบประมาณ** &gt; **การตั้งค่า** &gt; **การวางแผนงบประมาณ** &gt; **แม่แบบเอกสารเหตุผล**
2.  คลิก **ใหม่** และเรียกดูเอกสาร Microsoft Word ที่สร้างใหม่ของคุณ
3.  ป้อนชื่อที่แสดงและคำอธิบายเท็มเพลต คลิก **ตกลง**
4.  ไปที่ **การจัดทำงบประมาณ** &gt; **การตั้งค่า** &gt; **งบประมาณ** **การวางแผน** &gt; **กระบวนการวางแผนงบประมาณ**
5.  เลือกกระบวนการที่เท็มเพลตเหตุผลควรจะใช้ และคลิก **แก้ไข**
6.  ในฟิลด์ **เท็มเพลตเอกสารเหตุผล** เลือกเท็มเพลตที่เหมาะสม และบันทึก

##### <a name="edit-and-save-personalized-justification-documents"></a>แก้ไขและบันทึกเอกสารเหตุผลส่วนบุคคล

1.  สร้างแผนงบประมาณใหม่หรือเปิดแผนงบประมาณที่มีอยู่
2.  ในเมนูแบบหล่นลง **เหตุผล** เลือก **สร้างเหตุผลใหม่**
3.  หลังจากกรอกข้อมูลลงในรายละเอียด เลือกเพื่ออัปโหลดเอกสารส่วนบุคคลจากเมนูแบบหล่นลง **เหตุผล**






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
