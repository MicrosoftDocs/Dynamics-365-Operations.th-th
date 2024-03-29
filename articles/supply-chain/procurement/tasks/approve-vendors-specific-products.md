---
title: อนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ
description: 'กระบวนงานนี้แสดงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ '
author: GalynaFedorova
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5092012f27dd03343410d30d15cae11ad20ce052
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670173"
---
# <a name="approve-vendors-for-specific-products"></a>อนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ  ซึ่งจะช่วยให้คุณสามารถควบคุมว่าสามารถใช้ผู้จัดจำหน่ายใดเมื่อมีการเพิ่มผลิตภัณฑ์ลงในใบสั่งซื้อ คุณสามารถใช้กระบวนงานนี้ในข้อมูลสาธิตของบริษัท USMF หรือข้อมูลของคุณเอง ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า โดยทั่วไป งานนี้จะถูกดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ

1. ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ขยายแท็บด่วน **ซื้อ** ถ้ามีผู้จัดจำหน่ายหลักแสดงอยู่ในฟิลด์ **ผู้จัดจำหน่าย** จากนั้น คุณต้องเพิ่มผู้จัดจำหน่ายนี้ให้เป็นผู้จัดจำหน่ายที่ได้รับอนุมัติในขั้นตอนต่อไปนี้ จดบันทึกหมายเลขผู้จัดจำหน่าย ถ้ามีการแสดงขึ้น  
5. บนบานหน้าต่างการดำเนินการ คลิก **ซื้อ**
6. คลิก **การตั้งค่า**
7. คลิก **เพิ่ม**
8. ในฟิลด์ผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง เลือกผู้จัดจำหน่ายที่ได้รับอนุมัติ  ต้องมีอย่างน้อยหนึ่งบรรทัดที่มีผู้จัดจำหน่ายหลักถ้ามีผู้จัดจำหน่ายหลักอยู่ในเรกคอร์ดผลิตภัณฑ์ ถ้าคุณจดบันทึกหมายเลขผู้จัดจำหน่ายไว้ก่อนหน้า ให้เลือกที่นี่  
9. ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่ เลือกวันที่ที่ล่วงหน้าหลายเดือน  
10. คลิก **เพิ่ม**
11. ในฟิลด์ **ผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
12. ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่ เลือกวันที่ที่แตกต่างจากวันหมดอายุก่อนหน้า  
13. ปิดหน้า
14. บนบานหน้าต่างการดำเนินการ คลิก **ผู้จัดจำหน่ายที่ได้รับอนุมัติ**
15. ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่ วันที่นี้ทำหน้าที่เป็นตัวกรอง ดังนั้นคุณสามารถดูว่าใครคือผู้จัดจำหน่ายที่ได้รับอนุมัติ ถึงวันที่หนึ่งๆ  
16. ปิดหน้า
17. บนบานหน้าต่างการดำเนินการ คลิก **รอบระยะเวลาที่บังคับใช้**
18. ในฟิลด์ **แสดงผู้จัดจำหน่ายที่หมดอายุตาม** ให้ป้อนวันที่ คุณสามารถใช้หน้านี้เพื่อระบุผู้จัดจำหน่าย ที่สถานะการอนุมัติจะหมดอายุหลังจากวันที่หนึ่งๆ  
19. ปิดหน้า
20. คลิก **แก้ไข**
21. ในฟิลด์ **วิธีตรวจสอบผู้จัดจำหน่ายที่ได้รับอนุมัติ** ให้เลือกหนึ่งตัวเลือก ฟิลด์นี้อนุญาตให้คุณเลือกนโยบายสำหรับสิ่งที่ควรเกิดขึ้น หากผลิตภัณฑ์ถูกเพิ่มไปยังรายการใบสั่งซื้อ ที่ผู้จัดจำหน่ายไม่ใช่ผู้จัดจำหน่ายที่ได้รับอนุมัติ  
22. คลิก **บันทึก**
23. ปิดหน้า
24. ปิดหน้า
25. ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ความสัมพันธ์ของผู้จัดจำหน่าย/สินค้า > รายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติตามสินค้า** หน้านี้แสดงภาพรวมของผลิตภัณฑ์และผู้จัดจำหน่ายที่ได้รับอนุมัติทั้งหมด  
26. ปิดหน้า
27. ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด** คุณยังสามารถเริ่มต้นจากผู้จัดจำหน่าย แล้วไปที่รายการของผลิตภัณฑ์ที่ได้รับอนุมัติสำหรับบัญชีผู้จัดจำหน่ายนั้น  
28. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
29. บนบานหน้าต่างการดำเนินการ คลิก **การจัดซื้อ**
30. คลิก **รายชื่อผู้จัดจำหน่ายที่ได้รับอนุมัติตามผู้จัดจำหน่าย**
31. ปิดหน้า
32. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]