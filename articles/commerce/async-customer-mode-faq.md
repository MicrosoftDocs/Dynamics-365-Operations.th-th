---
title: FAQ โหมดการสร้างลูกค้าแบบอะซิงโครนัส
description: บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับโหมดการสร้างลูกค้าแบบอะซิงโครนัสใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229881"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>FAQ โหมดการสร้างลูกค้าแบบอะซิงโครนัส

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับโหมดการสร้างลูกค้าแบบอะซิงโครนัส (async) ใน Microsoft Dynamics 365 Commerce

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>เพราะเหตุใดฉันจึงไม่สามารถเปิดใช้งานคุณลักษณะ "เปิดใช้งานการแก้ไขลูกค้าในโหมดอะซิงโครนัส" ได้

ก่อนจะเปิดใช้งานคุณลักษณะ **เปิดใช้งานการแก้ไขลูกค้าในโหมดอะซิงโครนัส** คุณต้องเปิดใช้งานคุณลักษณะต่อไปนี้

- การปรับปรุงประสิทธิภาพสำหรับใบสั่งของลูกค้าและธุรกรรมของลูกค้า
- เปิดใช้งานการสร้างลูกค้าแบบอะซิงโครนัสที่ได้รับการปรับปรุง
- เปิดใช้งานการสร้างแบบอะซิงโครนัสสำหรับที่อยู่ลูกค้า

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>เพราะเหตุใดฉันยังคงเห็นการเรียกบริการแบบเรียลไทม์ที่เรียกไปยัง Commerce headquarters หลังจากเปิดใช้งานคุณลักษณะ "เปิดใช้งานการแก้ไขลูกค้าในโหมดอะซิงโครนัส" แล้ว

ปัญหานี้จะเกิดขึ้นเมื่อยังไม่ได้รันงาน Commerce Data Exchange (CDX) เพื่อให้แน่ใจว่าสถานะคุณลักษณะและข้อมูลเมตาของช่องทางอื่นถูกซิงโครไนส์กับช่องทาง ก่อนที่คุณจะลองสถานการณ์ใหม่ โปรดตรวจสอบให้แน่ใจว่างาน CDX ต่อไปนี้ถูกรันใน Commerce headquarters:

- 1110 (การตั้งค่าคอนฟิกแบบครอบคลุม)
- 1010 (ลูกค้า)
- 1070 (การตั้งค่าคอนฟิกช่องทาง)

ข้อมูลที่เก็บไว้ใน Commerce Scale Unit (CSU) อาจไม่สะท้อนให้เห็นใน Commerce headquarters ในทันทีหลังจากที่รันงาน CDX แล้ว

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>เพราะเหตุใด Commerce headquarters จึงแสดงการสร้างหรือการอัปเดตของลูกค้าจากการขายหน้าร้าน (POS) หรือช่องทางอีคอมเมิร์ซ

ตรวจสอบให้แน่ใจว่าคุณได้ปฏิบัติการดังต่อไปนี้ตามลำดับ:

1. รันงาน CDX P-job ใน Commerce headquarters เพื่อให้แน่ใจว่าข้อมูลลูกค้าในโหมด Async ที่จัดเก็บอยู่ในตาราง **RETAILASYNCCUSTOMERV2**, **RETAILASYNCADDRESSV2**, **RETAILASYNCCUSTOMERCONTACT**, **RETAILASYNCCUSTOMERAFFILIATION** และ **RETAILASYNCCUSTOMERATTRIBUTTAR2** มีให้ใช้งานใน Commerce headquarters
1. รันชุดงาน **ซิงโครไนส์ลูกค้าและคำขอช่องทาง** ใน Commerce headquarters หลังจากการปฏิบัติการชุดงานเสร็จเรียบร้อยแล้ว เรกคอร์ดทั้งหมดที่ประมวลผลเรียบร้อยแล้วจากตารางดังกล่าวก่อนหน้านี้จะมีการตั้งค่าฟิลด์ **OnlineOperationCompleted** เป็น **1**
