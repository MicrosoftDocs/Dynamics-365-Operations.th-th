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
ms.openlocfilehash: 054d62e2ff094aee987f8c6e04e2f2e173da633d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068774"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

เมื่อต้องการตั้งค่าคอนฟิกกิจกรรมคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์

กิจกรรมคู่ขนานประกอบด้วยสาขาลำดับงานที่เรียกใช้พร้อมกัน

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
    > ลำดับของสาขาไม่สำคัญ เพราะสาขาทั้งหมดของกิจกรรมคู่ขนานเรียกใช้พร้อมกัน

3. การตั้งค่าคอนฟิกแต่ละสาขา ดูที่ [ตั้งค่าคอนฟิกสาขาคู่ขนานในเวิร์กโฟลว์](configure-parallel-branch-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]