--- 
title: "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของการรายงานทางอิเล็กทรอนิกส์ (ER)"
description: "ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) "
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a>สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่ของการรายงานทางอิเล็กทรอนิกส์ (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER)  การตั้งค่าคอนฟิก ER แต่ละครั้ง จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก  ในตัวอย่างนี้ คุณจะสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถได้ในบริษัทอื่นใด ในฐานะตัวให้บริการการตั้งค่าคอนฟิก ER ที่ใช้ร่วมกันระหว่างบริษัททั้งหมด


## <a name="create-a-provider"></a>สร้างผู้ให้บริการ
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. คลิก ผู้ให้บริการการตั้งค่าคอนฟิก
3. คลิก สร้าง
    * เรกคอร์ดของผู้ให้บริการมีชื่อและ URL ที่ไม่ซ้ำกัน  ตรวจทวนเนื้อหาของหน้านี้ และข้ามขั้นตอนนี้ถ้าเรกคอร์ดสำหรับ Litware, Inc. (http://www.litware.com) มีอยู่แล้ว  
4. ในฟิลด์ชื่อ พิมพ์ 'Litware, Inc.'
    * Litware, inc  
5. ในฟิลด์ที่อยู่อินเทอร์เน็ต พิมพ์ 'http://www.litware.com'
    * http://www.litware.com  
6. คลิก บันทึก
7. ปิดหน้า

## <a name="select-as-an-active-provider"></a>เลือกเป็นผู้ให้บริการที่ใช้งานอยู่
1. เลือกผู้ให้บริการ Litware, Inc.
2. คลิก กำหนดเป็นใช้งานอยู่


