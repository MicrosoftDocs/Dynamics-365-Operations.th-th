---
title: เปิดใช้งานข้อเสนองบประมาณ (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995151"
---
# <a name="enable-budget-proposals-preview"></a>เปิดใช้งานข้อเสนองบประมาณ (ตัวอย่าง)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน

1. ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox (คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > ถ้าการปรับใช้ Microsoft Dynamics 365 Finance ของคุณเป็นการปรับใช้การให้บริการ คุณสามารถข้ามขั้นตอนนี้ได้ ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว ถ้าคุณไม่เห็นคุณสมบัตินี้ในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากคุณประสบปัญหาเมื่อพยายามเปิดใช้งาน ให้ส่งอีเมลไปที่ [ทีมแสดงตัวอย่างข้อมูลเชิงลึกของการเงิน](mailto:fiap@microsoft.com)

2. เปิดพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และปฏิบัติตามขั้นตอนเหล่านี้:

    1. เลือก **ตรวจหาการอัพเดต**
    2. ค้นหา **ข้อเสนองบประมาณ** และเปิดใช้งานลักษณะการทำงานนั้น

3. ไปที่ **การจัดงบประมาณ \> การตั้งค่า \> การจัดงบประมาณพื้นฐาน \> ข้อเสนองบประมาณ (ตัวอย่าง)** และเลือก **เปิดใช้งานคุณลักษณะ**

#### <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว
การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด
