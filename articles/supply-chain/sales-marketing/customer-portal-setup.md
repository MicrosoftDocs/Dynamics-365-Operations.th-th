---
title: ติดตั้ง ตั้งค่า และอัพเดทพอร์ทัลของลูกค้า
description: บทความนี้แสดงรายละเอียดของการให้สิทธิ์ใช้งาน และคำแนะนำการตั้งค่าสำหรับพอร์ทัลลูกค้า
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8344212e66cb57ea8c9d4e8c2cdfbf022bc199c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850596"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>ติดตั้ง ตั้งค่า และอัพเดทพอร์ทัลของลูกค้า

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>ข้อกำหนดสิทธิใช้งาน

เมื่อต้องการใช้งานพอร์ทัลลูกค้า คุณต้องมีสิทธิ์ใช้งานดังต่อไปนี้

- **พอร์ทัล Power Apps** – สิทธิ์การใช้งานนี้จำเป็นต้องใช้เพื่อโฮสต์พอร์ทัลของลูกค้า พอร์ทัลจะได้รับสิทธิ์ใช้งานตามการใช้งาน สำหรับข้อมูลเพิ่มเติม ดูที่ [พอร์ทัล Power Apps ข้อกำหนดสิทธิใช้งาน](/power-platform/admin/powerapps-flow-licensing-faq#portals)
- **การรวมแบบสองทิศทาง** – คุณต้องมีสิทธิ์การใช้งานที่จำเป็นเพื่อเปิดใช้งานการรวมแบบสองทิศทางสำหรับตาราง Supply Chain Management สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ความต้องการของระบบสำหรับการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>การดำเนินการที่ขึ้นกับการรวมแบบสองทิศทาง และพอร์ทัล Power Apps

พอร์ทัลลูกค้าจะขึ้นอยู่กับพอร์ทัล Power Apps และการรวมแบบสองทิศทาง ดังที่แสดงในภาพประกอบต่อไปนี้

![ความเชื่อมโยงของพอร์ทัลลูกค้า](media/customer-portal-elements.png "ความเชื่อมโยงของพอร์ทัลลูกค้า")

ซึ่งแตกต่างจากลักษณะการทำงานอื่น ๆ จาก Supply Chain Management เทมเพลตพอร์ทัลลูกค้าจะอยู่ในพอร์ทัล Power Apps เพราะฉะนั้น พอร์ทัลลูกค้าจะถูกจำกัดโดยฟังก์ชันและความสามารถที่มาจากพอร์ทัล Power Apps และตารางในการรวมแบบสองทิศทาง

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a> การตั้งค่าที่จำเป็นเพื่อเปิดใช้งานพอร์ทัลลูกค้า

หลังจากที่คุณตรวจสอบให้แน่ใจว่าคุณมีสิทธิใช้งานแล้ว จำเป็นคุณสามารถตั้งค่าการรวมแบบสองทิศทาง ตามที่อธิบายไว้ใน [คำแนะนำการซิงโครไนส์เริ่มต้นของการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md)

ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแมปตารางต่อไปนี้ในการรวมแบบสองทิศทาง:

- ส่วนหัวของใบสั่งขาย
- รายละเอียดใบสั่งขาย
- บัญชี
- ผู้ติดต่อ
- ผลิตภัณฑ์

หลังจากที่การตั้งค่านี้เสร็จสมบูรณ์ คุณสามารถจัดเตรียมเทมเพลตพอร์ทัลลูกค้าได้

## <a name="provision-the-customer-portal"></a>การจัดเตรียมพอร์ทัลลูกค้า

ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าคุณได้ทำการ [ตั้งค่าที่จำเป็น](#required-setup) เสร็จเรียบร้อยแล้ว ให้ทำตามขั้นตอนต่อไปนี้เพื่อจัดเตรียมพอร์ทัลลูกค้า

1. ไปที่ [make.powerapps.com](https://make.powerapps.com/)
2. ตรวจสอบให้แน่ใจว่าคุณกำลังใช้สภาพแวดล้อมที่คุณเปิดใช้งานการรวมแบบสองทิศทาง
3. บนแท็บ **สร้าง** เลื่อนลงไปที่ส่วน **เริ่มต้นจากเทมเพลต** และเลือกเทมเพลตที่มีชื่อว่า **พอร์ทัลของลูกค้า**
4. ทำตามคำแนะนำบนหน้าจอ

หลังจากการเตรียมเสร็จสมบูรณ์ แล้วคุณสามารถเข้าถึงพอร์ทัลของลูกค้าในส่วน **แอปของคุณ** จาก **โฮม** เพจ

> [!NOTE]
> ถ้าไม่ได้ติดตั้งโซลูชันการรวมแบบสองทิศทางในสภาพแวดล้อมที่คุณกำลังทำงานอยู่ คุณจะได้รับข้อความแสดงข้อผิดพลาดและไม่สามารถเตรียมใช้งานพอร์ทัลของลูกค้าได้

## <a name="update-the-customer-portal"></a>อัพเดทพอร์ทัลลูกค้า

ฟังก์ชันเพิ่มเติมอาจถูกเพิ่มเข้าในพอร์ทัลลูกค้าในภายหลัง การเปลี่ยนแปลงใด ๆ ที่ Microsoft ทำกับส่วนประกอบของโซลูชันพื้นฐาน จะปรากฏในสภาพแวดล้อมของคุณโดยอัตโนมัติ อย่างไรก็ตาม เว็บไซต์ที่กำลังเตรียมใช้งานในสภาพแวดล้อมของคุณ จะไม่สะท้อนถึงการเปลี่ยนแปลงที่เกิดขึ้นกับข้อมูลการตั้งค่าคอนฟิกโดยอัตโนมัติ คุณจะต้องใช้การเปลี่ยนแปลงดังกล่าวด้วยตนเอง โดยการรับโค้ดจากเทมเพลตใหม่และรวมกับเว็บไซต์ที่ถูกเตรียมแล้ว

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

เมื่อต้องการเรียนรู้ว่าคุณสามารถตั้งค่าและกำหนดค่าพอร์ทัลของลูกค้าเองได้อย่างไร คุณควรเริ่มต้นด้วยการดูเอกสารประกอบต่อไปนี้สำหรับเทคโนโลยีพื้นฐานดังนี้

- [เอกสารพอร์ทัล Power Apps](/powerapps/maker/portals/overview)
- [เอกสารการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

ในการจัดการพอร์ทัลของคุณอย่างมีประสิทธิภาพ คุณต้องเข้าใจพอร์ทัล Power Apps และวงจรของ Microsoft Dataverse สำหรับข้อมูลเพิ่มเติม ให้ดูทรัพยากรต่อไปนี้:

- [เกี่ยวกับวงจรชีวิตของพอร์ทัล](/powerapps/maker/portals/admin/portal-lifecycle)
- [อัพเกรดพอร์ทัล](/powerapps/maker/portals/admin/upgrade-portal)
- [ย้ายการตั้งค่าคอนฟิกพอร์ทัล](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: แอป Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]