---
title: ตั้งค่าคอนฟิกชื่อโดเมนของคุณ
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3df563b62b40970509340802a09bb36dda14777
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001011"
---
# <a name="configure-your-domain-name"></a>ตั้งค่าคอนฟิกชื่อโดเมนของคุณ


[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365 

## <a name="add-domains-during-e-commerce-initialization"></a>เพิ่มโดเมนระหว่างการเริ่มต้นอีคอมเมิร์ซ

เมื่อต้องการเชื่อมโยงโดเมนกับสภาพแวดล้อมของอีคอมเมิร์ซ Dynamics 365 Commerce ของคุณ ให้เริ่มต้นการใช้อีคอมเมิร์ซตามที่อธิบายไว้ใน  [ปรับใช้ผู้เข่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md) ระหว่างการเริ่มต้น ระบบจะขอให้คุณป้อนข้อมูลที่จะใช้เพื่อจัดเตรียมสภาพแวดล้อมของอีคอมเมิร์ซของคุณ ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้เพิ่มโดเมนทั้งหมดที่คุณวางแผนที่จะใช้กับสภาพแวดล้อมการทำงานนี้ โดเมนต่างๆ ควรถูกแยกด้วยเครื่องหมายอัฒภาค ในลักษณะนี้จะมีการตั้งค่าคอนฟิกโดเมนในส่วนประกอบอีคอมเมิร์ซทั้งหมดที่จำเป็น และจะพร้อมใช้งานเมื่อคุณสลับปริมาณการใช้งานจากเครือข่ายการจัดส่งเนื้อหา (CDN) หรือเว็บเซิร์ฟเวอร์ของคุณ แล้วชี้ไปที่ฟรอนท์เอนด์อีคอมเมิร์ซ

## <a name="add-domains-after-e-commerce-initialization"></a>เพิ่มโดเมนหลังจากการเริ่มต้นอีคอมเมิร์ซ

เมื่อต้องการเชื่อมโยงโดเมนใหม่กับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ หลังจากการเริ่มต้นอีคอมเมิร์ซคุณต้องส่งคำขอบริการ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์](associate-site-online-store.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก](upload-bulk-redirects.md)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-B2C-tenants.md)

[เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]