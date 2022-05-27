---
title: ทำความเข้าใจฟิลด์วันที่และเวลา
description: หัวข้อนี้จะอธิบายถึงสิ่งที่ควรคาดหวังเมื่อใช้ฟิลด์วันที่และเวลาใน Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f595e06d9ddc9b44e8820d814d888971444bdf6a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688502"
---
# <a name="understand-date-and-time-fields"></a>ทำความเข้าใจฟิลด์วันที่และเวลา

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



ฟิลด์ **วันที่และเวลา** เป็นแนวคิดพื้นฐานใน Microsoft Dynamics 365 Human Resources นับเป็นสิ่งสำคัญที่คุณจะต้องทำความเข้าใจวิธีการทำงานกับข้อมูล **วันที่และเวลา** ใน Dataverse และแหล่งข้อมูลภายนอก

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>การทำความเข้าใจความแตกต่างระหว่างชนิดของข้อมูลในฟิลด์วันที่และวันที่และเวลา

ฟิลด์ **วันที่และเวลา** มีข้อมูลโซนเวลา ในขณะที่ฟิลด์ **วันที่** ไม่มี ฟิลด์ **วันที่** แสดงข้อมูลเดียวกันในสถานที่ใดๆ เมื่อคุณป้อนวันที่ลงในฟิลด์ **วันที่** วันที่เดียวกันนั้นจะถูกเขียนลงในฐานข้อมูล

เมื่อข้อมูลแสดงในฟิลด์ **วันที่และเวลา** วันที่และเวลาจะถูกปรับปรุงตามโซนเวลาของผู้ใช้ที่ถูกเลือกในหน้า **ตัวเลือกผู้ใช้** (**ทั่วไป \> ตั้งค่า \> ตัวเลือกผู้ใช้**) ข้อมูลวันที่และเวลาที่คุณป้อนในฟิลด์อาจไม่ใช่ข้อมูลเดียวกันกับข้อมูลที่เขียนลงในฐานข้อมูล

[![หน้าตัวเลือกผู้ใช้](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>การทำความเข้าใจฟิลด์วันที่และเวลาในหน้า 

ข้อมูล **วันที่และเวลา** ที่แสดงบนหน้าจอจะไม่เหมือนกับข้อมูลที่จัดเก็บไว้ในฐานข้อมูล ถ้าโซนเวลาของผู้ใช้ไม่ได้รับการตั้งค่าเป็นเวลามาตรฐานสากล (UTC) ข้อมูลในฟิลด์ **วันที่และเวลา** จะถูกจัดเก็บเป็น UTC เสมอ

[![UTC ของหน้าผู้ปฏิบัติงาน](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>ทำความเข้าใจฟิลด์วันที่และเวลาในฐานข้อมูล 

เมื่อค่า **วันที่และเวลา** ถูกเขียนลงในงฐานข้อมูล จะมีการจัดเก็บข้อมูลเป็น UTC ดังนั้น ผู้ใช้จะสามารถดูข้อมูล **วันที่และเวลา** ใดๆ ที่เกี่ยวข้องกับโซนเวลาที่กำหนดไว้ในตัวเลือกผู้ใช้ของตนเองได้
 
ในตัวอย่างข้างต้น เวลาเริ่มต้นคือเวลาที่ไม่ใช่วันที่เฉพาะ เมื่อเปลี่ยนโซนเวลาของผู้ใช้ที่ล็อกอินจาก GMT +12:00 เป็น GMT UTC เรกคอร์ดเดียวกันจะแสดง 04/30/2019 12:00:00 แทน 05/01/2019 12:00:00

ในตัวอย่างด้านล่าง การจ้างงานของพนักงาน 000724 จะกลายเป็นใช้งานอยู่ในเวลาเดียวกัน ไม่ว่าจะเป็นโซนเวลาใด พนักงานจะกลายเป็นใช้งานอยู่เมื่อ 04/30/2019 ในโซนเวลา GMT ซึ่งเหมือนกับ 05/01/2019 ในโซนเวลา GMT +12:00 ทั้งสองอย่างอ้างอิงถึงช่วงเวลาเดียวกัน ไม่ใช่วันที่เฉพาะ 

[![GMT ของหน้าผู้ปฏิบัติงาน](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>ข้อมูลวันที่และเวลาในกรอบงานการจัดการข้อมูล, Excel, Dataverse, and Power BI 

การรายงาน The Data Management Framework (DMF) Excel Add-In Dataverse และ Power BI ทั้งหมดได้รับการออกแบบมาเพื่อโต้ตอบกับข้อมูลในระดับฐานข้อมูลโดยตรง เนื่องจากไม่มีไคลเอนต์ที่จะปรับปรุงข้อมูล **วันที่และเวลา** ไปยังโซนเวลาของผู้ใช้ ค่า **วันที่และเวลา** ทั้งหมดจะเป็น UTC ซึ่งอาจทำให้เกิดข้อสมมติฐานบางอย่างที่ไม่ถูกต้องเมื่อป้อนหรือดูข้อมูล
 
เมื่อข้อมูล **วันที่และเวลา** ที่ถูกส่งผ่าน DMF Excel หรือ Dataverse จะถูกคาดว่าเป็น UTC โดยฐานข้อมูล อย่างไรก็ตาม หากผู้ใช้ที่ดูข้อมูลไม่มีโซนเวลาของผู้ใช้ที่ตั้งค่าเป็น UTC ค่า **วันที่และเวลา** ที่ส่งจะไม่ปรากฏตามที่คาดไว้ และผู้ใช้อาจสับสน 
 
สิ่งเดียวกันอาจเกิดขึ้นในทางกลับกันเมื่อมีการส่งออกข้อมูล ข้อมูล **วันที่และเวลา** ในเอนทิตี้ DMF ที่ส่งออกอาจแตกต่างจากที่แสดงอยู่ในไคลเอนต์ Dynamics 
 
เมื่อใช้แหล่งข้อมูลภายนอกอย่าง DMF เพื่อดูหรือเขียนข้อมูล จะต้องคำนึงถึงว่าค่า **วันที่และเวลา** ถูกพิจารณาเป็นค่าเริ่มต้นเป็น UTC โดยไม่คำนึงถึงโซนเวลาของคอมพิวเตอร์ของผู้ใช้หรือการตั้งค่าโซนเวลาของผู้ใช้ปัจจุบัน 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>ตัวอย่างของเรกคอร์ดชนิดเดียวกันที่แสดงอยู่ในพื้นที่ผลิตภัณฑ์ที่แตกต่างกัน 

**ทรัพยากรบุคคลกับโซนเวลาของผู้ใช้ตั้งค่าเป็น UTC**

[![หน้าผู้ปฏิบัติงานที่ตั้งค่าเป็น UTC](./media/worker-form3.png)](./media/worker-form3.png)

**ทรัพยากรบุคคลกับโซนเวลาของผู้ใช้ตั้งค่าเป็น GMT+12:00** 

[![หน้าผู้ปฏิบัติงานที่ตั้งค่าเป็น GMT](./media/worker-form4.png)](./media/worker-form4.png)

**Excel ผ่าน OData**

[![Excel ผ่าน OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**การแบ่งระยะ DMF**

[![การแบ่งระยะ DMF](./media/DMFStaging.png)](./media/DMFStaging.png)

**ส่งออก DMF**

[![การส่งออก DMF](./media/DMFExport.png)](./media/DMFExport.png)

**Excel ผ่าน Dataverse**

[![Excel ผ่าน Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ข้อมูลวันที่และเวลา](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[โซนเวลาที่ผู้ใช้ต้องการ](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
