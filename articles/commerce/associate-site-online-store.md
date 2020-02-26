---
title: เชื่อมโยงไซต์อีคอมเมิร์ซกับช่องทางออนไลน์
description: หัวข้อนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์หนึ่งแห่งขึ้นไป
author: stuharg
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: bicyclingfool
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8de02eca941054c7c43dec1c904f461da1927230
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001219"
---
# <a name="associate-an-e-commerce-site-with-an-online-channel"></a>เชื่อมโยงไซต์อีคอมเมิร์ซกับช่องทางออนไลน์

[!include [banner](includes/banner.md)]


หัวข้อนี้อธิบายถึงวิธีการผูกไซต์ Microsoft Dynamics 365 Commerce ของคุณกับร้านค้าออนไลน์หนึ่งแห่งขึ้นไป 

หลังจากที่คุณได้เตรียมใช้งานอีคอมเมิร์ซโดยใช้พอร์ทัล Microsoft Dynamics Lifecycle Services (LCS) คุณพร้อมที่จะสร้างเว็บไซต์อีคอมเมิร์ซแรกของคุณ เนื่องจากเป็นส่วนหนึ่งของการสร้างไซต์เริ่มต้น คุณเชื่อมโยงไซต์กับร้านค้าออนไลน์ที่สร้างไว้ก่อนหน้านี้ ขั้นตอนนี้ผูกไซต์กับช่องทางออนไลน์ และให้ไซต์แสดงลำดับชั้นการนำทาง ผลิตภัณฑ์ ประเภท ราคา ตัวเลือกการจัดส่ง และข้อมูลอื่นๆ ที่คุณได้กำหนดไว้ในร้านค้าออนไลน์

เมื่อต้องการสร้างไซต์ใหม่และเชื่อมโยงร้านค้าออนไลน์กับไซต์ ใน LCS เลือกลิงค์สำหรับสภาพแวดล้อมการสร้างไซต์ หลังจากนั้น บนเพจสำหรับสภาพแวดล้อมการสร้างไซต์ ให้เลือก **ไซต์ใหม่** ในกล่องโต้ตอบ **ไซต์ใหม่** คุณต้องระบุข้อมูลพื้นฐานเกี่ยวกับไซต์ของคุณ สำหรับคำอธิบายที่สมบูรณ์ของข้อมูลที่คุณต้องระบุ ดูที่ [การสร้างไซต์อีคอมเมิร์ซใหม่](create-ecommerce-site.md)

หลังจากที่สร้างไซต์แล้ว คุณสามารถตรวจสอบว่ามีการเชื่อมโยงกับร้านค้าออนไลน์ของคุณ โดยเลือกแท็บ **ผลิตภัณฑ์** คุณควรเห็นการจัดประเภทของผลิตภัณฑ์ที่ถูกปันส่วนให้กับร้านค้าออนไลน์ นอกจากนี้คุณยังสามารถใช้ฟิลด์แบบหล่นลงที่ด้านบนซ้ายของเพจ เพื่อเข้าถึงผลิตภัณฑ์ตามประเภท

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md)

[ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)](add-cdn-support.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)
