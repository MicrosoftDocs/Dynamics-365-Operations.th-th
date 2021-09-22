---
title: พบงานไม่เพียงพอสำหรับคลัสเตอร์หลังจากตั้งค่าคอนฟิกโปรไฟล์
description: ถ้าคุณตั้งค่าคอนฟิกโปรไฟล์คลัสเตอร์ คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่ามีงานไม่เพียงพอ แก้ไขโปรไฟล์และตั้งค่า เรียกใช้ตําแหน่ง เป็น ไม่
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477706"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>พบงานไม่เพียงพอสำหรับคลัสเตอร์เมื่อใช้การเบิกสินค้าคลัสเตอร์ที่ระบบโดยตรง

## <a name="symptoms"></a>อาการ

เมื่อใช้กระบวนการ *เบิกสินค้าของคลัสเตอร์โดยตรงของระบบ* ถ้าคุณตั้งค่าคอนฟิกโพรไฟล์ของคลัสเตอร์ ตัวอย่างเช่น 10 ตำแหน่ง สามารถเบิกสินค้า กระบวนการทำงานตามที่วางแผนไว้เมื่อมีการทำงานเพียงพอสำหรับการเบิกสินค้าไปยัง 10 ตำแหน่ง อย่างไรก็ตาม หากมีเพียงแปดตําแหน่งที่จะเบิกสินค้า คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้

> พบงานไม่เพียงพอสำหรับคลัสเตอร์

## <a name="resolution"></a>การแก้ปัญหา

เมื่อต้องการแก้ไขปัญหานี้ แก้ไขโพรไฟล์ของคลัสเตอร์ และตั้งค่าตัวเลือก **การเรียกใช้ตำแหน่ง** เป็น *ไม่*
