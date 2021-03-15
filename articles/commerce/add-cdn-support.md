---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)
description: หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d9482a45cb8f2ea52e7f58d55e30cfe56694d04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985965"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)


[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Dynamics 365 Commerce ของคุณ

## <a name="overview"></a>ภาพรวม

เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้ 

คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย \<*e-commerce-tenant-name*\> เป็นชื่อของสภาพแวดล้อมของคุณ:

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

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure

การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ไปยังกลุ่ม back-end เพื่อเป็นโฮสต์ที่กำหนดเอง ที่มีส่วนหัวของโฮสต์ back-end ที่ว่างเปล่า
1. ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure โดยมีการป้อนชื่อโฮสต์ back-end

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure ด้วยค่าเริ่มต้นการสร้างสมดุลในการโหลด

![เพิ่มกล่องโต้ตอบกลุ่ม back-end ต่อไป](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>ตั้งค่ากฎใน Front Door Service ของ Azure

การตั้งค่ากฎการกำหนดเส้นทางใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่มการกำหนดเส้นทาง
1. ในฟิลด์ **ชื่อ** ให้ป้อน **ค่าเริ่มต้น**
1. ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**
1. ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**
1. ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบน ให้ป้อน **/\** _
1. ภายใต้ _*รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**
1. ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**
1. ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่** 
1. ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**
1. ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**

การตั้งค่ากฎการแคชใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่มกฎการแคช
1. ในฟิลด์ **ชื่อ** ให้ป้อน **สถิติ**
1. ในฟิลด์ **โพรโทคอลที่ยอมรับ** เลือก **HTTP และ HTTPS**
1. ในฟิลด์ **โฮสต์ Frontend** ให้ป้อน **dynamics-ecom-tenant-name.azurefd.net**
1. ภายใต้ **รูปแบบที่เข้ากัน** ในฟิลด์ด้านบน **/\_msdyn365/\_scnr/\** _
1. ภายใต้ _*รายละเอียดกระบวนการ** ตั้งค่าตัวเลือก **ชนิดของกระบวนการ** เป็น **ส่งต่อ**
1. ในฟิลด์ **กลุ่ม Backend** ให้เลือก **ecom-backend**
1. ในกลุ่มฟิลด์ **โพรโทคอลการส่งต่อ** เลือกตัวเลือก **การร้องขอการจับคู่**
1. ตั้งค่า่ตัวเลือก **เขียน URL ใหม่** เป็น **ปิดใช้งาน**
1. ตั้งค่า่ตัวเลือก **การแคช** เป็น **ปิดใช้งาน**
1. ในฟิลด์ **พฤติกรรมแคชสตริงการสอบถาม** เลือก **แคลทุก URL ที่ไม่ซ้ำกัน**
1. ในกลุ่มฟิลด์ **การบีบอัดแบบไดนามิก** ให้เลือกตัวเลือก **เปิดใช้งาน**

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกฎ** ใน Front Door Service ของ Azure

![กล่องโต้ตอบกฎ](./media/CDN_CachingRule.png)

> [!WARNING]
> หากโดเมนที่คุณจะใช้เปิดใช้งานอยู่และมีอยู่แล้ว ให้สร้างตั๋วการสนับสนุนจากไทล์ **สนับสนุน** ใน [Lifecycle Services ของ Microsoft Dynamics ](https://lcs.dynamics.com/) เพื่อรับความช่วยเหลือสำหรับขั้นตอนถัดไป สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การขอความช่วยเหลือสำหรับแอป Finance and Operations หรือ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)

หากโดเมนของคุณใหม่และไม่ใช่ไลฟ์โดเมนที่มีอยู่ก่อนหน้านี้ คุณสามารถเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure การทำเช่นนี้จะเปิดใช้งานการรับส่งผ่านเว็บเพื่อให้ตรงกับไซต์ของคุณผ่านทางอินสแตนซ์ Front Door ของ Azure การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

สำหรับคำแนะนำโดยละเอียดเกี่ยวกับการเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของ Azure ของคุณ ให้ดูที่ [การเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของคุณ](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)

ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าคอนฟิกชื่อโดเมนของคุณ](configure-your-domain-name.md)

[ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)

[สร้างไซต์อีคอมเมิร์ซ](create-ecommerce-site.md)

[เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์](associate-site-online-store.md)

[จัดการไฟล์ robots.txt](manage-robots-txt-files.md)

[อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก](upload-bulk-redirects.md)

[ตั้งค่าผู้เช่า B2C ใน Commerce](set-up-B2C-tenant.md)

[ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้](custom-pages-user-logins.md)

[ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce](configure-multi-B2C-tenants.md)

[เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]