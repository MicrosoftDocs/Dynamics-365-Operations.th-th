---
title: เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์
description: บทความนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์อย่างน้อยหนึ่งร้าน
author: bicyclingfool
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 006c8b60791e0176c808762025f3bfdeaff9c48d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878684"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a>เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์

[!include [banner](includes/banner.md)]

บทความนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์อย่างน้อยหนึ่งร้าน 

หลังจากที่คุณได้เตรียมใช้งานสภาพแวดล้อมอีคอมเมิร์ซ Dynamics 365 Commerce ของคุณ โดยใช้พอร์ทัล Microsoft Dynamics Lifecycle Services (LCS) คุณพร้อมที่จะสร้างเว็บไซต์อีคอมเมิร์ซแรกของคุณ เนื่องจากเป็นส่วนหนึ่งของการสร้างไซต์เริ่มต้น คุณเชื่อมโยงไซต์กับร้านค้าออนไลน์ที่สร้างไว้ก่อนหน้านี้ ขั้นตอนนี้ผูกไซต์กับช่องทางออนไลน์ และให้ไซต์แสดงลำดับชั้นการนำทาง ผลิตภัณฑ์ ประเภท ราคา ตัวเลือกการจัดส่ง และข้อมูลอื่นๆ ที่คุณได้กำหนดไว้ในร้านค้าออนไลน์

เมื่อต้องการสร้างไซต์ใหม่และเชื่อมโยงร้านค้าออนไลน์กับไซต์ ใน LCS เลือกลิงค์สำหรับสภาพแวดล้อมการสร้างไซต์ หลังจากนั้น บนเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่** ในกล่องโต้ตอบ **ไซต์ใหม่** คุณต้องระบุข้อมูลพื้นฐานเกี่ยวกับไซต์ของคุณ สำหรับคำอธิบายที่สมบูรณ์ของข้อมูลที่คุณต้องระบุ ดูที่ [การสร้างไซต์อีคอมเมิร์ซใหม่](create-ecommerce-site.md)

หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์ นอกจากนี้คุณยังสามารถใช้ฟิลด์แบบหล่นลงที่ด้านบนซ้ายของเพจ เพื่อเข้าถึงผลิตภัณฑ์ตามประเภท

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md)

[ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก](upload-bulk-redirects.md)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-B2C-tenants.md)

[เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]