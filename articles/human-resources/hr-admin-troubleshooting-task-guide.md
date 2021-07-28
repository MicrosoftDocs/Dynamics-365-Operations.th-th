---
title: บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ
description: บทความนี้อธิบายวิธีการบันทึกคู่มืองานไปยัง Microsoft Dynamics Lifecycle Services (LCS) และจากนั้น เล่นซ้ำ
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46532fce05b7faf15b3dc2e843dcd93a976c0da1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357276"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**รายละเอียดสภาพแวดล้อม** 

Microsoft Dynamics 365 Human Resources ซึ่งถูกปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS)

**ออก**

ลูกค้าต้องการบันทึกการบันทึกภารกิจใหม่ไปยังโครงการ LCS และจากนั้นเล่นซ้ำคู่มืองานที่บันทึกไว้

**ความละเอียด**

ทำตามขั้นตอนเหล่านี้เพื่อบันทึกการบันทึกงานไปยัง LCS

1. ลงชื่อเข้าใช้ไปยัง LCS และเลือกโครงการ
2. เลือกไทล์ **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**
3. ดูหน้าใน "ประสบการณ์ BPM ที่ปรับปรุงแล้ว"
4. เลือกไลบรารี และจากนั้น เลือก **คัดลอก**
5. ป้อนชื่อสำหรับตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM)
6. ลงชื่อเข้าใช้ทรัพยากรบุคคลจาก LCS
7. ในฟิลด์ **การค้นหา** ป้อน **วิธีใช้** วิธีใช้ Lifecycle Services ถูกเปิด
8. เลือกปุ่ม **รีเฟรช** สำหรับการตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services

    ไลบรารี BPM ใหม่ของคุณ ควรปรากฏอยู่ และควรถูกเปิดใช้งาน

9. ปิดหน้า
10. สร้างการบันทึกงาน
11. เมื่อคุณทำเสร็จสิ้น เลือก **บันทึกไปยัง Lifecycle Services**

    ![บันทึกไปยัง Lifecycle Services](media/task-guides.png)

12. เลือกไลบรารี BPM และโหนดเพื่อบันทึกการบันทึกงาน

ทำตามขั้นตอนเหล่านี้เพื่อเล่นซ้ำการบันทึกงานจาก LCS

1. เริ่มต้นตัวบันทึกงาน
2. เลือก **เปิดจาก LCS**
3. เลือกไลบรารีและโหนด BPM ที่มีคู่มืองานที่บันทึกไว้
4. เปิดคู่มืองาน


[!INCLUDE[footer-include](../includes/footer-banner.md)]