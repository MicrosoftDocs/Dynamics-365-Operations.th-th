---
title: การทดสอบแบบวินิจฉัยข้อมูลโดยใช้ Regression Suite Automation Tool
description: บทความนี้จะกล่าวถึงข้อแนะนำสำหรับการทดสอบแบบวินิจฉัยข้อมูลโดยใช้ Regression Suite Automation Tool
author: FrankDahl
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.custom: 21761
ms.openlocfilehash: f4322cb76d1d83c02ec9d4dcb997a1cd4730d090
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269605"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>การทดสอบแบบวินิจฉัยข้อมูลโดยใช้ Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

ในขณะที่การตรวจสอบความถูกต้องของการทำงานของแอพลิเคชัน ERP ไม่สามารถวินิจฉัยข้อมูลได้อย่างครบถ้วน มีหลายระยะและวิธีการสำหรับการทดสอบ ระยะการทดสอบเหล่านี้รวมถึง:  

- กรอบงาน SysTest
- กรอบงาน ATL
- Regression Suite Automation Tool (RSAT)

[![พีระมิดของการจัดประเภทการทดสอบ](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>ภาพรวม
-   **กรอบงาน SysTest** – กรอบงาน SysTest มีความน่าเชื่อถือสำหรับการเขียน unit tests เนื่องจาก unit tests โดยทั่วไปจะมีการทดสอบวิธีการหรือฟังก์ชัน การทดสอบหน่วยควรเป็นการวินิจฉัยข้อมูลอยู่เสมอและขึ้นอยู่กับข้อมูลที่ป้อนไว้เท่านั้นที่ให้ไว้เป็นส่วนหนึ่งของการทดสอบ
-   **กรอบงาน ATL** – Microsoft มีกรอบงาน ATL ซึ่งเป็นการเชื่อมต่อบนกรอบงาน SysTest และทำให้การทดสอบการเขียนทำงานง่ายและน่าเชื่อถือมากขึ้น กรอบงานนี้ควรใช้สำหรับการเขียน component tests หรือ integration tests อย่างง่าย
-   **RSAT** – The RSAT ถูกใช้สำหรับ integration tests และการทดสอบวงจรธุรกิจ การทดสอบวงจรธุรกิจเรียกอีกอย่างหนึ่งว่าการทดสอบการตรวจสอบความถูกต้องของการถดถอยที่จะขึ้นอยู่กับข้อมูลที่มีอยู่ อย่างไรก็ตามการทดสอบเหล่านี้สามารถกลายมาเป็นการวินิจฉัยขอมูลถ้าคุณพิจารณาถึงปัจจัยเพิ่มเติม 

    - ที่ใด unit tests และ component tests อยู่ในระดับต่ำและสามารถเป็นการวินิจฉัยข้อมูลได้โดยสมบูรณ์ (ไม่ขึ้นอยู่กับชุดข้อมูลที่มีอยู่), วงจรธุรกิจหรือการทดสอบการตรวจสอบความถูกต้องของการถดถอยจะขึ้นอยู่กับข้อมูลบางอย่างที่มีอยู่ ข้อมูลนี้รวมถึงการตั้งค่า การตั้งค่าคอนฟิก (พารามิเตอร์) และข้อมูลหลัก (ลูกค้า ผู้จัดจำหน่าย สินค้า และอื่นๆ) แต่ไม่มีข้อมูลธุรกรรม ตรวจสอบให้แน่ใจว่ามีการเปลี่ยนแปลงใดๆเกิดขึ้นในระหว่างการทดสอบถ้ามี การเปลี่ยนแปลงข้อมูลเหล่านี้จะถูกแปลงกลับเป็นส่วนหนึ่งของการทดสอบครั้งสุดท้าย
    - เลือกข้อมูลหลักตามเงื่อนไขบางอย่างแทนที่จะเลือกเรกคอร์ดเฉพาะ ตัวอย่างเช่น ถ้าคุณต้องการเลือกสินค้าตามค่ามิติของสินค้าและความพร้อมใช้งานของสินค้าคงคลัง ให้กรองข้อมูลรายการผลิตภัณฑ์ที่มีค่าดังกล่าวโดยให้เลือกสินค้าแรกและคัดลอกหมายเลขที่จะใช้สำหรับการทดสอบในอนาคต ถ้าเป็นบรรทัดข้อมูลหลักอย่างง่ายเช่นลูกค้าผู้จัดจำหน่ายหรือสินค้าจะสามารถสร้างขึ้นโดยเป็นส่วนหนึ่งของการทำงานอัตโนมัติและใช้ในการทดสอบในอนาคตผ่านการผูกมัด 
    - ป้อนตัวระบุเฉพาะเช่นหมายเลขใบแจ้งหนี้ โดยใช้ลำดับหมายเลขหรือโดยการใช้ฟังก์ชัน Microsoft Excel เช่น =TEXT(NOW(),"yyyymmddhhmm") ฟังก์ชันนี้จะให้หมายเลขที่ไม่ซ้ำกันทุกนาทีซึ่งช่วยให้คุณสามารถติดตามเมื่อมีการดำเนินการเกิดขึ้น นี้สามารถใช้สำหรับตัวแปรเช่นหมายเลขใบรับสินค้าและหมายเลขใบแจ้งหนี้ของผู้จัดจำหน่าย การทดสอบเหล่านี้ยังคงทำงานอยู่ในฐานข้อมูลเดียวกันซ้ำแล้วซ้ำอีกโดยไม่ต้องมีการคืนค่าใดๆ
    - ตั้งค่า **โหมดการแก้ไข** ของสภาพแวดล้อมเพื่อให้ **อ่าน** หรือ **แก้ไข** เป็นกรณีการทดสอบแรกเสมอเนื่องจากตัวเลือกเริ่มต้นเป็นแบบ **อัตโนมัติ**  ตัวเลือก **อัตโนมัติ** จะใช้ในการตั้งค่าก่อนหน้านี้เสมอและสามารถทำให้เกิดการทดสอบที่ไม่น่าเชื่อถือ 
 
    [![หน้าตัวเลือก, แท็บประสิทธิภาพ](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - ตรวจสอบความถูกต้องหลังจากที่คุณกรองข้อมูลธุรกรรมเฉพาะแทนการตรวจสอบทั่วไปเท่านั้น ตัวอย่างเช่นสำหรับหมายเลขของเรกคอร์ดให้กรองข้อมูลสำหรับหมายเลขธุรกรรมหรือวันที่ทำธุรกรรมเพื่อให้การตรวจสอบความถูกต้องไม่รวมธุรกรรมอื่นๆทั้งหมด 
    - ถ้าคุณกำลังตรวจสอบยอดดุลลูกค้าหรือการตรวจสอบงบประมาณ ให้บันทึกค่าก่อนแล้วจึงเพิ่มมูลค่าของธุรกรรมของคุณเพื่อตรวจสอบความถูกต้องของผลลัพธ์ที่คาดไว้แทนที่จะตรวจสอบความถูกต้องของค่าที่คาดอย่างคงที่ 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
