---
title: สร้างโครงการรวมข้อมูล
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการรวมข้อมูล
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 7841f8b31e0ac1a40dce9acaac747f5f378236e0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752675"
---
# <a name="create-a-data-integration-project"></a>สร้างโครงการรวมข้อมูล

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการรวมข้อมูล

1. ลงชื่อเข้าใช้ Microsoft Dynamics 365 Finance
2. ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือก **เอนทิตีข้อมูล** รอจนกว่าจะมีการรีเฟรชเอนทิตีข้อมูลทั้งหมดก่อนที่คุณจะไปยังขั้นตอนถัดไป
3. เปิด [พอร์ทัล Power Apps](https://make.powerapps.com/) และปฏิบัติตามขั้นตอนต่อไปนี้

    1. ให้เลือกสภาพแวดล้อมที่เหมาะสม
    2. ในบานหน้าต่างนำทางด้านซ้ายมือ ให้เลือก **Dataverse \> การเชื่อมต่อ**
    3. เชื่อมต่อกับอินสแตนซ์ที่เหมาะสมของรายการต่อไปนี้:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้

    1. เลือก **การรวมข้อมูล**
    2. เลือก **การตั้งค่าการเชื่อมต่อ**
    3. เลือก **การตั้งค่าการเชื่อมต่อใหม่**
    4. ป้อนชื่อสำหรับการเชื่อมต่อ
    5. เลือกการเชื่อมต่อที่ถูกต้องสำหรับสินค้าต่อไปนี้

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. เลือกการแม็ปองค์กรที่เหมาะสม
    7. เลือก **สร้าง**

5. เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้  

    1. สร้างโครงการการรวมข้อมูลสำหรัแม่แบบต่อไปนี้โดยใช้การตั้งค่าการเชื่อมต่อที่คุณเพิ่งสร้างขึ้น:

        - ผลลัพธ์เชิงลึกของการชำระเงินของลูกค้า (CDS to Fin และ Ops 10.0.17+)
        - ผลลัพธ์ของชุดเวลาของกระแสเงินสด (CD to Fin และ Ops)
        - ผลลัพธ์ของชุดเวลาของงบประมาณ (CD to Fin และ Ops)

    2. ตั้งค่าการจัดกำหนดการที่เหมาะสมสำหรับแต่ละโครงการ

> [!NOTE]
> ถ้าคุณไม่เห็นเอนทิตีที่จำเป็นใน CDS โปรดไปที่ **เครดิตและการเรียกเก็บเงิน > การตั้งค่า > ข้อมูลเชิงลึกทางการเงิน > พารามิเตอร์ข้อมูลเชิงลึกของการเงิน** ให้เปิดใช้งานลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าและคลิกที่ปุ่ม **สร้างแบบจำลองการคาดคะเน** เมื่อการใช้งานของโมเดล AI เสร็จสมบูรณ์ (ประสบความสำเร็จหรือล้มเหลว) เอนทิตี CDS ที่จำเป็นในการสร้างการรวมจะถูกปรับใช้ใน CDS

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
