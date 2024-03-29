---
title: เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ
description: บทความนี้อธิบายวิธีการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9535be3161253e88083b5add7ac55c12364aa383
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875605"
---
# <a name="responsible-maintenance-workers"></a>เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ

[!include [banner](../../includes/banner.md)]

 

เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบสามารถเกี่ยวข้องกับชนิดของสินทรัพย์ สินทรัพย์ ตำแหน่งที่ทำงาน ประเภทของชนิดงานบำรุงรักษา ชนิดงานการบำรุงรักษา ตัวแปรชนิดงานการบำรุงรักษา และการซื้อขาย สามารถใช้ได้ในใบสั่งงานและคำขอการบำรุงรักษาเพื่อบ่งชี้การกำหนดลักษณะเกี่ยวกับเจ้าหน้าที่บำรุงรักษาที่ควรรับผิดชอบใบสั่งงาน (อย่างไรก็ตาม เจ้าหน้าที่บำรุงรักษาเหล่านั้นไม่จำเป็นต้องเป็นผู้ปฏิบัติงานคนเดียวกันที่ถูกจัดกำหนดเวลาให้ดำเนินการใบสั่งงาน) การใช้ฟังก์ชันนี้เป็นทางเลือก ตัวอย่างเช่น สามารถใช้เพื่อเลือกผู้ปฏิบัติงานที่รับผิดชอบหรือกลุ่มผู้ปฏิบัติงานสำหรับชนิดงานหรือพื้นที่ทำงานเฉพาะ

ในระหว่างวงจรการใช้งานใบสั่งงานหรือวงจรการใช้งานคำขอการบำรุงรักษา คุณสามารถเปลี่ยนหรือปรับปรุงเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ การเปลี่ยนแปลงหรือการปรับปรุงนี้อาจเกี่ยวข้องกับ ตัวอย่างเช่น การเปลี่ยนแปลงในสสถานะของวงจรการใช้ของคำขอการบำรุงรักษา หรือสถานะของวงจรการใช้ของใบสั่งงาน

การตั้งค่าในหน้า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ** *ไม่* ถูกใช้ในระหว่างการจัดกำหนดการใบสั่งาน

> [!NOTE]
> ในการจัดการสินทรัพย์ คุณยังสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษา *ที่ต้องการ* ซึ่งอาจถูกปันส่วนให้กับใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน

ก่อนที่คุณจะสามารถตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบได้ คุณต้องตั้งค่ากลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษาที่ควรพร้อมใช้งานสำหรับการเลือก สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่ากลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษา ดู [กลุ่มผู้ปฏิบัติงานและกลุ่มเจ้าหน้าที่บำรุงรักษา](../setup-for-objects/workers-and-worker-groups.md)

## <a name="set-up-responsible-maintenance-workers"></a>ตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ

1. เลือก **สินทรัพย์** \> **การตั้งค่า** \> **ผู้ปฏิบัติ** \> **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**
2. เลือก **สร้าง** เพื่อสร้างเรกคอร์ด
3. อันดับแรก สร้างการตั้งค่าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบเริ่มต้น หรือกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ ที่ซึ่งคุณตั้งค่าเฉพาะฟิลด์ **กลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ** และ/หรือฟิลด์ **ผู้ปฏิบัติงานที่รับผิดชอบ** ปล่อยให้ฟิลด์ที่เหลือว่างเปล่า การตั้งค่าเริ่มต้นนี้จะใช้ในระหว่างการจัดกำหนดการใบสั่งงาน ถ้าไม่มีรายการอื่น การรวมกันที่เฉพาะเจาะจงมากขึ้นจับคู่เนื้อหาของใบสั่งงาน

    > [!NOTE]
    > ในระหว่างการสร้างคำขอการบำรุงรักษา เมื่อเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบหรือกลุ่มเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ ถูกทำให้พร้อมใช้งานสำหรับการเลือกในหน้า **คำขอการบำรุงรักษาทั้งหมด** การจัดการสินทรัพย์จะผ่านเรกคอร์ดเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบเพื่อตรวจสอบการจับคู่ที่เป็นไปได้ ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน กล่าวคือ อันดับแรกการจัดการสินทรัพย์ตรวจสอบการจับคู่สำหรับฟิลด์ **การค้า** ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ตัวแปรชนิดงานบำรุงรักษา** ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **ชนิดงานบำรุงรักษา** เป็นต้น ดังที่คุณสามารถเห็นได้ในโครงร่างของหน้า ลักษณะการทำงานนี้หมายความว่า ในการค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์ตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายเพื่อจับคู่ (อันดับแรก **การค้า** จากนั้น **ตัวแปรชนิดงานบำรุงรักษา** จากนั้น **ชนิดงานบำรุงรักษา** จากนั้น **ประเภทของชนิดงานบำรุงรักษา** จากนั้น **ตำแหน่งที่ทำงาน** จากนั้น **สินทรัพย์** และสุดท้าย **ชนิดสินทรัพย์**) ถ้าไม่พบการจับคู่ จะมีการใช้เรกคอร์ดข้อมูลเริ่มต้นที่ไม่มีการเลือกในฟิลด์ทั้งเจ็ดฟิลด์

ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **เจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ**

![หน้าเจ้าหน้าที่บำรุงรักษาที่รับผิดชอบ](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]