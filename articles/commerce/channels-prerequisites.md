---
title: ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง
description: หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477935"
---
# <a name="channel-setup-prerequisites"></a>ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง

[!include [banner](includes/banner.md)]

หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce

ก่อนที่ช่องทาง Dynamics 365 Commerce จะสามารถสร้างได้ ต้องทำงานที่มีข้อกำหนดเบื้องต้นหลายงานให้เสร็จสมบูรณ์ รายการของงานที่มีข้อกำหนดเบื้องต้นต่อไปนี้มีการจัดระเบียบตามชนิดช่องทาง

> [!NOTE]
> เอกสารบางอย่างยังคงถูกเขียน และลิงค์จะถูกอัพเดตเมื่อเนื้อหาใหม่ถูกเผยแพร่

## <a name="initialization"></a>การเริ่มต้น

- [เตรียมใช้งานข้อมูลเบื้องต้น](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>ข้อกำหนดเบื้องต้นสากลจำเป็นสำหรับชนิดช่องทางทั้งหมด

- [กำหนดและตั้งค่าคอนฟิกโครงสร้างนิติบุคคลของคุณ](channels-legal-entities.md) 
- [ตั้งค่าคอนฟิกลำดับชั้นขององค์กรของคุณ](channels-org-hierarchies.md)
- [ตั้งค่าคลังสินค้า](channels-setup-warehouse.md)
- [ตั้งค่าคอนฟิกภาษีขาย](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล](email-notification-profiles.md)
- [ตั้งค่าลำดับหมายเลข](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [ตั้งค่าลูกค้าและสมุดที่อยู่เริ่มต้น](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นช่องทาง Retail

- [รหัสข้อมูลและกลุ่มรหัสข้อมูล](info-codes-retail.md)
- [ตั้งค่าโปรไฟล์ฟังก์ชันของการขายปลีก](retail-functionality-profile.md)
- [ตั้งค่าสมุดที่อยู่พนักงาน](new-address-book.md)
- [ตั้งค่าโครงร่างหน้าจอ](pos-screen-layouts.md)
- [ตั้งค่าสถานีฮาร์ดแวร์](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นช่องทางศูนย์บริการ

- พารามิเตอร์ศูนย์บริการ
- [วิธีการชำระเงินตามใบสั่งของศูนย์บริการและการเรียกคืนเงิน](work-with-payments.md)
- [โหมดศูนย์บริการของการจัดส่งและค่าธรรมเนียม](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>ข้อกำหนดเบื้องต้นของช่องทางออนไลน์

- [สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์](online-functionality-profile.md)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของช่องทาง](channels-overview.md)

[ภาพรวมขององค์กรและลำดับชั้นขององค์กร](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[การตั้งค่าลำดับชั้นองค์กร](channels-org-hierarchies.md)

[สร้างนิติบุคคล](channels-legal-entities.md)

[ตั้งค่าช่องทางการขายปลีก](channel-setup-retail.md)
    
[ตั้งค่าช่องทางออนไลน์](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
