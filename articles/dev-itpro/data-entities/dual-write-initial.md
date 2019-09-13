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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873139"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของ Finance and Operations และ Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

ก่อนที่คุณจะใช้การรวมข้อมูล คุณต้องสร้างข้อมูลเริ่มต้นที่จำเป็นสำหรับลูกค้า ผู้จัดจำหน่าย และผู้ติดต่อ ตัวอย่างเช่น คุณต้องการสร้างสินค้าใน **กลุ่มผู้จัดจำหน่าย** ใหม่ และตั้งค่า **เงื่อนไขของการชำระเงิน** เป็น **Net30** ในกรณีนี้ ก่อนที่คุณจะพยายามสร้างสินค้า **กลุ่มผู้จัดจำหน่าย** คุณต้องตรวจสอบให้แน่ใจว่า **Net30** มีอยู่ในทั้ง Microsoft Dynamics 365 for Finance and Operations และ Common Data Service (ในอนาคต Microsoft จะนำออกใช้ฟังก์ชันแพลตฟอร์มการเขียนแบบคู่ที่เรียกว่า การซิงค์ครั้งแรก ฟังก์ชันนี้จะทำให้การซิงโครไนส์ข้อมูลแบบครั้งเดียวระหว่าง Finance and Operations และ Common Data Service เป็นส่วนหนึ่งของการตั้งค่าการเขียนแบบคู่)

> [!TIP]
> Microsoft กำลังนำออกใช้แผนผังการเขียนแบบคู่สำหรับข้อมูลอ้างอิงทั้งหมด ซึ่งรวมถึง **เงื่อนไขของการชำระเงิน** (เงื่อนไขการชำระเงิน) ถ้าคุณมีข้อมูลเริ่มต้นในระบบหนึ่งแล้ว การดำเนินการปรับปรุงขนาดเล็กบนเรกคอร์ดสามารถทริกเกอร์การเขียนแบบคู่บนเรกคอร์ดนั้นได้

คุณต้องทำตามลำดับของความสำคัญต่อไปนี้ และตรวจสอบให้แน่ใจว่าข้อมูลเริ่มต้นพร้อมใช้งานในทั้ง Finance and Operations และ Common Data Service

## <a name="vendor"></a>ผู้จัดจำหน่าย

นี่คือลำดับของการดำเนินการสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** :

1. กลุ่มผู้จัดจำหน่าย

    1. เงื่อนไขการชำระเงิน

        1. วันที่ชำระเงินและรายการ
        2. กำหนดการชำระเงิน

2. วิธีการชำระเงินของผู้จัดจำหน่าย

## <a name="customer-organization"></a>ลูกค้า (องค์กร)

นี่คือลำดับของการดำเนินการสำหรับเอนทิตี **ลูกค้า** :

1. กลุ่มลูกค้า

    1. เงื่อนไขการชำระเงิน

        1. วันที่ชำระเงินและรายการ
        2. การชำระเงิน 

2. วิธีการชำระเงินของลูกค้า

## <a name="contact-person"></a>ผู้ติดต่อ (บุคคล)

นี่คือลำดับของการดำเนินการสำหรับเอนทิตี **ผู้ติดต่อ** :

1. ลูกค้า
2. ผู้จัดจำหน่าย
