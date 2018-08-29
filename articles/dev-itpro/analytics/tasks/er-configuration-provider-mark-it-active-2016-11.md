--- 
title: "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"
description: "ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) "
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่

[!include [task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนต่อไปนี้จะอธิบายวิธีที่ผู้ใช้ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนารายงานอิเล็กทรอนิกส์ที่สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER)  การตั้งค่าคอนฟิก ER แต่ละครั้ง จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก  ในตัวอย่างนี้ คุณจะสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถได้ในบริษัทอื่นใด ในฐานะตัวให้บริการการตั้งค่าคอนฟิก ER ที่ใช้ร่วมกันระหว่างบริษัททั้งหมด


## <a name="create-a-provider"></a>สร้างผู้ให้บริการ
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. คลิก ผู้ให้บริการการตั้งค่าคอนฟิก
3. คลิก สร้าง
    * เรกคอร์ดของผู้ให้บริการมีชื่อและ URL ที่ไม่ซ้ำกัน  ตรวจทานเนื้อหาของหน้านี้ และข้ามกระบวนงานนี้ ถ้าเรกคอร์ดสำหรับ Litware, Inc. (`http://www.litware.com`) มีอยู่แล้ว  
4. ในฟิลด์ชื่อ พิมพ์ 'Litware, Inc.'
    * Litware, inc  
5. ในฟิลด์ที่อยู่อินเทอร์เน็ต ให้พิมพ์ `http://www.litware.com`
6. คลิก บันทึก
7. ปิดหน้า

## <a name="select-as-an-active-provider"></a>เลือกเป็นผู้ให้บริการที่ใช้งานอยู่
1. เลือกผู้ให้บริการ Litware, Inc.
2. คลิก กำหนดเป็นใช้งานอยู่


