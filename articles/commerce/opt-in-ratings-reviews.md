---
title: เลือกที่จะใช้การให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697991"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ

## <a name="overview"></a>ภาพรวม

โซลูชันการจัดอันดับและข้อคิดเห็นคือโซลูชันช่องทาง omni ที่คุณสามารถทำให้พร้อมใช้งานใน Dynamics 365 Commerce โดยใช้ Microsoft Dynamics Lifecycle Services (LCS) LCS เป็นพอร์ทัลการจัดการที่ร้านค้าปลีกใช้ในการจัดการสภาพแวดล้อมของตนเองจากการเตรียมใช้งานเพื่อรื้อถอน

ถ้าคุณต้องการใช้การจัดอันดับและโซลูชันข้อคิดเห็นบนเว็บไซต์การค้าของคุณ คุณต้องเลือกที่จะเข้าร่วมก่อน

## <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

เมื่อต้องการเลือกที่จะใช้การจัดอันดับและข้อคิดเห็นบนไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้

1. ทำตามขั้นตอนใน [ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)
1. ขณะที่คุณยังคงอยู่ใน LCS ให้ไปที่ **ที่การตั้งค่าการปรับใช้การขายปลีก \> การตั้งค่าอื่นๆ**
1. ตั้งค่าตัวเลือกการ **เปิดใช้งานการจัดอันดับและข้อคิดเห็น** เป็น **ใช่**
1. ใน **กลุ่มรักษาความปลอดภัย AAD สำหรับฟิลด์ผู้ควบคุมการการจัดอันดับและแสดงความคิดเห็น** (รหัสออบเจ็กต์ของกลุ่มรักษาความปลอดภัย) ให้ป้อนรหัสของกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) ที่รวมถึงผู้ควบคุมการจัดอันดับและการแสดงความคิดเห็น

    ![เลือกที่จะใช้การให้คะแนนและบทวิจารณ์](media/LCS_RnR_Preference.png)

1. ดำเนินกระบวนการเริ่มต้นทางอีคอมเมิร์ซให้เสร็จสมบูรณ์

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการให้คะแนนและบทวิจารณ์](ratings-reviews-overview.md)

[จัดการการให้คะแนนและบทวิจารณ์](manage-reviews.md)

[ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์](configure-ratings-reviews.md)

[ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Retail](sync-product-ratings.md)
