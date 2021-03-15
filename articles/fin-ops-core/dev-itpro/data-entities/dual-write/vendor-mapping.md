---
title: ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Dataverse
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f2fc88ed0c0f4dbec55f8ca251cca3d071760b55
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744526"
---
# <a name="integrated-vendor-master"></a>ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



คำว่า *ผู้จัดจำหน่าย* อ้างอิงถึงองค์กรของซัพพลายเออร์ หรือเจ้าของรายเดียวที่จัดหาสินค้าหรือบริการให้กับธุรกิจ แม้ว่า *ผู้จัดจำหน่าย* เป็นแนวคิดที่สร้างขึ้นใน Microsoft Dynamics 365 Supply Chain Management จะไม่มีแนวคิดของผู้จัดจำหน่ายอยู่ในแอปที่เป็นแบบโมเดลใน Dynamics 365 อย่างไรก็ตาม คุณสามารถโอเวอร์โหลดตาราง **บัญชี/ผู้ติดต่อ** เพื่อจัดเก็บข้อมูลของผู้จัดจำหน่าย ข้อมูลหลักของผู้จัดจำหน่ายแบบรวมจะแนะนำแนวคิดของผู้จัดจำหน่ายที่ชัดเจนในแอปที่เป็นแบบโมเดลใน Dynamics 365 คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายใหม่หรือข้อมูลผู้จัดจำหน่ายร้านค้าในตาราง **บัญชี/ผู้ติดต่อ** การรวมแบบสองทิศทางสนับสนุนทั้งสองวิธี

ในทั้งสองวิธีการ ข้อมูลผู้จัดจำหน่ายจะถูกรวมกันระหว่างพอร์ทัล Dynamics 365 Supply Chain Management Dynamics 365 Sales Dynamics 365 Field Service และ Power Apps ใน Supply Chain Management ข้อมูลจะพร้อมใช้งานสำหรับลำดับงาน เช่น ใบขอซื้อ และใบสั่งซื้อ

## <a name="vendor-data-flow"></a>โฟลว์ข้อมูลของผู้จัดจำหน่าย

ถ้าคุณไม่ต้องการจัดเก็บข้อมูลในตาราง **บัญชี/ผู้ติดต่อ** ใน Dataverse คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายใหม่ได้

![โฟลว์ข้อมูลของผู้จัดจำหน่าย](media/dual-write-vendor-data-flow.png)

ถ้าคุณไม่ต้องการจัดเก็บข้อมูลของผู้จัดจำหน่ายต่อในตาราง **บัญชี/ผู้ติดต่อ** คุณสามารถใช้การออกแบบของผู้จัดจำหน่ายแบบขยายได้ เมื่อต้องการใช้การออกแบบของผู้จัดจำหน่ายแบบขยาย คุณต้องตั้งค่าคอนฟิกลำดับงานของผู้จัดจำหน่ายในแพคเกจโซลูชันการรวมแบบสองทิศทาง สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สลับระหว่างการออกแบบของผู้จัดจำหน่าย](vendor-switch.md)

![โฟลว์ข้อมูลของผู้จัดจำหน่ายแบบขยาย](media/dual-write-vendor-detail.jpg)

> [!TIP]
> ถ้าคุณกำลังใช้พอร์ทัล Power Apps สำหรับผู้จัดจำหน่ายแบบบริการตนเอง ข้อมูลของผู้จัดจำหน่ายสามารถโฟลว์ไปยังแอป Finance and Operations ได้โดยตรง

## <a name="templates"></a>เท็มเพลต

ข้อมูลผู้จัดจำหน่ายรวมถึงข้อมูลทั้งหมดเกี่ยวกับผู้จัดจำหน่าย เช่น กลุ่มผู้จัดจำหน่าย ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และโพรไฟล์ใบแจ้งหนี้ คอเลคชันของแม็บตารางทำงานร่วมกันในขณะการรวมข้อมูลผู้จัดจำหน่าย ดังที่แสดงในตารางต่อไปนี้

แอป Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365     | คำอธิบาย
----------------------------|-----------------------------|------------
ผู้จัดจำหน่าย V2                   | บัญชี                     | ธุรกิจที่ใช้ตารางบัญชีเพื่อจัดเก็บข้อมูลผู้จัดจำหน่ายสามารถใช้ต่อไปได้ในลักษณะเดียวกัน นอกจากนี้ ยังสามารถใช้ประโยชน์จากฟังก์ชันของผู้จัดจำหน่ายที่ชัดเจนซึ่งกำลังจะมา เนื่องจากการรวมของแอป Finance and Operations
ผู้จัดจำหน่าย V2                   | Msdyn\_vendors              | ธุรกิจที่ใช้โซลูชันแบบกำหนดเองสำหรับผู้จัดจำหน่ายสามารถใช้ประโยชน์จากแนวคิดผู้จัดจำหน่ายแบบสำเร็จรูปที่ถูกนำมาใช้ใน Dataverse เนื่องจากการรวมของแอป Finance and Operations 
กลุ่มผู้จัดจำหน่าย               | msdyn\_vendorgroups         | เท็มเพลตนี้รวมข้อมูลกลุ่มผู้จัดจำหน่ายเข้าด้วยกัน
วิธีการชำระเงินของผู้จัดจำหน่าย       | msdyn\_vendorpaymentmethods | เท็มเพลตนี้รวมข้อมูลวิธีการชำระเงินของผู้จัดจำหน่วยเข้าด้วยกัน
ผู้ติดต่อ CDS V2             | ผู้ติดต่อ                    | เท็มเพลต [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) รวมข้อมูลผู้ติดต่อ ปฐมภูม ทุติยภูมิ ตติยภูมิ ทั้งหมดเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการกำหนดการชำระเงิน      | msdyn\_paymentschedulelines | เท็มเพลต [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) รวมข้อมูลอ้างอิงสำหรับลูกค้าและผู้จัดจำหน่ายเข้าด้วยกัน
กำหนดการชำระเงิน            | msdyn\_paymentschedules     | เท็มเพลต [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) รวมข้อมูลอ้างอิงกำหนดการชำระิิเงินเข้าด้วยกัน ทั้งสำหรับลูกค้าและผู้จัดจำหน่าย
รายการแสดงวันที่ในการชำระเงินของ CDS V2    | msdyn\_paymentdaylines      | เท็มเพลต [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) รวมข้อมูลอ้างอิงกำหนดการชำระเงินเข้าด้วยกัน สำหรับลูกค้าและผู้จัดจำหน่าย
CDS จำนวนวันการชำระเงิน            | msdyn\_paymentdays          | เท็มเพลต [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) รวมข้่อมูลอ้างอิงวันชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
เงื่อนไขการชำระเงิน            | msdyn\_paymentterms         | เท็มเพลต [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) รวมข้อมูลอ้างอิงเงื่อนไขการชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
ส่วนเพิ่มของชื่อ                | msdyn\_nameaffixes          | เท็มเพลต [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) รวมข้อมูลอ้างอิงส่วนเพิ่มของชื่อเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]