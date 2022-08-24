---
title: เพิ่มการสนับสนุนสำหรับเครือข่ายการให้บริการเนื้อหา (CDN)
description: บทความนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Microsoft Dynamics 365 Commerce ของคุณ
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 84839c1e370dccd19462de5c4a3dc120df15df09
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275851"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>เพิ่มการสนับสนุนสำหรับเครือข่ายการให้บริการเนื้อหา (CDN)

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการเพิ่มเครือข่ายการจัดส่งเนื้อหา (CDN) ไปยังสภาพแวดล้อม Microsoft Microsoft Dynamics 365 Commerce ของคุณ

เมื่อคุณตั้งค่าสภาพแวดล้อมของอีคอมเมิร์ซ ใน Dynamics 365 Commerce คุณสามารถตั้งค่าคอนฟิกให้ทำงานร่วมกับบริการ CDN ของคุณได้ 

คุณสามารถเปิดใช้งานโดเมนที่กำหนดเองของคุณในระหว่างกระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ อีกทางหนึ่งคือ คุณสามารถใช้คำขอบริการเพื่อตั้งค่าหลังจากที่กระบวนการเตรียมใช้งานเสร็จเรียบร้อยแล้ว กระบวนการเตรียมใช้งานสำหรับสภาพแวดล้อมของอีคอมเมิร์ซสร้างชื่อโฮสต์ที่เชื่อมโยงกับสภาพแวดล้อม ชื่อโฮสต์นี้มีรูปแบบต่อไปนี้ โดย \<*e-commerce-tenant-name*\> เป็นชื่อของสภาพแวดล้อมของคุณ:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นในระหว่างกระบวนการจัดเตรียม สนับสนุนใบรับรอง Secure Sockets Layer (SSL) สำหรับ \*.commerce.dynamics.com เท่านั้น ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง ดังนั้น คุณต้องยกเลิก SSL สำหรับโดเมนที่กำหนดเองใน CDN และส่งต่อข้อมูลจาก CDN ไปยังชื่อโฮสต์หรือปลายทางที่ Commerce ถูกสร้างขึ้น 

นอกจากนี้ *สถิติ* (JavaScript หรือไฟล์ Cascading Style Sheets \[CSS\]) จาก Commerce จะถูกส่งจากปลายทางที่ Commerce ถูกสร้าง \*.(commerce.dynamics.com) สถิตสามารถแคชได้เฉพาะเมื่อชื่อโฮสต์หรือปลายทางที่สร้าง Commerce ถูกวางอยู่หลัง CDN

## <a name="set-up-ssl"></a>ตั้งค่า SSL

หลังจากที่คุณจัดเตรียมสภาพแวดล้อม Commerce กับโดเมนแบบกำหนดเองที่ให้ไว้ หรือหลังจากที่คุณระบุโดเมนที่กำหนดเองสำหรับสภาพแวดล้อมของคุณ โดยใช้คำขอการบริการ คุณต้องทำงานกับทีมเตรียมความพร้อมของ Commerce เพื่อวางแผนการเปลี่ยนแปลง DNS

ดังที่ได้กล่าวถึงก่อนหน้านี้ ชื่อโฮสต์หรือปลายทางที่สร้างขึ้นจะสนับสนุนใบรับรอง SSL สำหรับ \*.commerce.dynamics.com เท่านั้น ไม่สนับสนุน SSL สำหรับโดเมนที่กำหนดเอง

## <a name="cdn-services"></a>การบริการ CDN

บริการ CDN ใดๆ สามารถใช้กับสภาพแวดล้อม Commerce ได้ นี่คือ สองตัวอย่าง:

- **Microsoft Azure Front Door Service** – โซลูชัน Azure CDN สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Front Door Service ของ Azure ดู [Azure Front Door Service Documentation](/azure/frontdoor/)
- **Akamai Dynamic Site Accelerator** – สำหรับข้อมูลเพิ่มเติม ดู [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp)

## <a name="cdn-setup"></a>การตั้งค่า CDN

กระบวนการติดตั้ง CDN ประกอบด้วยขั้นตอนทั่วไปเหล่านี้:

1. เพิ่มโฮสต์ front-end
1. ตั้งค่าคอนฟิกกลุ่ม back-end
1. ตั้งค่ากฎการกำหนดเส้นทาง

### <a name="add-a-front-end-host"></a>เพิ่มโฮสต์ front-end

คุณสามารถใช้บริการ CDN ใดๆได้ แต่ตัวอย่างในบทความนี้ จะใช้ Front Door Service ของ Azure 

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่า Front Door Service ่ของ Azure [เริ่มต้นแบบด่วน: สร้าง Front Door สำหรับโปรแกรมประยุกต์เว็บสากลที่พร้อมใช้งานอย่างสูง](/azure/frontdoor/quickstart-create-front-door)

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>ตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure

การตั้งค่าคอนฟิกกลุ่ม back-end ใน Front Door Service ของ Azure ให้ทำตามขั้นตอนต่อไปนี้

1. เพิ่ม **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ลงในกลุ่มเสริมเป็นโฮสต์ที่ศุลกากรที่มีส่วนหัวของโฮสต์เสริมที่เหมือนกับ **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**
1. ภายใต้ **สร้างสมดุลในการโหลด** ให้เว้นค่าเริ่มต้น
1. ปิดใช้งานการตรวจสอบความสมบูรณ์ของกลุ่มเสริม

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure โดยมีการป้อนชื่อโฮสต์ back-end

![เพิ่มกล่องโต้ตอบกลุ่ม backend](./media/CDN_BackendPool.png)

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **เพิ่มกลุ่ม back-end** ใน Front Door Service ของ Azure ด้วยค่าเริ่มต้นการสร้างสมดุลในการโหลด

![เพิ่มกล่องโต้ตอบกลุ่ม back-end ต่อไป](./media/CDN_BackendPool_2.png)

> [!NOTE]
> ตรวจสอบให้แน่ใจว่าได้ปิดใช้งาน **ปัญหาสุขภาพ** เมื่อตั้งค่าบริการ Front Door Service ของ Azure ของคุณเองใน Commerce


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


> [!WARNING]
> หากโดเมนที่คุณจะใช้เปิดใช้งานอยู่และมีอยู่แล้ว ให้สร้างตั๋วการสนับสนุนจากไทล์ **สนับสนุน** ใน [Lifecycle Services ของ Microsoft Dynamics ](https://lcs.dynamics.com/) เพื่อรับความช่วยเหลือสำหรับขั้นตอนถัดไป สำหรับข้อมูลเพิ่มเติม โปรดดู [รับการสนับสนุนสำหรับแอปการเงินและการดำเนินงาน หรือ Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md)

หากโดเมนของคุณใหม่และไม่ใช่ไลฟ์โดเมนที่มีอยู่ก่อนหน้านี้ คุณสามารถเพิ่มโดเมนที่กำหนดเองของคุณในการตั้งค่าคอนฟิกสำหรับ Front Door Service ของ Azure การทำเช่นนี้จะเปิดใช้งานการรับส่งผ่านเว็บเพื่อให้ตรงกับไซต์ของคุณผ่านทางอินสแตนซ์ Front Door ของ Azure การเพิ่มโดเมนแบบกำหนดเอง (ตัวอย่างเช่น `www.fabrikam.com`) คุณต้องตั้งค่าคอนฟิก Canonical Name (CNAME) สำหรับโดเมน

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **การตั้งค่าคอนฟิก CNAME** ใน Front Door Service ของ Azure

![กล่องโต้ตอบการตั้งค่าคอนฟิก CNAME](./media/CNAME_Configuration.png)

คุณสามารถใช้ Front Door Service ของ Azure เพื่อจัดการใบรับรอง หรือคุณสามารถใช้ใบรับรองของคุณเองสำหรับโดเมนที่กำหนดเอง

ภาพประกอบต่อไปนี้แสดงกล่องโต้ตอบ **Custom Domain HTTPS** ใน Front Door Service ของ Azure

![กล่องโต้ตอบ Custom Domain HTTPS](./media/Custom_Domain_HTTPS.png)

สำหรับคำแนะนำโดยละเอียดเกี่ยวกับการเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของ Azure ของคุณ ให้ดูที่ [การเพิ่มโดเมนที่กำหนดเองลงใน Front Door ของคุณ](/azure/frontdoor/front-door-custom-domain)

ตอนนี้ CDN ของคุณควรได้รับการตั้งค่าคอนฟิกอย่างถูกต้อง เพื่อให้สามารถใช้กับไซต์ Commerce ของคุณได้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตัวเลือกการใช้งานเครือข่ายการจัดส่งเนื้อหา](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
