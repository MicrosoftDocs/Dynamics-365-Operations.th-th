---
title: การสร้างคลาสการผลิต
description: 'ขั้นตอนนี้แสดงวิธีการตั้งค่าคลาสงาน '
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed9b72d891df4d40213d4854da6b09bd9876effa
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438841"
---
# <a name="create-a-work-class"></a>การสร้างคลาสการผลิต

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงวิธีการตั้งค่าคลาสงาน  คลาสงานถูกใช้เพื่อกำหนดและ/หรือจำกัดชนิดของรายการใบสั่งงานที่ผู้ปฏิบัติงานคลังสินค้าสามารถประมวลผลบนอุปกรณ์เคลื่อนที่  รายการที่ผู้ปฏิบัติงานสามารถประมวลผลจะถูกกำหนดจากคลาสงานบนรายการเมนูอุปกรณ์เคลื่อนที่ที่ผู้ปฏิบัติงานคลังสินค้ามีการเข้าถึงและคลาสงานที่ระบุไว้ในรายการงาน คลาสงานสามารถใช้เพื่อตรวจสอบสถานที่ส่งสินค้าสำหรับรายการใบสั่งงาน คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า

1. ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > คลาสงาน
2. คลิก สร้าง
3. ในฟิลด์รหัสคลาสงาน ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
5. ในฟิลด์ชนิดใบสั่งงาน ให้เลือกตัวเลือก
6. คลิก สร้าง
7. ในฟิลด์ชนิดสถานที่ ให้พิมพ์ค่าใดค่าหนึ่ง
    * ถ้าคุณเลือกชนิดสถานที่ นี่จะตั้งค่าข้อจำกัดสำหรับสถานที่ที่สามารถจัดเก็บสินค้าหลังจากที่ได้เบิกสินค้าไป การตั้งค่านี้จะใช้เมื่อคำสั่งสถานที่พยายามแก้ไขที่ตั้ง หรือถ้าผู้ปฏิบัติงานคลังสินค้าระบุสถานที่จัดเก็บสินค้าในอุปกรณ์เคลื่อนที่ด้วยตนเอง  
8. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]