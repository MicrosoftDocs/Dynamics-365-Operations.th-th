---
title: ทำงานร่วมกับผู้จัดจำหน่ายที่ใช้พอร์ทัลผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีที่เจ้าหน้าที่จัดซื้อสามารถใช้พอร์ทัลผู้จัดจำหน่ายเพื่อร่วมมือกับผู้จัดจำหน่ายภายนอกในระหว่างกระบวนการยืนยันใบสั่งซื้อ ข้อมูลนี้ใช้กับเฉพาะรุ่นกุมภาพันธ์ 2016 &amp; พฤษภาคม 2016 ของ Dynamics AX
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aece4fd621be803abe5011e40785f6a3301924f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019114"
---
# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>ทำงานร่วมกับผู้จัดจำหน่ายที่ใช้พอร์ทัลผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีที่เจ้าหน้าที่จัดซื้อสามารถใช้พอร์ทัลผู้จัดจำหน่ายเพื่อร่วมมือกับผู้จัดจำหน่ายภายนอกในระหว่างกระบวนการยืนยันใบสั่งซื้อ ข้อมูลนี้ใช้กับเฉพาะรุ่นกุมภาพันธ์ 2016 และ พฤษภาคม 2016 ของ Dynamics AX

ข้อมูลในหัวข้อนี้ใช้กับเฉพาะรุ่นกุมภาพันธ์ 2016 และพฤษภาคม 2016 ของ Dynamics AX สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันการทำงานร่วมกันกับผู้จัดจำหน่ายใหม่ ดู [การทำงานร่วมกันกับผู้จัดจำหน่ายกับผู้จัดจำหน่ายภายนอก](vendor-collaboration-work-external-vendors.md)  

พอร์ทัลผู้จัดจำหน่ายมีเป้าหมายเป็นผู้จัดจำหน่ายที่ไม่มีการรวมการแลกเปลี่ยนข้อมูลอิเล็กทรอนิกส์ (EDI) กับ Microsoft Dynamics AX สำหรับการแลกเปลี่ยนข้อมูลใบสั่งซื้อ (PO) พอร์ทัลอนุญาตให้ตัวแทนฝ่ายจัดซื้อสามารถส่ง PO ไปยังผู้จัดจำหน่าย และจากนั้นรับการตอบสนองที่ยืนยันหรือปฏิเสธใน Dynamics AX  

สามารถตั้งค่าคอนฟิกกระบวนการเพื่อให้การยืนยันจากผู้จัดจำหน่ายยืนยันใบสั่งโดยอัตโนมัติ ในกรณีนี้ การติดตามจำเป็นเพียงบางโอกาส เมื่อใบสั่งถูกปฏิเสธหรือถ้าใบรับรองของผู้จัดจำหน่ายถูกลงทะเบียนเป็นการตอบสนอง แต่สถานะของใบสั่งซื้อไม่ถูกอัพเดตเป็น **ยืนยันแล้ว** เนื่องจากปัญหาในกระบวนการยืนยัน

## <a name="po-confirmation-and-rejection"></a>การยืนยันและปฏิเสธใบสั่งซื้อ
มีการจัดเตรียม PO ใน Dynamics AX เมื่อคุณมีใบสั่งซื้อมีสถานะเป็น **อนุมัติ** คุณส่งไปยังผู้ขาย โดยการสร้างคำขอการยืนยัน ถ้าคุณต้องการดึงความสนใจของผู้จัดจำหน่ายไปยังใบสั่งซื้อใหม่ คุณยังสามารถใช้ระบบการจัดการการพิมพ์เพื่อส่งใบสั่งซื้อทางอีเมล ใบสั่งซื้อปรากฏขึ้นในพอร์ทัลของผู้จัดจำหน่าย และรวมถึงตัวเลือกสำหรับผู้จัดจำหน่ายเพื่อใช้ยืนยันหรือปฏิเสธ ผู้จัดจำหน่ายยังสามารถเพิ่มข้อคิดเห็นในการสื่อสารข้อมูลเช่นการเปลี่ยนแปลงใบสั่งซื้อ  

ในเว็บไซต์ของผู้จัดจำหน่าย ผู้จัดจำหน่ายสามารถดูบรรทัดใบสั่ง รายการเหล่านี้รวมถึงรายละเอียดเช่นหมายเลขสินค้าภายนอก มิติ ข้อมูลราคา ปริมาณ วันจัดส่ง และที่อยู่จัดส่ง ผู้จัดจำหน่ายสามารถสร้างรายงานที่แสดงข้อมูลใบสั่งซื้อ และยังแสดงราคารวมได้ด้วยเช่นกัน ค่าธรรมเนียมที่เกี่ยวข้องกับผู้จัดจำหน่ายจะแสดงถ้าผู้จัดจำหน่ายคลิกปุ่ม **ค่าธรรมเนียม** ในหัวข้อหรือบรรทัด ผู้จัดจำหน่ายสามารถนำเข้าข้อมูลในใบสั่งซื้อเข้าในระบบของตนเอง โดยใช้ฟังก์ชัน **ส่งออกไปที่ Excel** ได้  

ตารางต่อไปนี้แสดงอัตราแลกเปลี่ยนทั่วไปของข้อมูล โดยขึ้นอยู่กับว่าผู้จัดจำหน่ายตอบสนองอย่างไรเมื่อคุณส่งใบสั่งซื้อสำหรับใบยืนยันการขาย:

| ชนิดของการตอบรับ                                                                                                  | ผลลัพธ์                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ผู้จัดจำหน่ายยืนยันใบสั่ง ระบบถูกกำหนดค่าให้ยืนยันใบสั่งซื้อโดยอัตโนมัติเมื่อผู้จัดจำหน่ายยืนยัน    | สถานะใบสั่งจะถูกอัพเดตเป็น **ยืนยันแล้ว** ถ้ามีบางอย่างป้องกันใบสั่งจากการถูกอัพเดต จากนั้นการตอบสนองของผู้จัดจำหน่ายจะยังคงถูกเรกคอร์ดเป็น **ยืนยันแล้ว** แต่ใบสั่งซื้อที่จะยังคงอยู่ในสถานะอยู่ระหว่าง **การตรวจทานภายนอก**                                                                       |
| ผู้จัดจำหน่ายยืนยันใบสั่ง ระบบไม่ได้ถูกกำหนดค่าให้ยืนยันใบสั่งซื้อโดยอัตโนมัติเมื่อผู้จัดจำหน่ายยืนยัน | การตอบสนองของผู้จัดจำหน่ายถูกเรกคอร์ดเป็น **ยืนยันแล้ว** แต่ใบสั่งซื้อยังคงอยู่ในสถานะอยู่ระหว่าง **การตรวจทานภายนอก**                                                                                                                                                                                      |
| ผู้จัดจำหน่ายปฏิเสธใบสั่ง                                                                                     | การตอบสนองของผู้จัดจำหน่ายถูกเรกคอร์ดเป็น **ปฏิเสธแล้ว** และใบสั่งซื้อยังคงอยู่ในสถานะอยู่ระหว่าง **การตรวจทานภายนอก** การปฏิเสธจะได้รับพร้อมกับเหตุผลและคำแนะนำสำหรับการเปลี่ยนแปลง เช่นวันจัดส่งอื่น คุณปรับปรุงใบสั่งซื้อ แล้วส่งเวอร์ชันใหม่สำหรับใบยืนยันการขาย |

## <a name="changes-to-a-po"></a>การเปลี่ยนแปลงใบสั่งซื้อ
เมื่อคุณต้องการเปลี่ยนใบสั่งซื้อที่ถูกคอนเฟิร์มแล้ว คุณสามารถส่งใบสั่งซื้อใหม่ไปยังผู้จัดจำหน่ายโดยใช้พอร์ทัลผู้จัดจำหน่าย ใบสั่งซื้อใหม่จะมีคำเสริมท้ายเวอร์ชันที่บ่งชี้ว่า มีการปรับเปลี่ยนใบสั่งซื้อที่มีการอธิบายไว้ก่อนหน้านี้ พอร์ทัลผู้จัดจำหน่ายช่วยให้สามารถติดตามประวัติของใบสั่งแต่ละผู้จัดจำหน่าย ในสั่งซื้อที่ยืนยันรุ่นไว้ก่อนหน้านี้จะยังคงอยู่ในรายการของในสั่งซื้อที่ยืนยันจนกว่าจะได้รับการยืนยันใบสั่งซื้อใหม่  

เมื่อคุณยกเลิกใบสั่งซื้อ สถานะจะถูกเปลี่ยนกลับไปเป็น **อนุมัติแล้ว** คุณต้องส่งกลับไปที่ผู้จัดจำหน่ายโดยใช้พอร์ทัลผู้จัดจำหน่ายเพื่อให้ผู้จัดจำหน่ายสามารถยืนยันหรือปฏิเสธการยกเลิก หลังจากมียืนยันการยกเลิก ใบสั่งซื้อจะปรากฏในรายชื่อผู้จัดจำหน่ายของรายการใบสั่งซื้อที่ยืนยันเป็น **ยกเลิก**

## <a name="versions-status-transitions-and-change-management"></a>รุ่น การเปลี่ยนแปลงสถานะ และการจัดการการเปลี่ยนแปลง
เมื่อใบสั่งซื้อถูกส่งให้กับผู้จัดจำหน่าย จะถูกลงทะเบียนในระบบในรุ่นเฉพาะของใบสั่งซื้อ และสถานะจะเปลี่ยนจาก **อนุมัติแล้ว** เป็น **อยู่ระหว่างการตรวจทานภายนอก** ถ้าใบสั่งซื้อมีการเปลี่ยนแปลงในภายหลัง ใบสั่งซื้อรุ่นใหม่จะถูกสร้าง และสถานะจะกลับไปเป็น **อนุมัติแล้ว** (หรือ **ร่าง** ถ้าการจัดการการเปลี่ยนแปลงถูกเปิดใช้งาน)  

ตารางต่อไปนี้แสดงตัวอย่างของการเปลี่ยนแปลงในสถานะและรุ่นที่อาจพบในใบสั่งซื้อ:

| การดำเนินการ                                                   | สถานะและรุ่น                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| รุ่นเริ่มต้นของ PO ถูกสร้างใน Dynamics AX | สถานะเป็น **อนุมัติแล้ว**                                                                           |
| ใบสั่งซื้อจะถูกส่งไปยังพอร์ทัลของผู้จัดจำหน่าย                     | รุ่นจะถูกลงทะเบียนบนพอร์ทัลผู้จัดจำหน่าย และสถานะจะถูกเปลี่ยนเป็น **อยู่ระหว่างการตรวจทานภายนอก**    |
| คุณทำการเปลี่ยนแปลงบางอย่างที่ถูกร้องขอโดยผู้จัดจำหน่าย  | สถานะจะเปลี่ยนกลับไปเป็น **อนุมัติแล้ว**                                                            |
| คุณสามารถส่งใบสั่งซื้อเวอร์ชันใหม่ไปยังพอร์ทัลผู้จัดจำหน่าย | รุ่นใหม่จะถูกลงทะเบียนบนพอร์ทัลผู้จัดจำหน่าย และสถานะจะถูกเปลี่ยนเป็น **อยู่ระหว่างการตรวจทานภายนอก** |
| ผู้จัดจำหน่ายอนุมัติรุ่นใหม่ของใบสั่งซื้อ           | สถานะจะถูกเปลี่ยนเป็น **ยืนยันแล้ว**                                                                |

เพื่อดูรุ่นของใบสั่งซื้อที่ถูกส่งไปยังผู้จัดจำหน่ายและการตอบสนองของผู้จัดจำหน่าย คลิก **สมุดรายวัน** &gt; **การยืนยันคำร้องขอ** จากใบสั่งซื้อ  

ใบสั่งที่ถูกส่งไปยังผู้จัดจำหน่ายเพื่อการตอบสนอง และมีสถานะเป็น **อยู่ระหว่างการตรวจทานภายนอก** จะปรากฏขึ้นในรายการ **ใบสั่งซื้อถูกส่งไปยังพอร์ทัลของผู้จัดจำหน่ายแล้ว กำลังรอการตอบสนอง** หรือรายการ **ใบสั่งซื้อที่ถูกส่งไปยังพอร์ทัลของผู้จัดจำหน่าย ร้องขอการตอบสนองสำหรับการดำเนินการ** เมื่อคุณเปลี่ยนแปลงใบสั่งที่ถูกส่งไปยังผู้จัดจำหน่ายแล้ว เพื่อให้สถานะเปลี่ยนกลับเป็น **อนุมัติแล้ว** จะไม่ปรากฏในรายการเหล่านี้ เมื่อต้องการดูว่าก่อนหน้านี้มีการตอบสนองใบสั่งจากผู้จัดจำหน่ายหรือไม่ คลิก **สมุดรายวัน** &gt; **ยืนยันคำขอ**  

ผู้จัดจำหน่ายที่ไม่มีการยืนยันใบสั่งซื้อในพอร์ทัลของผู้จัดจำหน่าย พวกเขาสามารถส่งข้อความอีเมล หรือการสื่อสารการยอมรับใบสั่งซื้อผ่านช่องทางอื่นๆ ของพวกเขา จากนั้น คุณสามารถยืนยันใบสั่งใน Dynamics AX ได้ด้วยตนเอง ในกรณีนี้ คุณจะได้รับคำเตือนว่าใบสั่งมีการยืนยันแม้ว่าจะไม่มีการตอบสนองใดๆ จากผู้จัดจำหน่าย จากนั้นใบสั่งซื้อจะแสดงในประวัติการยืนยันในพอร์ทัลของผู้จัดจำหน่ายเป็นการยืนยันใบสั่งที่เปิดที่ไม่มีคำตอบใดๆ นอกจากนี้ ผู้จัดจำหน่ายจะไม่มีตัวเลือกที่จะยืนยันหรือปฏิเสธใบสั่งซื้อ  

**หมายเหตุ:** รุ่นของ PO ที่พร้อมใช้งานสำหรับกระบวนการอื่นๆ ใน Dynamics AX เป็นรุ่นล่าสุดเสมอ ถึงแม้ว่ารุ่นนั้นจะยังไม่ได้ลงทะเบียน

### <a name="change-management"></a>การจัดการการเปลี่ยนแปลง

ถ้าคุณเปิดใช้งานการจัดการการเปลี่ยนแปลงสำหรับใบสั่งซื้อ ใบสั่งซื้อจะส่งผ่านลำดับงานการอนุมัติเพื่อเข้าถึงสถานะ **อนุมัติ** กระบวนการนี้ไม่สามารถมองเห็นได้โดยผู้จัดจำหน่าย  

เมื่อการจัดการการเปลี่ยนแปลงเปิดอยู่สำหรับใบสั่งซื้อ เวอร์ชันจะลงทะเบียนเมื่อใบสั่งซื้อได้รับอนุมัติ ไม่ใช่เมื่อมีการส่งไปยังผู้จัดจำหน่าย หรือยืนยันใบสั่งซื้อ  

ตารางต่อไปนี้แสดงตัวอย่างของการเปลี่ยนแปลงในสถานะและรุ่นที่อาจพบในใบสั่งซื้อเมื่อการจัดการการเปลี่ยนแปลงถูกเปิดใช้งาน


|                                                    การดำเนินการ                                                     |                                                                                                                                                                                                                      สถานะและรุ่น                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           รุ่นเริ่มต้นของ PO ถูกสร้างใน Dynamics AX                            |                                                                                                                                                                                                            สถานะเป็น <strong>ร่าง</strong>                                                                                                                                                                                                             |
| ใบสั่งซื้อถูกส่งไปที่กระบวนการอนุมัติอีกครั้ง (นี่คือกระบวนการภายในที่ไม่ได้เกี่ยวข้องกับผู้จัดจำหน่าย) |                                                                                                                        เปลี่ยนสถานะจาก <strong>ร่าง</strong> เป็น <strong>ระหว่างการตรวจทาน</strong> เป็น <strong>อนุมัติ</strong> ถ้าใบสั่งซื้อไม่ถูกปฏิเสธในระหว่างกระบวนการอนุมัติ ใบสั่งซื้อที่อนุมัติแล้วถูกลงทะเบียนเป็นรุ่น                                                                                                                        |
|                                      ใบสั่งซื้อจะถูกส่งไปยังพอร์ทัลของผู้จัดจำหน่าย                                      |                                                                                                                                                                      รุ่นจะถูกลงทะเบียนในพอร์ทัลผู้จัดจำหน่าย และสถานะจะถูกเปลี่ยนเป็น <strong>อยู่ระหว่างการตรวจทานภายนอก</strong>                                                                                                                                                                       |
|                            คุณทำการเปลี่ยนแปลงบางอย่างที่ถูกร้องขอโดยผู้จัดจำหน่าย                            |                                                                                                                                                                                                    สถานะจะเปลี่ยนกลับไปเป็น <strong>ร่าง</strong>                                                                                                                                                                                                     |
|                              ใบสั่งซื้อถูกส่งไปที่กระบวนการอนุมัติอีกครั้ง                               | เปลี่ยนสถานะจาก <strong>ร่าง</strong> เป็น <strong>ระหว่างการตรวจทาน</strong> เป็น <strong>อนุมัติ</strong> ถ้าใบสั่งซื้อไม่ถูกปฏิเสธในระหว่างกระบวนการอนุมัติ อีกทางหนึ่งคือ ระบบสามารถถูกตั้งค่าคอนฟิกเพื่อให้การเปลี่ยนแปลงฟิลด์เฉพาะไม่ต้องมีการอนุมัติใหม่ ในกรณีนี้ สถานะที่เปลี่ยนเริ่มจาก <strong>ร่าง</strong> และจากนั้นจะถูกอัพเดตโดยอัตโนมัติเป็น <strong>อนุมัติแล้ว</strong> ใบสั่งซื้อที่อนุมัติแล้วถูกลงทะเบียนเป็นรุ่นใหม่ |
|                           คุณสามารถส่งใบสั่งซื้อเวอร์ชันใหม่ไปยังพอร์ทัลผู้จัดจำหน่าย                            |                                                                                                                                                                    รุ่นใหม่จะถูกลงทะเบียนในพอร์ทัลผู้จัดจำหน่าย และสถานะจะถูกเปลี่ยนเป็น <strong>อยู่ระหว่างการตรวจทานภายนอก</strong>                                                                                                                                                                     |
|                                ผู้จัดจำหน่ายอนุมัติรุ่นใหม่ของใบสั่งซื้อ                                 |                                                                                                                                                     สถานะจะถูกเปลี่ยนเป็น <strong>ยืนยันแล้ว</strong> โดยอัตโนมัติ หรือเมื่อคุณได้รับการตอบสนองจากผู้จัดจำหน่ายและยืนยันใบสั่งซื้อแล้ว อย่างใดอย่างหนึ่ง                                                                                                                                                     |

<a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม
--------

[ความปลอดภัยของผู้ใช้พอร์ทัลของผู้จัดจำหน่าย](configure-security-vendor-portal-users.md)

[พื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)



