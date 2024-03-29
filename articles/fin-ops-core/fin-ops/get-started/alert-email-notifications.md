---
title: การแจ้งเตือนลูกค้าทางอีเมล
description: บทความนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งกฎที่ส่งการแจ้งเตือนอีเมลที่เหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 469c7fdda40780d6e559819103d73d7a4e7132a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878291"
---
# <a name="client-alert-notifications-by-email"></a>การแจ้งเตือนลูกค้าทางอีเมล

[!include [banner](../includes/banner.md)]

คุณสามารถกำหนดกฏการแจ้งเตือนแบบกำหนดเองที่ตรวจสอบมุมมองที่กรองแล้วของข้อมูล และส่งการแจ้งเตือนอีเมลโดยอัตโนมัติ เมื่อเหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น ตัวเลือกในการส่งการแจ้งเตือนทางอีเมลพร้อมใช้งานสำหรับชนิดการแจ้งเตือนที่รองรับทั้งหมด และคุณยังสามารถเปิดสำหรับกฎการแจ้งเตือนที่มีอยู่ได้ด้วย

คุณสามารถใช้การควบคุมภายในเพื่อสร้างกฎการแจ้งเตือนที่ตรวจสอบมุมมองที่กรองแล้วของชุดงานของระบบได้ โดยการตรวจสอบค่าของฟิลด์ **สถานะ** คุณยังสามารถตั้งค่าคอนฟิกกฎการแจ้งเตือนที่ส่งอีเมล เมื่อชุดงานล้มเหลว หลังจากที่คุณสร้างกฎการแจ้งเตือนเหล่านี้ คุณจะไม่ต้องตรวจสอบรายงานสำหรับการเปลี่ยนแปลงไปยังข้อมูลทางธุรกิจอีกต่อไป คุณสามารถใช้บริการการตรวจหาการเปลี่ยนแปลงอัจฉริยาทำการตรวจสอบให้คุณแทน

การแจ้งเตือนไคลเอ็นต์ขึ้นอยู่กับระบบย่อยของอีเมลที่ได้รับผ่านการรวมกับ Microsoft Office เราขอแนะนำให้คุณใช้ผู้ให้บริการ Simple Mail Transfer Protocol (SMTP) เพื่อให้การกระจายอีเมลไม่ต้องขึ้นกับไคลเอ็นต์จดหมายท้องถิ่น

เพื่อส่งการแจ้งเตือนทางอีเมล ลูกค้าต้องตั้งค่าคอนฟิกบริการอีเมลแบบรวม มีการส่งการแจ้งเตือนทางอีเมลไปยังผู้รับในนามของเจ้าของการแจ้งเตือน

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกอีเมลใน ดูที่ [ตั้งค่าคอนฟิกและส่งอีเมล](../organization-administration/configure-email.md)

ภาพต่อไปนี้แสดงกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** ซึ่งรวมตัวเลือก **ส่งอีเมล** ในขณะนี้

[![สร้างกล่องโต้ตอบกฎการแจ้งเตือน ที่ซึ่งตัวเลือกส่งอีเมลถูกตั้งเป็น ใช่](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> เมื่อตัวเลือก **ส่งอีเมล** ถูกตั้งเป็น **ใช่** การแจ้งเตือนจะถูกส่งจากศูนย์การดำเนินการต่อไป

## <a name="alert-notification-email-templates"></a>เท็มเพลตอีเมลการแจ้งเตือน

บริการส่งการแจ้งเตือนอีเมลโดยใช้เท็มเพลตอีเมลที่กำหนดไว้ล่วงหน้า ซึ่งจัดส่งรายละเอียดพื้นฐานของการแจ้งเตือน

ภาพต่อไปนี้แสดงโครงสร้างของการแจ้งเตือน เมื่อได้รับทางอีเมล

[![การแจ้งเตือนตามเท็มเพลตสำหรับการสร้างเรกคอร์ด การเปลี่ยนแปลงฟิลด์ และการลบเท็มเพลต](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]