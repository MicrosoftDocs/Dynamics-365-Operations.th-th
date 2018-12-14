---
title: "บันทึกคู่มืองานไปยัง LCS และเล่นซ้ำ"
description: "หัวข้อนี้อธิบายวิธีการบันทึกคู่มืองานไปยัง Microsoft Dynamics Lifecycle Services (LCS) และจากนั้นเล่นซ้ำ"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>บันทึกคู่มืองานไปยัง LCS และเล่นซ้ำ

[!include [banner](includes/banner.md)]

**รายละเอียดสภาพแวดล้อม** 

Microsoft Dynamics 365 for Talent ที่ถูกปรับใช้ผ่านทาง Microsoft Dynamics Lifecycle Services (LCS)

**ออก**

ลูกค้าต้องการบันทึกการบันทึกภารกิจใหม่ไปยังโครงการ LCS ของเขาหรือเธอ และจากนั้นเล่นซ้ำคู่มืองานที่บันทึกไว้

**การแก้ปัญหา**

ทำตามขั้นตอนเหล่านี้เพื่อบันทึกการบันทึกงานไปยัง LCS

1. ลงชื่อเข้าใช้ไปยัง LCS และเลือกโครงการ
2. เลือกไทล์ **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**
3. ดูหน้าใน "ประสบการณ์ BPM ที่ปรับปรุงแล้ว"
4. เลือกไลบรารี และจากนั้น เลือก **คัดลอก**
5. ป้อนชื่อสำหรับตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM)
6. ลงชื่อเข้าใช้ใน Talent จาก LCS
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

