---
title: ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน
description: เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d23e981526fd17a3cb856fffcc39e76cf24da68
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797712"
---
# <a name="configure-parallel-branches-in-a-workflow"></a>ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน

[!include [banner](../includes/banner.md)]

เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์

โดยพื้นฐานสาขาคู่ขนานคือลำดับงานที่รันในบริบทของลำดับงานหลัก

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
