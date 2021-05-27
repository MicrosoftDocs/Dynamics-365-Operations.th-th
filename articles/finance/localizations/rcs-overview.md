---
title: Regulatory Configuration Service
description: หัวข้อนี้แสดงภาพรวมของความสามารถของ Regulatory Configuration Service (RCS) และอธิบายวิธีการเข้าถึงบริการ
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019405"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) เป็นโปรแกรมออกแบบแบบสแตนด์อโลนและบริการจัดการวงจรชีวิตสำหรับฟังก์ชันแบบสากลไม่มีรหัส/รหัสต่ำ ผู้มีส่วนได้ส่วนเสียแบบสากลของ RCS ขยายและปรับเปลี่ยนพื้นที่หลักของภาษี การออกใบแจ้งหนี้อิเล็กทรอนิกส์ การรายงานตามระเบียบบังคับ การธนาคาร และเอกสารทางธุรกิจโดยไม่เกี่ยวข้องกับนักพัฒนา แนวทางแบบสากลไม่มีรหัส/รหัสต่านี้ช่วยให้เป็นสากลง่ายขึ้น เร็วกว่า และต้นทุนที่มีประสิทธิภาพมากกว่าในการสร้างหรือขยาย

RCS ให้ความสามารถต่อไปนี้:

- การสนับสนุนฟังก์ชันทั้งหมดที่ได้รับจากการรายงานทางอิเล็กทรอนิกส์ (ER)
- เงื่อนไขเบื้องต้นในการตั้งค่าคอนฟิกไมโครเซอร์วิสแบบสากลใหม่
- สนับสนุนสำหรับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)
- สนับสนุนการคํานวณภาษี สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [บริการภาษี](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)
- การสนับสนุนฟังก์ชันคุณลักษณะสากลใหม่ซึ่งช่วยให้การจัดการรอบเวลาของลักษณะการการใช้ฟังก์ชันหลายส่วนประกอบง่ายขึ้น และช่วยให้สามารถตั้งค่าคอนฟิกการการและตั้งค่าพารามิเตอร์ลักษณะการใช้งานต่าง ๆ ง่ายขึ้น หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [Regulatory Configuration Service – การจัดการคุณลักษณะสากลแบบง่ายสำหรับบริการสากล](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)
- สนับสนุนการเผยแพร่ การจัดเก็บ และการแบ่งปันการตั้งค่าคอนฟิกที่กําหนดเองจากส่วนกลางในที่เก็บส่วนกลางเพื่อให้การจัดการการตั้งค่าคอนฟิกง่ายขึ้นโดยไม่ต้องใช้ Microsoft Dynamics Lifecycle Services (LCS)

## <a name="access-rcs"></a>การเข้าถึง RCS

คุณสามารถลงชื่อสมัครหรือเข้าสู่ระบบ RCS จาก [หน้า Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)

![ลงชื่อสมัครใช้และลงชื่อเข้าใช้ RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

บนหน้า **Regulatory Configuration Service** ให้ตรวจทานและยอมรับข้อกําหนดและเงื่อนไขเพิ่มเติมเพื่อใช้บริการ แล้วเลือกปุ่มใดปุ่มหนึ่งต่อไปนี้

- **ลงชื่อสมัคร** หากคุณเป็นผู้ใช้ครั้งแรกของบริการ และคุณใช้ที่อยู่อีเมลธุรกิจเพื่อเตรียมใช้งานสภาพแวดล้อมบริการขององค์กร
- **เข้าสู่ระบบ** ถ้าคุณเคยลงชื่อสมัครใช้บริการแล้วก่อนหน้านี้ และคุณต้องการเข้าถึงสภาพแวดล้อมขององค์กร

## <a name="regional-availability"></a>ความพร้อมของภูมิภาค

โดยทั่วไป RCS จะพร้อมใช้งานในภูมิภาคต่อไปนี้:

- สหรัฐ
- อินเดีย
- ฝรั่งเศส
- ยุโรป

ดูรายการภูมิภาคทั้งหมด โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/dynamics_365_international_availability_deck)

## <a name="related-rcs-documentation"></a>คู่มือ RCS ที่เกี่ยวข้อง

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับส่วนประกอบที่เกี่ยวข้อง ให้ดูที่คู่มือต่อไปนี้:

- **ที่เก็บส่วนกลาง:**

    - [สร้างการตั้งค่าคอนฟิก ER & อัปโหลดไปที่ที่เก็บส่วนกลาง](rcs-global-repo-upload.md)
    - [แบ่งปันการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง](rcs-global-repo-share-configuration.md)
    - [การกรองข้อมูลขั้นสูงในที่เก็บส่วนกลาง](enhanced-filtering-global-repo.md)
    - [ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลาง](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [ยกเลิกการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง](discontinuing-configurations-rcs-global-repo.md)

- **คุณลักษณะที่ใช้ทั่วโลก**

    - [Regulatory configuration service (RCS) - คุณลักษณะที่ใช้ทั่วโลก](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)