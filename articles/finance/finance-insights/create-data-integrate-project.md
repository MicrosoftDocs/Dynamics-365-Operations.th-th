---
title: สร้างโครงการรวมข้อมูล
description: บทความนี้จะอธิบายถึงวิธีการสร้างโครงการรวมข้อมูล
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876253"
---
# <a name="create-a-data-integration-project"></a>สร้างโครงการรวมข้อมูล

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายถึงวิธีการสร้างโครงการรวมข้อมูล

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

    6. เลือกการแมปองค์กรที่เหมาะสม
    7. เลือก **สร้าง**

5. เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้  

    1. สร้างโครงการการรวมข้อมูลเดียวสำหรับเทมเพลตแต่ละรายการต่อไปนี้โดยใช้การตั้งค่าการเชื่อมต่อที่คุณเพิ่งสร้างขึ้น:

        - ผลลัพธ์เชิงลึกของการชำระเงินของลูกค้า (CDS to Fin และ Ops 10.0.17+)
        - ผลลัพธ์ของชุดเวลาของกระแสเงินสด (CD to Fin และ Ops)
        - ผลลัพธ์ของชุดเวลาของงบประมาณ (CD to Fin และ Ops)

      > [!NOTE]
      > การสร้างโครงการการรวมข้อมูลหลายโครงการให้กับเทมเพลตแต่ละรายการอาจทําให้เกิดข้อผิดพลาดที่จะบล็อคการอัปเดต

    2. ตั้งค่าการจัดกำหนดการที่เหมาะสมสำหรับแต่ละโครงการ

> [!NOTE]
> ถ้าคุณไม่เห็นเอนทิตีที่จำเป็นใน Dataverse โปรดไปที่ **เครดิตและการเรียกเก็บเงิน** > **การตั้งค่า** > **Finance Insights** > **พารามิเตอร์ Finance Insights** ให้เปิดใช้งาน **การคาดการณ์การชำระเงินของลูกค้า** และเลือก **สร้างแบบจำลองการคาดคะเน** เมื่อการใช้งานของโมเดล AI เสร็จสมบูรณ์ เอนทิตี Dataverse ที่จำเป็นในการสร้างการรวมจะถูกปรับใช้

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
