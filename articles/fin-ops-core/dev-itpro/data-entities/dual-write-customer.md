---
title: ข้อมูลหลักของลูกค้าแบบรวม
description: หัวข้อนี้อธิบายการรวมของข้อมูลของลูกค้าระหว่าง Finance and Operations และ Common Data Service
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769694"
---
# <a name="integrated-customer-master"></a>ข้อมูลหลักของลูกค้าแบบรวม

[!include [banner](../includes/banner.md)]

เป็นเรื่องปกติสำหรับเรกคอร์ดลูกค้าที่จะมีความเชี่ยวชาญในแอพลิเคชันมากกว่าหนึ่งรายการ ตัวอย่างเช่น กิจกรรมการขายสามารถนำเรกคอร์ดลูกค้าเชิงพาณิชย์เข้ามาผ่านแอพลิเคชันทางการขายและ e-Commerce หรือการขายปลีกสามารถนำเรกคอร์ดลูกค้าเข้ามาผ่านแอพลิเคชัน Finance and Operations โดยไม่คำนึงถึงจุดกำเนิดของเรกคอร์ดลูกค้า จะมีการรวมอยู่เบื้องหลังในขอบเขตของแอพลิเคชันและความแตกต่างของโครงสร้างพื้นฐาน การพัฒนาความเชี่ยวชาญของลูกค้าแบบรวมช่วยจัดการสถานการณ์จำลองการพัฒนาความเชี่ยวชาญที่หลากหลาย และให้มุมมองที่ครอบคลุมของลูกค้าไปยังชุดแอพลิเคชัน Dynamics 365

## <a name="customer-data-flow"></a>โฟลว์ข้อมูลของลูกค้า

*ลูกค้า*เป็นแนวคิดที่กำหนดไว้อย่างดีในแอปพลิเคชัน ดังนั้น การรวมของข้อมูลลูกค้าก็เกี่ยวข้องกับความสอดคล้องแนวคิดของลูกค้าระหว่างสองแอพลิเคชัน ภาพประกอบต่อไปนี้แสดงโฟลว์ข้อมูลของลูกค้า

![โฟลว์ข้อมูลของลูกค้า](media/dual-write-customer-data-flow.png)

ลูกค้าสามารถแบ่งออกย่างกว้างๆ ได้เป็นสองประเภท: ลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้ ลูกค้าสองประเภทนี้จะถูกจัดเก็บและได้รับจัดการโดยแตกต่างกันใน Finance and Operations และ Common Data Service

ใน Finance and Operations ทั้งลูกค้าเชิงพาณิชย์/เชิงองค์กร และผู้บริโภค/ผู้ใช้ จะมีความเชี่ยวชาญในตารางเดียวที่ชื่อว่า **CustTable** (CustomerCustomerV3Entity) และจะถูกจำแนกประเภทตามแอททริบิวต์ **ชนิด** (ถ้า **ชนิด** ถูกตั้งค่าเป็น **องค์กร** ลูกค้าเป็นลูกค้าเชิงพาณิชย์/เชิงองค์กร และถ้ามีการตั้งค่า **ชนิด** เป็น **บุคคล** ลูกค้าเป็นผู้บริโภค/ผู้ใช้) ข้อมูลผู้ติดต่อหลักจะได้รับการจัดการผ่านเอนทิตี SMMContactPersonEntity

ใน Common Data Service ลูกค้าเชิงพาณิชย์/เชิงองค์กรมีความเชี่ยวชาญในเอนทิตีบัญชี และถูกระบุเป็นลูกค้า เมื่อมีการตั้งค่าแอททริบิวต์ **RelationshipType** เป็น **ลูกค้า** ทั้งผู้บริโภค/ผู้ใช้และผู้ติดต่อจะถูกแสดงโดยเอนทิตีผู้ติดต่อ เพื่อให้การแยกที่ชัดเจนระหว่างผู้บริโภค/ผู้ใช้ และผู้ติดต่อ เอนทิตี **ผู้ติดต่อ** มีแฟล็กบูลีนที่มีชื่อว่า **Sellable** เมื่อ **Sellable** เป็น **จริง** ผู้ติดต่อเป็นผู้บริโภค/ผู้ใช้ และสามารถสร้างใบเสนอราคาและใบสั่งสำหรับผู้ติดต่อนั้นได้ เมื่อ **Sellable** เป็น **เท็จ** ผู้ติดต่อเป็นเพียงผู้ติดต่อหลักของลูกค้า

เมื่อผู้ติดต่อที่ไม่ใช่ Sellable มีส่วนร่วมในกระบวนการใบเสนอราคาหรือใบสั่ง **Sellable** ถูกตั้งค่าเป็น **จริง** เพื่อแฟล็กผู้ติดต่อเป็นผู้ติดต่อ Sellable ผู้ติดต่อที่กลายเป็นผู้ติดต่อที่สามารถขายได้ยังคงเป็นผู้ติดต่อ Sellable

## <a name="templates"></a>เท็มเพลต

ข้อมูลลูกค้ารวมถึงข้อมูลทั้งหมดเกี่ยวกับลูกค้า เช่น กลุ่มลูกค้า ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และสถานะบัตรสมาชิก ชุดของแผนผังเอนทิตีทำงานร่วมกันในระหว่างการโต้ตอบข้อมูลลูกค้า ดังที่แสดงในตารางต่อไปนี้

แอพ Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365         | คำอธิบาย
----------------------------|---------------------------------|------------
ผู้ติดต่อ CDS V2             | ผู้ติดต่อ                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลการติดต่อหลัก ทุติยภูมิ และตติยภูมิสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
กลุ่มลูกค้า             | msdyn_customergroups            | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลกลุ่มลูกค้า
วิธีการชำระเงินของลูกค้า     | msdyn_customerpaymentmethods    | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลวิธีการชำระเงิน
ลูกค้า V3                | บัญชี                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับลูกค้าเชิงพาณิชย์และเชิงองค์กร
ลูกค้า V3                | ผู้ติดต่อ                        | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลหลักของลูกค้าสำหรับผู้บริโภคและผู้ใช้ปลายทาง
บัตรสมาชิก                | msdyn_loyaltycards              | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลบัตรสมาชิก
ส่วนเพิ่มของชื่อ                | msdyn_nameaffixes               | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของส่วนเพิ่มของชื่อสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการแสดงวันที่ในการชำระเงินของ CDS V2    | msdyn_paymentdaylines           | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของบรรทัดวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
CDS จำนวนวันการชำระเงิน            | msdyn_paymentdays               | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของวันชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการกำหนดการชำระเงิน      | msdyn_paymentschedulelines      | ซิงค์ข้อมูลอ้างอิงของบรรทัดกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
กำหนดการชำระเงิน            | msdyn_paymentschedules          | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของกำหนดการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย
เงื่อนไขการชำระเงิน            | msdyn_paymentterms              | เท็มเพลตนี้จะซิงโครไนส์ข้อมูลอ้างอิงของเงื่อนไขการชำระเงินสำหรับทั้งลูกค้าและผู้จัดจำหน่าย

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
