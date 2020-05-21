---
title: ป้ายทะเบียนที่ได้รับผ่านทางแอปคลังสินค้า
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าแอปคลังสินค้า เพื่อสนับสนุนการใช้กระบวนการรับป้ายทะเบียนเพื่อรับสินค้าคงคลังที่มีอยู่จริง
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346387"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>ป้ายทะเบียนที่ได้รับผ่านทางแอปคลังสินค้า

หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าแอปคลังสินค้า เพื่อให้สนับสนุนการใช้กระบวนการรับป้ายทะเบียนเพื่อรับสินค้าคงคลังที่มีอยู่จริง

คุณสามารถใช้ฟังก์ชันนี้เพื่อบันทึกการรับสินค้าคงคลังขาเข้าที่เกี่ยวข้องกับใบแจ้งเตือนการจัดส่งล่วงหน้า (ASN) อย่างรวดเร็ว ระบบจะสร้าง ASN โดยอัตโนมัติ เมื่อมีการใช้กระบวนการจัดการคลังสินค้าเพื่อจัดส่งใบสั่งโอนย้าย สำหรับกระบวนการใบสั่งซื้อ ASN สามารถถูกบันทึกด้วยตนเอง หรือสามารถถูกนำเข้าได้โดยอัตโนมัติโดยใช้กระบวนการเอนทิตี้ข้อมูล ASN ขาเข้า

ข้อมูล ASN ถูกเชื่อมโยงกับการโหลดและการจัดส่งผ่านทาง *โครงสร้างการบรรจุ* ที่ซึ่งแท่นวางสินค้า (ป้ายทะเบียนหลัก) สามารถมีกรอบได้ (แผ่นป้ายทะเบียนที่ซ้อนกัน)

> [!NOTE]
> เมื่อต้องการลดจำนวนของรายการความเคลื่อนไหวของสินค้าคงคลัง เมื่อมีการใช้โครงสร้างการจัดส่งที่มีการใช้ป้ายทะเบียนที่ซ้อนกัน ระบบจะบันทึกปริมาณคงคลังคงเหลือที่มีอยู่จริงบนป้ายทะเบียนหลัก เมื่อต้องการทริกเกอร์การเคลื่อนไหวของปริมาณคงคลังคงเหลือที่มีอยู่จริงจากป้ายทะเบียนหลักไปยังป้ายทะเบียนที่ซ้อนกัน โดยยึดตามข้อมูลโครงสร้างการบรรจุ อุปกรณ์เคลื่อนที่ต้องมีรายการเมนูที่ยึดตามกระบวนการสร้างงาน *บรรจุไปยังป้ายทะเบียนที่ซ้อนกัน*

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>แสดงหรือข้ามหน้าสรุปการรับสินค้า

คุณสามารถใช้คุณลักษณะ *ควบคุมว่าจะแสดงหน้าสรุปการรับสินค้าบนอุปกรณ์เคลื่อนที่* เพื่อใช้ประโยชน์จากขั้นตอนของแอปคลังสินค้าโดยละเอียดเพิ่มเติม โดยเป็นส่วนหนึ่งของกระบวนการรับป้ายทะเบียน

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *ควบคุมว่าจะแสดงหน้าสรุปการรับสินค้าบนอุปกรณ์เคลื่อนที่หรือไม่*

เมื่อเปิดใช้งานคุณลักษณะนี้ รายการเมนูบนอุปกรณ์เคลื่อนที่สำหรับการรับป้ายทะเบียน หรือการรับป้ายทะเบียนการรับสินค้าและการย้ายเก็บจะให้การตั้งค่า **หน้าแสดงการสรุปการรับสินค้า** การตั้งค่านี้มีตัวเลือกดังต่อไปนี้:

- **แสดงสรุปโดยละเอียด** – ในระหว่างการรับป้ายทะเบียน ผู้ปฏิบัติงานจะเห็นหน้าพิเศษที่แสดงข้อมูล ASN แบบเต็ม
- **ข้ามสรุป** – ผู้ปฏิบัติงานจะไม่เห็นข้อมูล ASN แบบเต็ม นอกจากนี้ ผู้ปฏิบัติงานคลังสินค้าจะยังไม่สามารถตั้งค่ารหัสการโอนการครอบครอง หรือเพิ่มข้อยกเว้น ในระหว่างกระบวนการรับสินค้าได้

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>ป้องกันใบสั่งโอนย้าย ป้ายทะเบียนที่ส่ง ไม่ให้ถูกใช้ที่คลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง

ไม่สามารถใช้กระบวนการรับป้ายทะเบียนได้ ถ้า ASN มีรหัสป้ายทะเบียนอยู่แล้ว และมีข้อมูลปริมาณคงเหลือที่มีอยู่จริงที่สถานที่คลังสินค้าอื่นที่ไม่ใช่สถานที่คลังสินค้าที่มีการลงทะเบียนป้ายทะเบียนเกิดขึ้น

สำหรับสถานการณ์ใบสั่งโอนย้ายที่ซึ่งคลังสินค้าส่งต่อไม่ได้ติดตามป้ายทะเบียน (และดังนั้น จึงไม่สามารถติดตามปริมาณคงคลังคงเหลือที่มีอยู่จริงสำหรับป้ายทะเบียนแต่ละแผ่น) คุณสามารถใช้คุณลักษณะ *ป้องกันใบสั่งโอนย้ายที่จัดส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นๆ นอกเหนือจากคลังสินค้าปลายทาง* เพื่อป้องกันการอัปเดตปริมาณคงคลังคงเหลือของป้ายทะเบียนที่อยู่ระหว่างการส่งต่อ

ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:

- **โมดูล:** *การจัดการคลังสินค้า*
- **ชื่อคุณลักษณะ:** *ป้องกันใบสั่งโอนย้ายที่ส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง*

เมื่อต้องการจัดการฟังก์ชันเมื่อคุณลักษณะนี้พร้อมใช้งาน ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**
1. บนแท็บ **ทั่วไป** บน FastTab **ป้ายทะเบียน** ให้ตั้งค่าฟิลด์ **นโยบายส่งต่อป้ายทะเบียนของคลังสินค้า** เป็นค่าใดค่าหนึ่งต่อไปนี้:

    - **อนุญาตให้ใช้ป้ายทะเบียนที่ไม่มีการติดตามอีกครั้ง** – ระบบทำงานในลักษณะเดียวกันกับทำงานเมื่อคุณลักษณะ *ป้องกันใบสั่งโอนย้ายที่จัดส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง* ไม่พร้อมใช้งาน ค่านี้เป็นการตั้งค่าเริ่มต้น เมื่อคุณเรียกใช้งานคุณลักษณะเป็นครั้งแรก
    - **ป้องกันไม่ให้มีการนำป้ายทะเบียนที่ไม่มีการติดตามไปใช้ซ้ำ** – เฉพาะการอัปเดตปริมาณคงเหลือที่เกี่ยวข้องกับป้ายทะเบียนที่จัดส่งเท่านั้นที่จะได้รับอนุญาตที่คลังสินค้าปลายทาง จนกว่าจะได้รับใบสั่งโอนย้าย

## <a name="more-information"></a>ข้อมูลเพิ่มเติม

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเมนูบนอุปกรณ์เคลื่อนที่ ให้ดูที่ [ตั้งค่าอุปกรณ์เคลื่อนที่สำหรับงานของคลังสินค้า](configure-mobile-devices-warehouse.md)
