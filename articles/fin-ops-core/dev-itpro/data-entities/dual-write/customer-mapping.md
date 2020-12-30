---
title: ข้อมูลหลักของลูกค้าแบบรวม
description: ในหัวข้อนี้อธิบายการรวมข้อมูลลูกค้าระหว่าง Finance and Operations กับ Dataverse
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
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685650"
---
# <a name="integrated-customer-master"></a>ข้อมูลหลักของลูกค้าแบบรวม

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


ข้อมูลลูกค้าสามารถทำเป็นต้นฉบับได้ในแอพลิเคชัน Dynamics 365 มากกว่าหนึ่งรายการ ตัวอย่างเช่น แถวลูกค้าสามารถเริ่มต้นได้ผ่านทางกิจกรรมการขายใน Dynamics 365 Sales (แอปที่เป็นแบบโมเดลใน Dynamics 365) หรือแถวสามารถเริ่มต้นได้ผ่านทางกิจกรรมการขายปลีกใน Dynamics 365 Commerce (แอป Finance and Operations) ไม่ว่าข้อมูลลูกค้าที่มีต้นกำเนิดมาจากที่ใดก็ตาม จะมีการรวมอยู่เบื้องหลัง ข้อมูลหลักของลูกค้าแบบรวมช่วยให้คุณมีความยืดหยุ่นในการเข้าถึงข้อมูลลูกค้าในแอพลิเคชัน Dynamics 365 และให้มุมมองที่ครอบคลุมของลูกค้าทั่วทั้งชุดแอพลิเคชัน Dynamics 365

## <a name="customer-data-flow"></a>โฟลว์ข้อมูลของลูกค้า

*ลูกค้า* เป็นแนวคิดที่กำหนดไว้อย่างดีในแอปพลิเคชัน ดังนั้น การรวมของข้อมูลลูกค้าก็เกี่ยวข้องกับความสอดคล้องแนวคิดของลูกค้าระหว่างสองแอพลิเคชัน ภาพประกอบต่อไปนี้แสดงโฟลว์ข้อมูลของลูกค้า

![โฟลว์ข้อมูลของลูกค้า](media/dual-write-customer-data-flow.png)

ลูกค้าสามารถแบ่งออกย่างกว้างๆ ได้เป็นสองประเภท: ลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้ ลูกค้าสองประเภทนี้ถูกจัดเก็บและจัดการแตกต่างกันไปใน Finance and Operations และ Dataverse

ใน Finance and Operations ทั้งลูกค้าเชิงพาณิชย์ / องค์กรและผู้บริโภค / ผู้ใช้จะเชี่ยวชาญในตารางเดียวที่มีชื่อว่า **CustTable** (CustCustomerV3Entity) และจะถูกแบ่งออกตามแอตทริบิวต์ **ชนิด** (ถ้า **ชนิด** ถูกตั้งค่าเป็น **องค์กร** ลูกค้าเป็นลูกค้าเชิงพาณิชย์/เชิงองค์กร และถ้ามีการตั้งค่า **ชนิด** เป็น **บุคคล** ลูกค้าเป็นผู้บริโภค/ผู้ใช้) ข้อมูลผู้ติดต่อหลักจะได้รับการจัดการผ่านเอนทิตี SMMContactPersonEntity

ใน Dataverse ลูกค้าเชิงพาณิชย์/เชิงองค์กรมีความเชี่ยวชาญในเอนทิตีบัญชี และถูกระบุเป็นลูกค้า เมื่อมีการตั้งค่าแอททริบิวต์ **RelationshipType** เป็น **ลูกค้า** ทั้งผู้บริโภค/ผู้ใช้และผู้ติดต่อจะถูกแสดงโดยเอนทิตีผู้ติดต่อ เพื่อให้การแยกที่ชัดเจนระหว่างผู้บริโภค/ผู้ใช้ และผู้ติดต่อ เอนทิตี **ผู้ติดต่อ** มีแฟล็กบูลีนที่มีชื่อว่า **Sellable** เมื่อ **Sellable** เป็น **จริง** ผู้ติดต่อเป็นผู้บริโภค/ผู้ใช้ และสามารถสร้างใบเสนอราคาและใบสั่งสำหรับผู้ติดต่อนั้นได้ เมื่อ **Sellable** เป็น **เท็จ** ผู้ติดต่อเป็นเพียงผู้ติดต่อหลักของลูกค้า

เมื่อผู้ติดต่อที่ไม่ใช่ Sellable มีส่วนร่วมในกระบวนการใบเสนอราคาหรือใบสั่ง **Sellable** ถูกตั้งค่าเป็น **จริง** เพื่อแฟล็กผู้ติดต่อเป็นผู้ติดต่อ Sellable ผู้ติดต่อที่กลายเป็นผู้ติดต่อที่สามารถขายได้ยังคงเป็นผู้ติดต่อ Sellable

## <a name="templates"></a>เท็มเพลต

ข้อมูลลูกค้ารวมถึงข้อมูลทั้งหมดเกี่ยวกับลูกค้า เช่น กลุ่มลูกค้า ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และสถานะบัตรสมาชิก ชุดของแผนผังตารางทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอป Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365         | คำอธิบาย
----------------------------|---------------------------------|------------
ผู้ติดต่อ CDS V2             | ผู้ติดต่อ                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลการติดต่อหลัก ทุติยภูมิ และตติยภูมิสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
กลุ่มลูกค้า             | msdyn_customergroups            | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลกลุ่มลูกค้า
วิธีการชำระเงินของลูกค้า     | msdyn_customerpaymentmethods    | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลวิธีการชำระเงิน
ลูกค้า V3                | บัญชี                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับลูกค้าเชิงพาณิชย์และเชิงองค์กร
ลูกค้า V3                | ผู้ติดต่อ                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับผู้บริโภคและผู้ใช้ปลายทาง
ส่วนเพิ่มของชื่อ                | msdyn_nameaffixes               | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของส่วนเพิ่มของชื่อสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการแสดงวันที่ในการชำระเงินของ CDS V2    | msdyn_paymentdaylines           | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของบรรทัดวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
CDS จำนวนวันการชำระเงิน            | msdyn_paymentdays               | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการกำหนดการชำระเงิน      | msdyn_paymentschedulelines      | ซิงค์ข้อมูลอ้างอิงของบรรทัดกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
กำหนดการชำระเงิน            | msdyn_paymentschedules          | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
เงื่อนไขการชำระเงิน            | msdyn_paymentterms              | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของเงื่อนไขการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
