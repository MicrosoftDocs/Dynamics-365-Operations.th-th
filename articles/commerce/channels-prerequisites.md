---
title: ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง
description: หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002300"
---
# <a name="channel-setup-prerequisites"></a>ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง


[!include [banner](includes/banner.md)]

หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

ก่อนที่ช่องทาง Dynamics 365 Commerce จะสามารถสร้างได้ ต้องทำงานที่มีข้อกำหนดเบื้องต้นหลายงานให้เสร็จสมบูรณ์ รายการของงานที่มีข้อกำหนดเบื้องต้นต่อไปนี้มีการจัดระเบียบตามชนิดช่องทาง

> [!NOTE]
> เอกสารบางอย่างยังคงถูกเขียน และลิงค์จะถูกอัพเดตเมื่อเนื้อหาใหม่ถูกเผยแพร่

## <a name="initialization"></a>การเริ่มต้น

- [เตรียมใช้งานข้อมูลเบื้องต้น](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>ข้อกำหนดเบื้องต้นสากลจำเป็นสำหรับชนิดช่องทางทั้งหมด

- [กำหนดและตั้งค่าคอนฟิกโครงสร้างนิติบุคคลของคุณ](channels-legal-entities.md) 
- [ตั้งค่าคอนฟิกลำดับชั้นขององค์กรของคุณ](channels-org-hierarchies.md)
- [ตั้งค่าคลังสินค้า](channels-setup-warehouse.md)
- [ตั้งค่าคอนฟิกภาษีขาย](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล](email-notification-profiles.md)
- [ตั้งค่าลำดับหมายเลข](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าลูกค้าและสมุดที่อยู่เริ่มต้น](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นช่องทาง Retail

- [รหัสข้อมูลและกลุ่มรหัสข้อมูล](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าโปรไฟล์ฟังก์ชันของการขายปลีก](retail-functionality-profile.md)
- [ตั้งค่าสมุดที่อยู่พนักงาน](new-address-book.md)
- [ตั้งค่าโครงร่างหน้าจอ](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าสถานีฮาร์ดแวร์](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นช่องทางศูนย์บริการ

- พารามิเตอร์ศูนย์บริการ
- วิธีการขอคืนเงินของศูนย์บริการ
- ชนิดการเช่า
- บริการชำระเงิน
- รหัสการระงับใบสั่ง

## <a name="online-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นช่องทางแบบออนไลน์

- [สร้างโปรไฟล์ฟังก์ชันแบบออนไลน์](online-functionality-profile.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของช่องทาง](channels-overview.md)

[ภาพรวมขององค์กรและลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[การตั้งค่าลำดับชั้นองค์กร](channels-org-hierarchies.md)

[สร้างนิติบุคคล](channels-legal-entities.md)

[ตั้งค่าช่องทางการขายปลีก](channel-setup-retail.md)
    
[ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)
