---
title: ตั้งค่านโยบายงานของคลังสินค้า (ใบสมัคร พฤษภาคม 2016)
description: กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca54cceb83425c43b5d124cd6d11be0cdef4d63a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145927"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a>ตั้งค่านโยบายงานของคลังสินค้า (ใบสมัคร พฤษภาคม 2016)

[!include [banner](../../includes/banner.md)]

กระบวนการคลังสินค้าไม่รวมงานคลังสินค้าเสมอไป โดยการกำหนดนโยบายงาน คุณสามารถป้องกันการสร้างงานสำหรับการเบิกวัตถุดิบและการสำรองสินค้าสำเร็จรูป สำหรับชุดของผลิตภัณฑ์ที่ตำแหน่งเฉพาะได้ บริษัทข้อมูลสาธิต USMF ถูกนำมาใช้เพื่อสร้างการบันทึกนี้ คำแนะนำงานนี้ต้องการแอพลิเคชัน Dynamics AX 7.0.1 หรือใหม่กว่า

1. ไปที่การจัดการคลังสินค้า > ตั้งค่า > งาน > นโยบายงาน
2. คลิก สร้าง
3. ในฟิลด์ชื่อนโยบายงาน ให้พิมพ์ 'ไม่มีงานการย้ายเก็บ'
4. คลิก บันทึก
5. คลิก เพิ่ม
6. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
7. ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองสินค้าที่สำเร็จแล้ว'
8. คลิก เพิ่ม
9. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
10. ในฟิลด์ชนิดใบสั่งงาน ให้เลือก 'การสำรองผลิตภัณฑ์ร่วมและสินค้าพลอยได้'
11. ขยายส่วนสถานที่เก็บสินค้าคงคลัง
12. คลิก เพิ่ม
13. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
14. ในรายการคลังสินค้า ป้อน '51'
15. ในฟิลด์สถานที่ ให้ป้อนหรือเลือก '001'
16. ขยายส่วนผลิตภัณฑ์
17. ในฟิลด์การเลือกผลิตภัณฑ์ ให้ป้อน 'เลือกแล้ว'
18. คลิก เพิ่ม
19. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
20. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือก 'L0101'
21. คลิก บันทึก

