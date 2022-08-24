---
title: เลือกที่จะใช้การให้คะแนนและบทวิจารณ์
description: บทความนี้อธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269174"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

[!include [banner](includes/banner.md)]

บทความนี้อธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ

โซลูชันการให้คะแนนและการตรวจทาน เป็นโซลูชันช่องทาง Omni ที่คุณสามารถทำให้พร้อมใช้งานใน Dynamics 365 Commerce ได้ โดยใช้ Microsoft Dynamics Lifecycle Services (LCS) LCS เป็นพอร์ทัลการจัดการที่ร้านค้าปลีกใช้ในการจัดการสภาพแวดล้อมของตนเองจากการเตรียมใช้งานเพื่อรื้อถอน

หากคุณต้องการใช้โซลูชันการให้คะแนนและการวิจารณ์บนเว็บไซต์การค้าของคุณ คุณต้องเลือกรับการให้คะแนนและตรวจสอบระหว่างการปรับใช้ไซต์ e-Commerce ของคุณบน Dynamics 365 Commerce

## <a name="opt-in-to-use-ratings-and-reviews"></a>เลือกที่จะใช้การให้คะแนนและบทวิจารณ์

เมื่อต้องการเลือกที่จะใช้การจัดอันดับและข้อคิดเห็นบนไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้

1. ทำตามขั้นตอนใน [ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)
1. ขณะที่คุณยังคงอยู่ใน LCS ให้ไปที่ **ที่การตั้งค่าการปรับใช้การขายปลีก \> การตั้งค่าอื่นๆ**
1. ตั้งค่าตัวเลือกการ **เปิดใช้งานการจัดอันดับและข้อคิดเห็น** เป็น **ใช่**
1. ในฟิลด์ **กลุ่มรักษาความปลอดภัย AAD สำหรับผู้ควบคุมการให้คะแนนและบทวิจารณ์** ให้ป้อนรหัสของกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) ที่รวมถึงผู้ควบคุมการให้คะแนนและบทวิจารณ์

    ![เลือกที่จะใช้การให้คะแนนและบทวิจารณ์](media/LCS_RnR_Preference_2.png)

1. ดำเนินกระบวนการเริ่มต้นทางอีคอมเมิร์ซให้เสร็จสมบูรณ์

> [!NOTE] 
> หากคุณเป็นลูกค้า Dynamics 365 Commerce แล้ว ซึ่งได้ปรับใช้ไซต์ e-Commerce โดยไม่ต้องเลือกรับการให้คะแนนและการวิจารณ์ และตอนนี้ต้องการใช้การให้คะแนนและการวิจารณ์จากแพคเกจ Dynamics 365 Commerce โปรดส่งคำขอการบริการ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการส่งคำขอการบริการ ดู [กระบวนการส่งคำขอการบริการ](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json) 

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของการให้คะแนนและบทวิจารณ์](ratings-reviews-overview.md)

[จัดการการให้คะแนนและบทวิจารณ์](manage-reviews.md)

[ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์](configure-ratings-reviews.md)

[ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Commerce](sync-product-ratings.md)

[เปิดใช้งานการเผยแพร่การให้คะแนนและบทวิจารณ์ด้วยตนเองโดยผู้ดูแล](manual-publish-rating-reviews.md)

[นําเข้าและส่งออกการให้คะแนนและบทวิจารณ์](import-export-reviews.md)

[ตั้งค่าคอนฟิกการรับรองความถูกต้องแบบบริการกับบริการ](service-to-service-auth.md)

[คำถามที่ถามบ่อยเกี่ยวกับการให้คะแนนและบทวิจารณ์](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
