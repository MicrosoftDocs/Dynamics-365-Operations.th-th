---
title: ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน
description: เมื่อต้องการตั้งค่าคอนฟิกกิจกรรมคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72f07addd4856bbc61099926b0ee99b4de967e6a841de3833e72e89d4a038b55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746523"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน

[!include [banner](../includes/banner.md)]

เมื่อต้องการตั้งค่าคอนฟิกกิจกรรมคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์

กิจกรรมคู่ขนานประกอบด้วยสาขาลำดับงานที่รันพร้อมกัน

## <a name="name-a-parallel-activity"></a>กำหนดชื่อกิจกรรมคู่ขนาน

ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับกิจกรรมคู่ขนาน

1. คลิกขวาที่กิจกรรมคู่ขนาน แล้วคลิก **คุณสมบัติ** เพื่อเปิดแบบฟอร์ม **คุณสมบัติ**
2. ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**
3. ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับกิจกรรมคู่ขนาน
4. คลิก **ปิด**

## <a name="configure-the-branches-of-a-parallel-activity"></a>ตั้งค่าคอนฟิกสาขาของกิจกรรมคู่ขนาน

ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มและตั้งค่าคอนฟิกสาขาของกิจกรรมคู่ขนานนี้

1. ดับเบิลคลิกที่กิจกรรมคู่ขนานเพื่อแสดงสาขาของกิจกรรมคู่ขนาน
2. เมื่อต้องการเพิ่มสาขา ให้ลากองค์ประกอบ **สาขา** จากพื้นที่ **องค์ประกอบลำดับงาน** ไปยังจุดแทรกบนผืนผ้าใบ ภาพต่อไปนี้แสดงจุดแทรก

    ![จุดแทรก](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > ลำดับของสาขาไม่สำคัญ เพราะสาขาทั้งหมดของกิจกรรมคู่ขนานรันพร้อมกัน

3. การตั้งค่าคอนฟิกแต่ละสาขา ดูที่ [ตั้งค่าคอนฟิกสาขาคู่ขนานในเวิร์กโฟลว์](configure-parallel-branch-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]