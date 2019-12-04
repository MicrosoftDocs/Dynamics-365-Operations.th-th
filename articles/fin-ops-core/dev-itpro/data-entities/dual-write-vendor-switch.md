---
title: สลับระหว่างการออกแบบผู้จัดจำหน่าย
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772375"
---
# <a name="switch-between-vendor-designs"></a>สลับระหว่างการออกแบบผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>โฟลว์ข้อมูลของผู้จัดจำหน่าย 

หากคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการแยกข้อมูลผู้จัดจำหน่ายออกจากข้อมูลลูกค้า ใช้การออกแบบผู้จัดจำหน่ายพื้นฐานนี้  

![ขั้นตอนของผู้จัดจำหน่ายพื้นฐาน](media/dual-write-switch-1.png)
 
ถ้าคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการใช้เอนทิตี **บัญชี** ต่อเพื่อการเก็บข้อมูลผู้จัดจำหน่าย ใช้การออกแบบผู้จัดจำหน่ายแบบขยายนี้ ในการออกแบบนี้ข้อมูลของผู้จัดจำหน่ายแบบขยาย เช่นสถานะระงับของผู้จัดจำหน่ายและโพรไฟล์ผู้จัดจำหน่ายถูกจัดเก็บในเอนทิตี **ผู้จัดจำหน่าย** ใน Common Data Service 

![โฟลว์ของผู้จัดจำหน่ายแบบขยาย](media/dual-write-switch-2.png)
 
ทำตามขั้นตอนด้านล่างเพื่อใช้การออกแบบผู้จัดจำหน่ายแบบขยาย: 
 
1. แพคเกจโซลูชัน **SupplyChainCommon** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงาน ดังที่แสดงในรูปแบบต่อไปนี้
    > [!div class="mx-imgBorder"]
    > ![เท็มเพลตการประมวลผลลำดับงาน](media/dual-write-switch-3.png)
2. สร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน: 
    1. สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตีบัญชี** และคลิก **ตกลง** ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**
        > [!div class="mx-imgBorder"]
        > ![สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี](media/dual-write-switch-4.png)
    2. สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **อัปเดตเอนทิตีบัญชี** และคลิก **ตกลง** ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี** 
        > [!div class="mx-imgBorder"]
        > ![อัพเดตเอนทิตีบัญชี](media/dual-write-switch-5.png)
    3. สร้างกระบวนการลำดับงานใหม่จากเท็มเพลตที่สร้างบนเอนทิตี **บัญชี** 
        > [!div class="mx-imgBorder"]
        > ![สร้างผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![อัพเดตเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-7.png)
    4. คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์หรือแบ็คกราวน์ตามความต้องการของคุณ 
        > [!div class="mx-imgBorder"]
        > ![การแปลงเป็นลำดับงานพื้นหลัง](media/dual-write-switch-8.png)
    5. เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี **บัญชี** ของ Customer Engagement สำหรับการจัดเก็บข้อมูลผู้จัดจำหน่าย 
 
