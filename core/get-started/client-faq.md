---
title: "FAQ เกี่ยวกับไคลเอนต์ Dynamics 365 for Operations"
description: "บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับไคลเอนต์ Microsoft Dynamics 365 for Operations"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e8f09b965403298630460ccb6669fd82abb0e8c
ms.contentlocale: th-th
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>FAQ เกี่ยวกับไคลเอนต์ Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]


บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับไคลเอนต์ Microsoft Dynamics 365 for Operations

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>เพราะเหตุใดสัญลักษณ์จึงไม่โหลดเมื่อฉันใช้ Dynamics 365 for Operations
-----------------------------------------------------------------

การตั้งค่าความปลอดภัยในเบราเซอร์ของคุณอาจป้องกันสัญลักษณ์จากการถูกโหลดอย่างถูกต้อง เพื่อแก้ไขปัญหานี้ ทำตามขั้นตอนต่อไปนี้:

-   ถ้าคุณกำลังประสบกับปัญหานี้ใน Internet Explorer คลิก **เครื่องมือ**แล้วคลิก **ตัวเลือกอินเทอร์เน็ต**  ในกล่องโต้ตอบตัวเลือกอินเทอร์เน็ต บนแท็บ **ความเป็นส่วนตัว** คลิก **ระดับแบบกำหนดเอง** และตรวจสอบให้แน่ใจว่าตัวเลือก **ดาวน์โหลดแบบอักษร** ได้ถูกเลือก
-   มิฉะนั้น คุณอาจต้องเพิ่มไซต์ Dynamics 365 for Operations ลงในรายการไซต์ที่เชื่อถือ

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>ฉันขาด ribbon จาก Dynamics AX 2012 ฉันสามารถรักษาแท็บบานหน้าต่างการดำเนินการให้เปิดตลอดเวลาได้หรือไม่
เรากำลังวางแผนจะใช้คุณลักษณะนี้ในเร็วๆ นี้ ผู้ใช้สามารถเลือกเพื่อรักษาแท็บในบานหน้าต่างการดำเนินการเปิดตลอดเวลา มิฉะนั้น แท็บจะสามารถยุบเมื่อไม่ได้กำลังใช้งาน เพื่อเข้าใช้พื้นที่หน้าจอเพิ่มเติมสำหรับหน้านั้น

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>เหตุใดบางครั้งฉันสามารถดูเมนูทางลัดที่แตกต่างกันเมื่อฉันคลิกขวา
ถ้าคุณคลิกขวาในฟิลด์แก้ไขได้ (หรือ ถ้าข้อความถูกเลือก), เมนูทางลัดของเบราเซอร์จะแสดงขึ้น เมนูนี้ช่วยให้คุณเข้าถึงคำสั่ง **ตัด**, **สำเนา**และ **วาง** เราไม่สามารถฝังคำสั่งเหล่านี้ลงในเมนูทางลัด Dynamics 365 for Operations เนื่องจาก เหตุผลด้านความปลอดภัย เบราเซอร์ไม่อนุญาติให้เราเข้าถึงคลิปบอร์ดระบบทางโปรแกรม

ถ้าคุณคลิกขวาที่ป้ายชื่อฟิลด์หรือค่าของตัวควบคุมแบบอ่านอย่างเดียว คุณจะเห็นเมนูทางลัด Dynamics 365 for Operations

เพื่อให้เข้าถึงแป้นพิมพ์ได้ง่าย เราวางแผนจะใช้แป้นพิมพ์ลัดในอนาคตซึ่งจะเปิดเมนูทางลัด Dynamics 365 for Operations

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>ฟังก์ชันดูรายละเอียดใน Dynamics 365 for Operations อยู่ที่ใด
ตัวเลือก **ดูรายละเอียด** จะพร้อมใช้งานในสองวิธี:

-   หากส่วนควบคุมมีความสามารถในการ **ดูรายละเอียด**และถ้าตัวควบคุมมีค่า ค่านั้นจะแสดงเป็นไฮเปอร์ลิงค์ คุณสามารถคลิกไฮเปอร์ลิงค์เพื่อเปิดหน้าซึ่งประกอบด้วยรายละเอียดเพิ่มเติม
-   **ดูรายละเอียด** เป็นตัวเลือกบนเมนูทางลัด Dynamics 365 for Operations สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเมนูทางลัด Dynamics 365 for Operations จะแสดงขึ้นเมื่อคุณคลิกขวา โปรดดูส่วนก่อนหน้านี้





