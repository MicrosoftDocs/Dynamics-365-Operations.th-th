---
title: โซนเวลาของสถานที่เพิ่มเติม
description: บทความนี้แสดงภาพรวมของโซนเวลาของสถานที่ใหม่ที่มีการเพิ่มลงใน Microsoft Dynamics 365 Supply Chain Management
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c20225cfb3c44fff955d0ad4e96c7fecf0ddf715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900664"
---
# <a name="additional-location-zones"></a>โซนเวลาของสถานที่เพิ่มเติม

[!include [banner](../includes/banner.md)]

ฟิลด์โซนเวลาใหม่สามฟิลด์พร้อมใช้งานใน Microsoft Dynamics 365 Supply Chain Management ผู้จัดการคลังสินค้าสามารถใช้เพื่อกำหนดองค์กรหรือโครงร่างของคลังสินค้าเพิ่มเติม สามารถตั้งฟิลด์โซนเวลาใหม่ด้วยตนเอง หรือโดยใช้วิซาร์ด **การตั้งค่าสถานที่** สามารถใช้ได้ในการสอบถามหรือการกรองข้อมูลที่ใช้ตารางสถานที่ตั้ง

ไม่จำเป็นต้องมีการตั้งค่าเพิ่มเติมสำหรับการใช้ฟิลด์โซนเวลา

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะโซนเวลาที่ตั้งเพิ่มเติม

(เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.25 คุณลักษณะนี้จะเปิดตามค่าเริ่มต้น) ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *โซนเวลาที่ตั้งเพิ่มเติม* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

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