---
title: ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน
description: เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7dac62abe080ac362abc3456a7760bbd3f790fd
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066504"
---
# <a name="configure-parallel-branches-in-a-workflow"></a>ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์

โดยพื้นฐานสาขาคู่ขนานคือลำดับงานที่เรียกใช้ในบริบทของลำดับงานหลัก

## <a name="name-a-branch"></a>ชื่อสาขา

ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับสาขาคู่ขนาน

1. คลิกขวาที่สาขาคู่ขนาน แล้วคลิก **คุณสมบัติ** ปิดใช้งานแบบฟอร์ม **คุณสมบัติ** แล้ว
2. ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**
3. ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับสาขาคู่ขนาน
4. คลิก **ปิด**

## <a name="design-and-configure-the-elements-of-a-branch"></a>ออกแบบและตั้งค่าคอนฟิกองค์ประกอบของสาขา

ทำตามขั้นตอนเหล่านี้เพื่อออกแบบตั้งค่าคอนฟิกองค์ประกอบของสาขาคู่ขนาน

1. ดับเบิลคลิกที่สาขาคู่ขนาน
2. ลากองค์ประกอบลำดับงานบนผืนผ้าใบ แล้วตั้งค่าคอนฟิกองค์ประกอบ เช่นเดียวกับการสร้างลำดับงานอื่น สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างภาพรวมลำดับงาน](create-workflow.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการสร้างลำดับงาน](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]