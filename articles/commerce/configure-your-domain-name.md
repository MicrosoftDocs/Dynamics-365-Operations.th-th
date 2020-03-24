---
title: ตั้งค่าคอนฟิกชื่อโดเมนของคุณ
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096831"
---
# <a name="configure-your-domain-name"></a>ตั้งค่าคอนฟิกชื่อโดเมนของคุณ


[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365 

## <a name="add-domains-during-e-commerce-initialization"></a>เพิ่มโดเมนระหว่างการเริ่มต้นอีคอมเมิร์ซ

เมื่อต้องการเชื่อมโยงโดเมนกับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ ให้เริ่มต้นการใช้อีคอมเมิร์ซตามที่อธิบายไว้ใน [การจัดวางไซต์ e commerce ใหม่](deploy-ecommerce-site.md) ระหว่างการเริ่มต้น ระบบจะขอให้คุณป้อนข้อมูลที่จะใช้เพื่อจัดเตรียมสภาพแวดล้อมของอีคอมเมิร์ซของคุณ ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้เพิ่มโดเมนทั้งหมดที่คุณวางแผนที่จะใช้กับสภาพแวดล้อมการทำงานนี้ โดเมนต่างๆ ควรถูกแยกด้วยเครื่องหมายอัฒภาค ในลักษณะนี้จะมีการตั้งค่าคอนฟิกโดเมนในส่วนประกอบอีคอมเมิร์ซทั้งหมดที่จำเป็น และจะพร้อมใช้งานเมื่อคุณสลับปริมาณการใช้งานจากเครือข่ายการจัดส่งเนื้อหา (CDN) หรือเว็บเซิร์ฟเวอร์ของคุณ แล้วชี้ไปที่ฟรอนท์เอนด์อีคอมเมิร์ซ

## <a name="add-domains-after-e-commerce-initialization"></a>เพิ่มโดเมนหลังจากการเริ่มต้นอีคอมเมิร์ซ

เมื่อต้องการเชื่อมโยงโดเมนใหม่กับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ หลังจากการเริ่มต้นอีคอมเมิร์ซคุณต้องส่งคำขอบริการ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[ตั้งค่าช่องทางร้านค้าออนไลน์](online-stores.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[เชื่อมโยงไซต์ออนไลน์กับช่องทาง](associate-site-online-store.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก](upload-bulk-redirects.md)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-B2C-tenants.md)

[เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)
