---
title: ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม
description: หัวข้อนี้อธิบายการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอพลิเคชัน Finance and Operations และ Common Data Service
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
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771007"
---
# <a name="integrated-vendor-master"></a>ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม

[!include [banner](../includes/banner.md)]

คำว่า *ผู้จัดจำหน่าย* หมายถึงองค์กรของซัพพลายเออร์หรือเจ้าของแต่ละรายที่เป็นส่วนหนึ่งของกระบวนการห่วงโซ่อุปทาน และที่จัดหาสินค้าสำหรับธุรกิจ แม้ว่า *ผู้จัดจำหน่าย* เป็นแนวคิดที่สร้างขึ้นในแอพลิเคชัน Finance and Operations แนวคิดของผู้จัดจำหน่ายไม่มีอยู่ในแอพลิเคชัน Dynamics 365 อื่น ๆ แต่บางธุรกิจจะโอเวอร์โหลดเอนทิตีบัญชีเพื่อจัดเก็บทั้งข้อมูลลูกค้าและข้อมูลผู้จัดจำหน่าย ธุรกิจอื่นๆ ใช้แนวคิดของผู้จัดจำหน่ายที่กำหนดเอง การรวม Common Data Service สนับสนุนการออกแบบเหล่านี้ทั้งสองรายการ ดังนั้น คุณจึงสามารถเปิดใช้งานการออกแบบแบบใดแบบหนึ่ง โดยขึ้นอยู่กับสถานการณ์จำลองทางธุรกิจของคุณ

การรวมของข้อมูลผู้จัดจำหน่ายระหว่างแอป Finance and Operations และแอป Dynamics 365 อื่น ให้คุณพัฒนาความเชี่ยวชาญของหลายข้อมูลได้ โดยไม่คำนึงถึงจุดกำเนิดของข้อมูลของผู้จัดจำหน่าย จะมีการรวมอยู่เบื้องหลังในขอบเขตของแอพลิเคชันและความแตกต่างของโครงสร้างพื้นฐาน 

### <a name="vendor-data-flow"></a>โฟลว์ข้อมูลของผู้จัดจำหน่าย

ถ้าคุณต้องการใช้แอพลิเคชัน Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการแยกข้อมูลผู้จัดจำหน่ายออกจากข้อมูลลูกค้า คุณสามารถใช้การออกแบบผู้จัดจำหน่ายใหม่ได้

![โฟลว์ข้อมูลของผู้จัดจำหน่าย](media/dual-write-vendor-data-flow.png)

ถ้าคุณต้องการใช้แอพลิเคชัน Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการใช้เอนทิตีบัญชีต่อเพื่อจัดเก็บข้อมูลผู้จัดจำหน่าย คุณสามารถใช้การออกแบบผู้จัดจำหน่ายแบบขยายใหม่ได้ ในการออกแบบนี้ ข้อมูลผู้จัดจำหน่ายแบบขยาย เช่น กลุ่มผู้จัดจำหน่าย และโพรไฟล์การลงบัญชีผู้จัดจำหน่าย จะถูกเก็บไว้ในรายละเอียดผู้จัดจำหน่าย

![โฟลว์ข้อมูลของผู้จัดจำหน่ายแบบขยาย](media/dual-write-vendor-detail.jpg)

ข้อมูลการติดต่อของผู้จัดจำหน่ายคล้ายกับข้อมูลการติดต่อของลูกค้า ในเบื้องหลัง ข้อมูลของผู้ติดต่อที่เก็บไว้และถูกดึงจากเอนทิตีเีดียวกัน

## <a name="templates"></a>เท็มเพลต

ข้อมูลผู้จัดจำหน่ายรวมถึงข้อมูลทั้งหมดเกี่ยวกับผู้จัดจำหน่าย เช่น กลุ่มผู้จัดจำหน่าย ที่อยู่ ข้อมูลผู้ติดต่อ โพรไฟล์การชำระเงิน และโพรไฟล์ใบแจ้งหนี้ คอเลคชันของแม็บเอนทิตีทำงานร่วมกันในขณะการรวมข้อมูลผู้จัดจำหน่าย ดังที่แสดงในตารางต่อไปนี้

แอพ Finance and Operations | แอปพลิเคชันอื่น ๆ ของ Dynamics 365         | คำอธิบาย
----------------------------|---------------------------------|------------
ผู้จัดจำหน่าย V2               | บัญชี | ธุรกิจที่ใช้เอนทิตีบัญชีเพื่อจัดเก็บข้อมูลผู้จัดจำหน่ายสามารถใช้ต่อไปได้ในลักษณะเดียวกัน นอกจากนี้ ยังสามารถใช้ประโยชน์จากฟังก์ชันของผู้จัดจำหน่ายที่ชัดเจนซึ่งกำลังจะมา เนื่องจากการรวมของแอพลิเคชัน Finance and Operations
ผู้จัดจำหน่าย V2               | Msdyn\_vendors | ธุรกิจที่ใช้โซลูชันแบบกำหนดเองสำหรับผู้จัดจำหน่ายสามารถใช้ประโยชน์จากแนวคิดผู้จัดจำหน่ายแบบสำเร็จรูปที่ถูกนำมาใช้ใน Common Data Service เนื่องจากการรวมของแอพลิเคชัน Finance and Operations 
กลุ่มผู้จัดจำหน่าย | msdyn_vendorgroups | เท็มเพลตนี้รวมข้อมูลกลุ่มผู้จัดจำหน่ายเข้าด้วยกัน
วิธีการชำระเงินของผู้จัดจำหน่าย | msdyn_vendorpaymentmethods | เท็มเพลตนี้รวมข้อมูลวิธีการชำระเงินของผู้จัดจำหน่วยเข้าด้วยกัน
ผู้ติดต่อ CDS V2             | ผู้ติดต่อ                        | เท็มเพลต [contacts](dual-write-customer.md#cds-contacts-v2-to-contacts) รวมข้อมูลผู้ติดต่อ ปฐมภูม ทุติยภูมิ ตติยภูมิ ทั้งหมดเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
รายการกำหนดการชำระเงิน      | msdyn_paymentschedulelines      | เท็มเพลต [payment schedule lines](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) รวมข้อมูลอ้างอิงสำหรับลูกค้าและผู้จัดจำหน่ายเข้าด้วยกัน
กำหนดการชำระเงิน            | msdyn_paymentschedules          | เท็มเพลต [payment schedules](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) รวมข้อมูลอ้างอิงกำหนดการชำระิิเงินเข้าด้วยกัน ทั้งสำหรับลูกค้าและผู้จัดจำหน่าย
รายการแสดงวันที่ในการชำระเงินของ CDS V2    | msdyn_paymentdaylines           | เท็มเพลต [payment day lines](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) รวมข้อมูลอ้างอิงกำหนดการชำระเงินเข้าด้วยกัน สำหรับลูกค้าและผู้จัดจำหน่าย
CDS จำนวนวันการชำระเงิน            | msdyn_paymentdays               | เท็มเพลต [payment days](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) รวมข้่อมูลอ้างอิงวันชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
เงื่อนไขการชำระเงิน            | msdyn_paymentterms              | เท็มเพลต [terms of payment](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) รวมข้อมูลอ้างอิงเงื่อนไขการชำระเงินเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย
ส่วนเพิ่มของชื่อ                | msdyn_nameaffixes               | เท็มเพลต [name affixes](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) รวมข้อมูลอ้างอิงส่วนเพิ่มของชื่อเข้าด้วยกัน สำหรับทั้งลูกค้าและผู้จัดจำหน่าย

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
