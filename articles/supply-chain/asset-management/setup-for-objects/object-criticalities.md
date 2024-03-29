---
title: ประเภทการวิพากษ์วิจารณ์สินทรัพย์
description: บทความจะอธิบายชนิดการวิพากษ์วิจารณ์สินทรัพย์ในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfde9a9bc681c0d758491fc5c361b5b046e20d9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899511"
---
# <a name="asset-criticality-types"></a>ประเภทการวิพากษ์วิจารณ์สินทรัพย์

[!include [banner](../../includes/banner.md)]

 

บทความจะอธิบายชนิดการวิพากษ์วิจารณ์สินทรัพย์ในการจัดการสินทรัพย์ การวิพากษ์วิจารณ์สินทรัพย์เกี่ยวข้องกับสินทรัพย์ และจะถูกโอนย้ายไปยังใบสั่งงาน ไม่สามารถเปลี่ยนแปลงในใบสั่งงานได้ การวิพากษ์วิจารณ์สินทรัพย์ถูกใช้ในการคำนวณการวิพากษ์วิจารณ์ใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน กล่าวคือ มีการใช้ในการคำนวณขอบเขตที่งานบำรุงรักษาในสินทรัพย์มีผลต่อกำหนดการผลิตและผลผลิตในบริษัทของคุณ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าที่เกี่ยวข้องกับการคำนวณของคะแนนการจัดอันดับสำหรับการจัดกำหนดการใบสั่งงาน ดู [พารามิเตอร์การจัดการสินทรัพย์](../setup-for-objects/enterprise-asset-management-parameters.md)

ในการตั้งค่าการวิพากษ์วิจารณ์ อันดับแรกคุณจะสร้างชนิดของการวิพากษ์วิจารณ์ที่ควรใช้ในการตั้งค่าสินทรัพย์ จากนั้น คุณตั้งค่าการวิพากษ์วิจารณ์สินทรัพย์

## <a name="set-up-criticality-types"></a>ตั้งค่าชนิดการวิพากษ์วิจารณ์

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **ชนิดการวิพากษ์วิจารณ์**
2. เลือก **สร้าง** เพื่อสร้างเรกคอร์ด
3. ในฟิลด์ **การวิพากษ์วิจารณ์** ให้ป้อนหมายเลขที่บ่งชี้การวิพากษ์วิจารณ์
4. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับชนิดการวิพากษ์วิจารณ์
5. ในฟิลด์ **ปัจจัย** ให้ป้อนปัจจัย ปัจจัยนี้จะใช้ในระหว่างการคำนวณการจัดกำหนดการใบสั่งงาน เพื่อกำหนดเรกคอร์ดการวิพากษ์วิจารณ์ที่ควรใช้ (เรกคอร์ดที่มีการใช้ปัจจัยสูงสุดอยู่เสมอ) การตั้งค่านี้จะเกี่ยวข้องถ้า ดังที่แสดงในภาพประกอบต่อไปนี้ มีการสร้างรายการการวิพากษ์วิจารณ์ที่มีค่าการวิพากษ์วิจารณ์เดียวกัน

    ![หน้าชนิดการวิพากษ์วิจารณ์](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>ตั้งค่าการวิพากษ์วิจารณ์สินทรัพย์

1. เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **การวิพากษ์วิจารณ์สินทรัพย์**
2. เลือก **สร้าง** เพื่อสร้างเรกคอร์ด
3. โดยขึ้นอยู่กับระดับที่ต้องการของรายละเอียดสำหรับการวิพากษ์วิจารณ์สินทรัพย์ ทำให้การเลือกที่เกี่ยวข้องในฟิลด์ **ตำแหน่งที่ทำงาน** **ชนิดสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** **สินทรัพย์** **ประเภทชนิดงาน** **ชนิดงาน** **ตัวแปรชนิดงาน** และ **ข้อกำหนดเกี่ยวกับงาน**

    > [!NOTE]
    > เมื่อมีการเลือกการวิพากษ์วิจารณ์สินทรัพย์ การจัดการสินทรัพย์จะผ่านเรกคอร์ดการวิพากษ์วิจารณ์สินทรัพย์ทั้งหมดเพื่อตรวจสอบการจับคู่ที่เป็นไปได้ ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน กล่าวอีกนัยหนึ่งคือ อันดับแรกการจัดการสินทรัพย์จะตรวจสอบ **ข้อกำหนดเกี่ยวกับงาน** ถ้าไม่พบการจับคู่ จะตรวจสอบ **ตัวแปรชนิดงาน** ถ้าไม่พบการจับคู่ จะตรวจสอบ **ชนิดงาน** และอื่นๆ ดังที่คุณสามารถดูได้ในโครงร่างของหน้า ลักษณะการทำงานนี้หมายความว่า การค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์จะตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายสำหรับการจับคู่ ถ้าไม่พบการจับคู่ จะมีการใช้เรกคอร์ด "เริ่มต้น" ที่ไม่มีการใช้การเลือก

4. ในฟิลด์ **การวิพากษ์วิจารณ์** ให้เลือกหนึ่งในค่าการวิพากษ์วิจารณ์ที่คุณสร้างไว้ในกระบวนงานก่อนหน้านี้

### <a name="notes-about-criticality-setup"></a>บันทึกย่อเกี่ยวกับการตั้งค่าการวิพากษ์วิจารณ์

- ถ้าคุณเปลี่ยนแปลงการวิพากษ์วิจารณ์สินทรัพย์ในการตั้งค่านี้ หลังจากที่คุณได้ใช้ในใบสั่งงานแล้ว จะไม่มีการปรับปรุงการวิพากษ์วิจารณ์ในใบสั่งงานให้สอดคล้องกัน
- การวิพากษ์วิจารณ์ในใบสั่งงานจะถูกคำนวณใหม่ทุกครั้งที่มีการเพิ่มหรือลบรายการใบสั่งงานจากใบสั่งงาน
- ถ้าใบสั่งงานประกอบด้วยงานในใบสั่งงานหลายงาน การวิพากษ์วิจารณ์สูงสุด ตามฟิลด์ **ปัจจัย** ในหน้า **ชนิดการวิพากษ์วิจารณ์** จะใช้ในใบสั่งงานเสมอ
- โดยทั่วไป การวิพากษ์วิจารณ์สินทรัพย์สามารถเปลี่ยนแปลงได้ตลอดรอบระยะเวลา การวิพากษ์วิจารณ์อาจได้รับผลกระทบจากการซื้ออุปกรณ์ใหม่ การตกแต่งใหม่ และอื่นๆ พิจารณาการประเมินการวิพากษ์วิจารณ์สินทรัพย์ของคุณใหม่ในช่วงเวลาปกติ (ตัวอย่างเช่น ปีละครั้ง หรือปีเว้นปี) เพื่อให้แน่ใจว่าคำนิยามการวิพากษ์วิจารณ์ของคุณตรงกับการตั้งค่าการผลิตปัจจุบันของคุณ


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]