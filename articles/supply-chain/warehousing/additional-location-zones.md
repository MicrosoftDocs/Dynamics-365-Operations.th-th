---
title: โซนเวลาของสถานที่เพิ่มเติม
description: หัวข้อนี้แสดงภาพรวมของโซนเวลาของสถานที่ใหม่ที่มีการเพิ่มลงใน Microsoft Dynamics 365 Supply Chain Management
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438849"
---
# <a name="additional-location-zones"></a>โซนเวลาของสถานที่เพิ่มเติม

[!include [banner](../includes/banner.md)]

ฟิลด์โซนเวลาใหม่สามฟิลด์พร้อมใช้งานใน Microsoft Dynamics 365 Supply Chain Management ผู้จัดการคลังสินค้าสามารถใช้เพื่อกำหนดองค์กรหรือโครงร่างของคลังสินค้าเพิ่มเติม สามารถตั้งฟิลด์โซนเวลาใหม่ด้วยตนเอง หรือโดยใช้วิซาร์ด **การตั้งค่าสถานที่** สามารถใช้ได้ในการสอบถามหรือการกรองข้อมูลที่ใช้ตารางสถานที่ตั้ง

ไม่จำเป็นต้องมีการตั้งค่าเพิ่มเติมสำหรับการใช้ฟิลด์โซนเวลา

## <a name="turn-on-the-additional-location-zone-feature"></a>เปิดคุณลักษณะโซนเวลาสถานที่เพิ่มเติม

ก่อนที่คุณจะสามารถใช้คุณลักษณะ *โซนเวลาสถานที่เพิ่มเติม* จะต้องมีการเปิดอยู่ในระบบของคุณ ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *โซนเวลาสถานที่เพิ่มเติม*

## <a name="use-location-zones"></a>ใช้โซนเวลาสถานที่

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> วิซาร์ดการตั้งค่าสถานที่**
2. ตั้งค่าดังต่อไปนี้:

    - ในฟิลด์  **คลังสินค้า** เลือก _62_
    - ในฟิลด์ **รหัสโซน** ให้เลือก _FLOOR_
    - ในฟิลด์ **โซนเวลาเพิ่มเติม 1** ให้เลือก _PICKZONE1_
    - ในฟิลด์ **โซนเวลาเพิ่มเติม 2** ให้เลือก _WEBSHOP1_
    - ในฟิลด์ **รหัสโพรไฟล์สถานที่** ให้เลือก _FLOOR_

3. เลือกรายการ **ชั้น**
4. ในฟิลด์ **จากหมายเลข** ให้ป้อน _1_ ในฟิลด์ **ไปยังหมายเลข** ให้ป้อน _3_
5. เลือกรายการ **ที่เก็บ**
6. ในฟิลด์ **จากหมายเลข** ให้ป้อน _1_ ในฟิลด์ **ไปยังหมายเลข** ให้ป้อน _5_
7. เลือก **สร้าง**
8. คุณได้รับข้อความแจ้งว่ามีการเพิ่มสถานที่ตั้งใหม่แล้ว เลือกปุ่ม **แสดงข้อความ** เพื่อดูข้อความ
9. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คลังสินค้า \> สถานที่** สถานที่ใหม่จะปรากฏในรายการและฟิลด์โซนเวลาทั้งหมดจะพร้อมใช้งาน (นั่นคือฟิลด์โซนเวลาที่มีอยู่และฟิลด์โซนเวลาเพิ่มเติมใหม่)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]