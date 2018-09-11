--- 
title: "สร้างผลิตภัณฑ์ใหม่"
description: "งานนี้แสดงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่ "
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 56ce5d965952d0cb41278915e4631ae9d920f5f9
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-product"></a>สร้างผลิตภัณฑ์ใหม่

[!include [task guide banner](../../includes/task-guide-banner.md)]

งานนี้แสดงวิธีการสร้างผลิตภัณฑ์ที่ใช้ร่วมกันใหม่  ซึ่งมักจะถูกดำเนินการโดยผู้ออกแบบผลิตภัณฑ์  ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF

1. ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์

## <a name="create-a-product"></a>สร้างผลิตภัณฑ์
1. คลิก สร้าง
2. ในฟิลด์หมายเลขผลิตภัณฑ์ ให้พิมพ์ค่า
    * ถ้าลำดับหมายเลขไม่ได้ถูกตั้งค่าสำหรับหมายเลขผลิตภัณฑ์ ต้องมีการป้อนด้วยตนเอง  
3. ในฟิลด์ชื่อผลิตภัณฑ์ ให้พิมพ์ค่า
    * ชื่อผลิตภัณฑ์เป็นค่าเริ่มต้นที่ใช้เป็นชื่อค้นหา  คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น  
4. คลิก ตกลง

## <a name="set-up-dimension-groups"></a>ตั้งค่ากลุ่มมิติ
1. คลิกกลุ่มมิติเพื่อเปิดกล่องโต้ตอบการวาง
2. ในฟิลด์กลุ่มแบบจำลองมิติการจัดเก็บ ให้ป้อนหรือเลือกค่า
    * กลุ่มมิติการจัดเก็บจะกำหนดว่า มิติการจัดเก็บใดที่คุณต้องป้อนในแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการติดตามในสินค้าคงคลัง  
3. ในฟิลด์กลุ่มมิติการติดตาม ให้ป้อนหรือเลือกค่า
    * กลุ่มมิติการติดตามจะกำหนดว่า มิติการติดตามใดที่คุณต้องป้อนสำหรับแต่ละธุรกรรมสำหรับผลิตภัณฑ์ และวิธีการจัดการในสินค้าคงคลัง  
4. คลิก ตกลง


