---
title: ตั้งค่าลำดับชั้นขององค์กร
description: หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997786"
---
# <a name="set-up-organization-hierarchies"></a>ตั้งค่าลำดับชั้นขององค์กร


[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

ก่อนที่จะสร้างช่องทาง คุณต้องตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าลำดับชั้นขององค์กรของคุณแล้ว

คุณสามารถใช้ลำดับชั้นขององค์กรเพื่อดู และรายงานในบธุรกิจของคุณจากมุมมองต่างๆได้ ตัวอย่างเช่น คุณสามารถตั้งค่าหนึ่งลำดับชั้นสำหรับภาษี ทางกฎหมาย หรือการรายงานตามกฎหมาย จากนั้นคุณสามารถตั้งค่าอีกลำดับชั้นได้เพื่อรายงานข้อมูลทางการเงินที่ไม่จำเป็นทางกฎหมาย แต่ถูกใช้เป็นการรายงานภายใน

ก่อนที่คุณจะสร้างลำดับชั้นขององค์กร คุณต้องสร้างองค์กร สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างนิติบุคคล](channels-legal-entities.md) หรือ [สร้างหน่วยปฏิบัติงาน](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)


สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:
- [ภาพรวมขององค์กรและลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [วางแผนลำดับชั้นขององค์กรของคุณ](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [สร้างลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>สร้างลำดับชั้นขององค์กร

หากต้องการสร้างลำดับชั้นองค์กร ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ลำดับชั้นขององค์กร**
1. บนหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง
1. ในส่วน **วัตถุประสงค์** เลือก **กำหนดวัตถุประสงค์**
1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ เลือกวัตถุประสงค์เพื่อกำหนดให้กับลำดับชั้นขององค์กรของคุณ
1. ในส่วน **ลำดับชั้นที่กำหนด** เลือก **เพิ่ม**
1. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก ค้นหาลำดับชั้นที่คุณเพิ่งสร้างขึ้น
1. เลือก **ตกลง**

รูปภาพต่อไปนี้แสดงตัวอย่างของลำดับชั้นขององค์กรที่สร้างขึ้นสำหรับชุดของร้านค้า "Adventure Works" แบบสมมติ

![ตัวอย่างลำดับชั้นขององค์กร](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>เพิ่มองค์กรให้กับลำดับชั้น

หากต้องการเพิ่มองค์กรให้กับลำดับชั้น ให้ทำตามขั้นตอนต่อไปนี้

1. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ เลือกลำดับชั้นของคุณ
1. บนบานหน้าต่างการดำเนินการ เลือก **ดู**
1. เพิ่มองค์กรตามความจำเป็น
1. เมื่อต้องการเพิ่มองค์กร ให้เลือก **แก้ไข** และจากนั้นเลือก **แทรก** เมื่อคุณดำเนินการเปลี่ยนแปลงเสร็จสิ้น คุณสามารถบันทึกแบบร่างและเผยแพร่การเปลี่ยนแปลงได้

รูปภาพต่อไปนี้แสดงนิติบุคคลที่เพิ่มที่รากลำดับชั้นกับศูนย์ต้นทุนสี่ศูนย์ที่เพิ่มสำหรับช่องทาง "ขนาดเล็ก" "ช่องระบาย" "ออนไลน์" และ "ศูนย์บริการ" คุณสามารถเพิ่มร้านค้าปลีก ศูนย์บริการ และช่องทางออนไลน์ต่าง ๆ เข้าในแต่ละที่ได้

![ตัวอย่างของตัวออกแบบลำดับชั้น](media/hierarchy-designer.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมขององค์กรและลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[วางแผนลำดับชั้นขององค์กรของคุณ](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[สร้างนิติบุคคล](channels-legal-entities.md)

[สร้างหน่วยปฏิบัติงาน](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[ภาพรวมของช่องทาง](channels-overview.md)

[ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]