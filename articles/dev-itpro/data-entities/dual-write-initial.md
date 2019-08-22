---
title: ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของ Finance and Operations และ Common Data Service
description: หัวข้อนี้ระบุลำดับของการซิงโครไนส์ที่คุณต้องปฏิบัติตามเพื่อสร้างข้อมูลเริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797309"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของ Finance and Operations และ Common Data Service

ก่อนที่คุณจะใช้การรวมข้อมูล คุณต้องสร้างข้อมูลเริ่มต้นที่จำเป็นสำหรับลูกค้า ผู้จัดจำหน่าย และผู้ติดต่อ ตัวอย่างเช่น ถ้าคุณต้องการสร้างรายการของ **กลุ่มผู้จัดจำหน่าย** ใหม่ และตั้งค่า **เงื่อนไขของการชำระเงิน** เป็น **Net30** จากนั้น ก่อนที่คุณจะพยายามสร้างรายการ **กลุ่มผู้จัดจำหน่าย** คุณต้องตรวจสอบให้แน่ใจว่า **Net30** พร้อมใช้งานในทั้ง Finance and Operations และ Common Data Service (ในอนาคต เราจะนำออกใช้ฟังก์ชันแพลตฟอร์มการเขียนแบบคู่ที่เรียกว่า **การซิงค์ครั้งแรก** จะทำให้การซิงโครไนส์ข้อมูลแบบครั้งเดียวระหว่าง Finance and Operations และ Common Data Service เป็นส่วนหนึ่งของการตั้งค่าการเขียนแบบคู่)

เคล็ดลับ: เรากำลังนำออกใช้แผนผังการเขียนแบบคู่สำหรับข้อมูลอ้างอิงทั้งหมด ซึ่งรวมถึง **เงื่อนไขของการชำระเงิน** (เงื่อนไขการชำระเงิน) ถ้าคุณมีข้อมูลเริ่มต้นในระบบหนึ่งแล้ว การดำเนินการปรับปรุงขนาดเล็กบนเรกคอร์ดสามารถทริกเกอร์การเขียนแบบคู่บนเรกคอร์ดนั้นได้ 

คุณต้องทำตามลำดับความสำคัญต่อไปนี้และตรวจสอบให้แน่ใจว่าข้อมูลเริ่มต้นพร้อมใช้งานในทั้ง Finance and Operations และ Common Data Service   

## <a name="vendor"></a>ผู้จัดจำหน่าย

ลำดับของการดำเนินการสำหรับผู้จัดจำหน่ายคือ:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>ลูกค้า (องค์กร)

ลำดับของการดำเนินการสำหรับลูกค้าคือ:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>ผู้ติดต่อ (บุคคล)

ลำดับของการดำเนินการสำหรับผู้ติดต่อคือ:

```
Customer
Vendor               
```
