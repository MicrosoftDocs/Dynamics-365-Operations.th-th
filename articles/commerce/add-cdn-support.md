---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)
description: หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf5a0da2803f985e6c0c04dd9916977397173d11
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001633"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)


[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ

## <a name="overview"></a>ภาพรวม

เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้ 

คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย *ชื่อผู้เช่าอีคอมเมิร์ซ* เป็นชื่อของสภาพแวดล้อมของคุณ:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นในระหว่างกระบวนการจัดเตรียม สนับสนุนใบรับรอง Secure Sockets Layer (SSL) สำหรับ \*.commerce.dynamics.com เท่านั้น ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง ดังนั้น คุณต้องยกเลิก SSL สำหรับโดเมนที่กำหนดเองใน CDN และส่งต่อข้อมูลจาก CDN ไปยังชื่อโฮสต์หรือปลายทางที่ Commerce ถูกสร้างขึ้น 

นอกจากนี้ *สถิติ* (JavaScript หรือไฟล์ Cascading Style Sheets \[CSS\]) จาก Commerce จะถูกส่งจากปลายทางที่ Commerce ถูกสร้าง \*.(commerce.dynamics.com) สถิตสามารถแคชได้เฉพาะเมื่อชื่อโฮสต์หรือปลายทางที่สร้าง Commerce ถูกวางอยู่หลัง CDN

## <a name="set-up-ssl"></a>ตั้งค่า SSL

เพื่อช่วยรับประกันว่ามีการตั้งค่า SSL และสถิตที่มีการแคช คุณต้องตั้งค่าคอนฟิก CDN ของคุณเพื่อให้เชื่อมโยงกับชื่อโฮสต์ที่ Commerce สร้างขึ้นสำหรับสภาพแวดล้อมของคุณ นอกจากนี้คุณต้องแคชรูปแบบต่อไปนี้สำหรับสถิตเท่านั้น: 

/\_msdyn365/\_scnr/\*

หลังจากที่คุณจัดเตรียมสภาพแวดล้อม Commerce กับโดเมนแบบกำหนดเองที่ให้ไว้ หรือหลังจากที่คุณระบุโดเมนที่กำหนดเองสำหรับสภาพแวดล้อมของคุณ โดยใช้คำขอการบริการ ให้กำหนดโดเมนที่กำหนดเองของคุณไปยังชื่อโฮสต์หรือปลายทางที่ Commerce สร้างขึ้น

ดังที่ได้กล่าวถึงก่อนหน้านี้ ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นจะสนับสนุนใบรับรอง SSL สำหรับ \*.commerce.dynamics.com เท่านั้น ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง

## <a name="cdn-services"></a>การบริการ CDN

บริการ CDN ใดๆ สามารถใช้กับสภาพแวดล้อม Commerce ได้ นี่คือ สองตัวอย่าง:

- **Microsoft Azure Front Door Service** – โซลูชัน Azure CDN สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Front Door Service ของ Azure ดู [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/)
- **Akamai Dynamic Site Accelerator** – สำหรับข้อมูลเพิ่มเติม ดู [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)

## <a name="cdn-setup"></a>การตั้งค่า CDN

กระบวนการติดตั้ง CDN ประกอบด้วยขั้นตอนทั่วไปเหล่านี้:

1. เพิ่มโฮสต์ front-end
1. ตั้งค่าคอนฟิกกลุ่ม back-end
1. ตั้งค่ากฎสำหรับการกำหนดเส้นทางและการแคช

### <a name="add-a-front-end-host"></a>เพิ่มโฮสต์ front-end

คุณสามารถใช้บริการ CDN ใดๆได้ แต่ตัวอย่างในหัวข้อนี้ จะใช้ Front Door Service ของ Azure 

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Front Door Service ่ของ Azure [เริ่มต้นแบบด่วน: สร้าง Front Door สำหรับโปรแกรมประยุกต์เว็บสากลที่พร้อมใช้งานอย่างสูง](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure

การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ทำตามขั้นตอนต่อไปนี้

1. เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ไปยังกลุ่ม back-end เป็นโฮสต์ที่กำหนดเอง ที่มีส่วนหัวของโฮสต์ back-end ที่ว่างเปล่า
1. ภายใต้ **ปัญหาสุขภาพ** ในฟิลด์ **พาธ** ให้ป้อน **/keepalive**
1. ในฟิลด์ **ช่วง (วินาที)** ให้ป้อน **255**
1. ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม Backend** ใน Front Door Service ของ Azure

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>ตั้งค่ากฎใน Front Door Service ของ Azure

การตั้งค่ากฎการกำหนดเส้นทางใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่มการกำหนดเส้นทาง
1. ในฟิลด์ **ชื่อ** ให้ป้อน **ค่าเริ่มต้น**
1. ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**
1. ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**
1. ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบนให้ป้อน **/\***
1. ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**
1. ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**
1. ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่** 
1. ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**
1. ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**

การตั้งค่ากฎการแคชใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่มกฎการแคช
1. ในฟิลด์ **ชื่อ** ให้ป้อน **สถิติ**
1. ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**
1. ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**
1. ภายใต้ **Patterns to match** ในฟิลด์ด้านบนให้ป้อน **/\_msdyn365/\_scnr/\***
1. ภายใต้ **รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**
1. ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**
1. ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**
1. ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**
1. ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**
1. ในฟิลด์ **พฤติกรรมแคชสตริงการสอบถาม** เลือก **แคลทุก URL ที่ไม่ซ้ำกัน**
1. ในกลุ่มฟิลด์ **การบีบอัดแบบไดนามิก** ให้เลือกตัวเลือก **เปิดใช้งาน**

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกฎ** ใน Front Door Service ของ Azure

![กล่องโต้ตอบกฎ](./media/CDN_CachingRule.png)

หลังจากที่มีการปรับใช้การตั้งค่าคอนฟิกนี้แล้ว คุณต้องเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> ถ้าโดเมนที่คุณจะใช้มีการใช้งานและใช้ได้ยู่แล้ว โปรดติดต่อฝ่ายสนับสนุนเพื่อเปิดใช้งานโดเมนนี้ กับ Front Door Service ของ Azure เพื่อตั้งค่าการทดสอบ

คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md)

[ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[เชื่อมโยงไซต์ออนไลน์กับช่องทาง](associate-site-online-store.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)
