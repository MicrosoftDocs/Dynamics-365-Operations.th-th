---
title: ตั้งค่ารอบระยะเวลาการชำระภาษีขาย
description: หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระภาษีขายใน Dynamics 365 Finance
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8683f3b6e10efe6e975ae6bc3d7863f884bb9a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994476"
---
# <a name="set-up-sales-tax-settlement-periods"></a>ตั้งค่ารอบระยะเวลาการชำระภาษีขาย

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระภาษีขาย รอบระยะเวลาการจ่ายภาษีขาย ประกอบด้วยข้อมูลเกี่ยวกับช่วงรอบระยะเวลาสำหรับที่ภาษีขายจำเป็นต้องถูกรายงานและชำระเงิน  สามารถดำเนินการกระบวนการชำระเงินได้สำหรับรอบระยะเวลาการชำระเงินสำหรับช่วงวันที่เฉพาะ  รหัสภาษีทั้งหมดที่เชื่อมโยงกับรอบระยะเวลาการจ่ายเงินจะถูกตั้งค่า  ภาระภาษีจะถูกลงรายการบัญชีของผู้จัดจำหน่ายหรือบัญชีแยกประเภททั่วไปอย่างใดอย่างหนึ่ง ขึ้นอยู่กับการตั้งค่าของหน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้อง 

งานนี้ใช้บริษัทสาธิต USMF 

1. ในบานหน้าต่างนำทางให้ ไปที่ **โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีขาย > รอบระยะเวลาการชำระภาษีขาย**
2. เลือก **ใหม่**
3. ในฟิลด์ **ระยะเวลาการชำระเงิน** ให้พิมพ์ค่า
4. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์ **หน่วยงานจัดเก็บภาษี** ให้เลือกหน่วยงานจัดเก็บภาษีขายที่ได้รับรายงานและการชำระเงินที่สร้างขึ้นสำหรับรอบระยะเวลาการชำระเงิน
6. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
7. ในฟิลด์ **เงื่อนไขการชำระเงิน** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง หน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้องสามารถถูกตั้งค่าให้เป็นผู้จัดจำหน่ายและการชำระภาษีขายจะสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง  เงื่อนไขการชำระเงินจะกำหนดวันครบกำหนดชำระสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง  
8. เลือกชนิดสำหรับช่วงรอบระยะเวลาการชำระเงิน
9. ป้อนหมายเลขของหน่วยช่วงรอบระยะเวลาต่อรอบระยะเวลา  ตัวอย่างเช่น หนึ่งไตรมาสมี 3 เดือน
10. เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ใช้การประมวลผลชุดงานสำหรับการชำระภาษีขาย** กระบวนการชำระสำหรับรอบระยะเวลาการชำระสามารถประมวลผลเป็นชุดงานในเบื้องหลัง  ซึ่งเหมาะสำหรับธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลาหนึ่ง  
    > [!NOTE]
    > ปัจจุบันนี้ไม่มีการสนับสนุนในสเปน ญี่ปุ่น และเนเธอร์แลนด์
11. เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี** โดยค่าเริ่มต้น ระบบจะสร้างธุรกรรมออฟเซ็ตภาษีในระหว่างกระบวนการชำระเงิน ซึ่งทำให้เกิดปัญหาประสิทธิภาพการทำงาน ถ้ามีธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลา เลือกกล่องกาเครื่องหมายนี้เพื่อป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี
12. ขยายแท็บ **ช่วงรอบระยะเวลา**
13. เลือก **เพิ่ม**
14. ในฟิลด์ **วันที่เริ่มต้น** ในแถวใหม่ ป้อนวันที่
15. ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่
16. เลือก **ช่วงรอบระยะเวลาใหม่** เมื่อมีการป้อนรอบระยะเวลาแรก รอบระยะเวลาใหม่จะถูกสร้างโดยอัตโนมัติ  คุณสามารถกลับมาและเพิ่มช่วงรอบระยะเวลาใหม่ตามความต้องการ  
17. ปิดหน้า

