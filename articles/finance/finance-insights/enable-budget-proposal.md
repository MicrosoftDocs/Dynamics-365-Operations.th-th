---
title: เปิดใช้งานข้อเสนองบประมาณ
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ab65d1b0e366bfe6bdb07688f89d440662165063
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386497"
---
# <a name="enable-budget-proposals"></a>เปิดใช้งานข้อเสนองบประมาณ

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานข้อเสนองบประมาณในข้อมูลเชิงลึกทางการเงิน

1. ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox (คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > ข้ามขั้นตอนนี้ถ้าคุณใช้รุ่น 10.0.20 หรือใหม่กว่า หรือถ้าคุณใช้งานการปรับใช้ Service Fabric ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว ถ้าคุณไม่เห็นคุณลักษณะในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากประสบปัญหาเมื่อคุณพยายามเปิดใช้งาน โปรดติดต่อ <fiap@microsoft.com>

2. เปิดพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และปฏิบัติตามขั้นตอนเหล่านี้:

    1. เลือก **ตรวจหาการอัพเดต**
    2. ค้นหา **ข้อเสนองบประมาณ** และเปิดใช้งานลักษณะการทำงานนั้น

3. ไปที่ **การจัดงบประมาณ \> การตั้งค่า \> การจัดงบประมาณพื้นฐาน \> ข้อเสนองบประมาณ (ตัวอย่าง)** และเลือก **เปิดใช้งานคุณลักษณะ**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
