---
title: เลือกที่จะใช้การให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416137"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ

## <a name="overview"></a>ภาพรวม

โซลูชันการให้คะแนนและการตรวจทาน เป็นโซลูชันช่องทาง Omni ที่คุณสามารถทำให้พร้อมใช้งานใน Dynamics 365 Commerce ได้ โดยใช้ Microsoft Dynamics Lifecycle Services (LCS) LCS เป็นพอร์ทัลการจัดการที่ร้านค้าปลีกใช้ในการจัดการสภาพแวดล้อมของตนเองจากการเตรียมใช้งานเพื่อรื้อถอน

หากคุณต้องการใช้โซลูชันการให้คะแนนและการวิจารณ์บนเว็บไซต์การค้าของคุณ คุณต้องเลือกรับการให้คะแนนและตรวจสอบระหว่างการปรับใช้ไซต์ e-Commerce ของคุณบน Dynamics 365 Commerce

## <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

เมื่อต้องการเลือกที่จะใช้การจัดอันดับและข้อคิดเห็นบนไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้

1. ทำตามขั้นตอนใน [ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)
1. ขณะที่คุณยังคงอยู่ใน LCS ให้ไปที่ **ที่การตั้งค่าการปรับใช้การขายปลีก \> การตั้งค่าอื่นๆ**
1. ตั้งค่าตัวเลือกการ **เปิดใช้งานการจัดอันดับและข้อคิดเห็น** เป็น **ใช่**
1. ใน **กลุ่มรักษาความปลอดภัย AAD สำหรับฟิลด์ผู้ควบคุมการการจัดอันดับและแสดงความคิดเห็น** (รหัสออบเจ็กต์ของกลุ่มรักษาความปลอดภัย) ให้ป้อนรหัสของกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) ที่รวมถึงผู้ควบคุมการจัดอันดับและการแสดงความคิดเห็น

    ![เลือกที่จะใช้การให้คะแนนและบทวิจารณ์](media/LCS_RnR_Preference.png)

1. ดำเนินกระบวนการเริ่มต้นทางอีคอมเมิร์ซให้เสร็จสมบูรณ์

> [!NOTE] 
> หากคุณเป็นลูกค้า Dynamics 365 Commerce แล้ว ซึ่งได้ปรับใช้ไซต์ e-Commerce โดยไม่ต้องเลือกรับการให้คะแนนและการวิจารณ์ และตอนนี้ต้องการใช้การให้คะแนนและการวิจารณ์จากแพคเกจ Dynamics 365 Commerce โปรดส่งคำขอการบริการ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการส่งคำขอการบริการ ดู [กระบวนการส่งคำขอการบริการ](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json) 

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการให้คะแนนและบทวิจารณ์](ratings-reviews-overview.md)

[จัดการการให้คะแนนและบทวิจารณ์](manage-reviews.md)

[ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์](configure-ratings-reviews.md)

[ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Commerce](sync-product-ratings.md)


