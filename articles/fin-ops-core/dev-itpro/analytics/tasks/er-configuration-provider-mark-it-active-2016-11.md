---
title: สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายว่าใช้งานอยู่
description: บทความนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์ สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิก
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93c2e114c97290347b71e94d87ea5339688791cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883609"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายว่าใช้งานอยู่

[!include [banner](../../includes/banner.md)]

บทความนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์ สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) การตั้งค่าคอนฟิก ER แต่ละครั้ง จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก  ในตัวอย่างนี้ คุณจะสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถได้ในบริษัทอื่นใด ในฐานะตัวให้บริการการตั้งค่าคอนฟิก ER ที่ใช้ร่วมกันระหว่างบริษัททั้งหมด

## <a name="create-a-provider"></a>สร้างผู้ให้บริการ
1. ไปที่ **บานหน้าต่างนำทาง** ในมุมบนซ้าย และเลือก **การจัดการองค์กร**
2. ไปที่ **พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**
3. ไปที่ **ลิงค์ที่เกี่ยวข้อง > ตัวให้บริการการตั้งค่าคอนฟิก**
4. เลือก **ใหม่**
    - เรกคอร์ดของผู้ให้บริการมีชื่อและ URL ที่ไม่ซ้ำกัน  ตรวจทานเนื้อหาของหน้านี้ และข้ามกระบวนงานนี้ ถ้าเรกคอร์ดสำหรับ Litware, Inc. (https://www.litware.com) มีอยู่แล้ว  
5. ในฟิลด์ชื่อ ให้พิมพ์ `Litware, Inc.`
6. ในฟิลด์ที่อยู่อินเทอร์เน็ต ให้พิมพ์ `https://www.litware.com`
7. เลือก **บันทึก**
8. ปิดหน้า

## <a name="select-as-an-active-provider"></a>เลือกเป็นผู้ให้บริการที่ใช้งานอยู่
1. เลือกผู้ให้บริการ Litware, Inc.
2. เลือก **กำหนดเป็นใช้งานอยู่**

![พื้นที่ทำงานการรายงานทางอิเล็กทรอนิกส์](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]