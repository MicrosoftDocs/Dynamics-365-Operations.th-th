---
title: คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Finance
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Finance
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127988"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Finance

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง 

> [!NOTE]
> ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Finance 10.0.12

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>รายงาน SSRS โปแลนด์: ทะเบียน VAT ขาย ทะเบียน VAT ซื้อ ทะเบียน VAT สรุปของสหภาพยุโรป – การอ้างอิงคุณลักษณะ PL-00014

|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | ไม่จำเป็นทางกฎหมาย  |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่ (รูปแบบ Excel สำหรับไฟล์การตรวจสอบมาตรฐานที่มีการรายงานภาษี VAT - JPK_VDEK) |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ใบคำขอเปิด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | เลิกสนับสนุน: ภายในวันที่ 1 กรกฎาคม 2021 เราวางแผนจะไม่สนับสนุนรายงาน SSRS อีกต่อไป: **ทะเบียน VAT ขาย ทะเบียน VAT ซื้อ ทะเบียน VAT สรุปของสหภาพยุโรป – การอ้างอิงคุณลักษณะ PL-00014** ตัวอย่างรูปแบบ Excel สำหรับไฟล์การตรวจสอบมาตรฐานที่มีการรายงานภาษี VAT (JPK_VDEK) จะถูกนำมาใช้แทน |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Finance 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>กล่องโต้ตอบการเปลี่ยนแปลงคำขอของลำดับงานไม่รวมรายการแบบหล่นลงของการเลือกผู้ใช้ไว้อีกต่อไป
|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | เปลี่ยนเป็นคุณลักษณะการเลือกกลุ่มบัญชี  |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่ |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ลำดับงาน |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | เลิกสนับสนุน: โดยวันที่ 1 ธันวาคม 2020 เราวางแผนที่จะไม่สนับสนุนการตั้งค่าชนิดใบสำคัญภาษาจีนโดยไม่มีการเลือกกลุ่มบัญชีอีกต่อไป ค้นหารายละเอียดเพิ่มเติมเกี่ยวกับการออกแบบใหม่ใน [มีอะไรใหม่ใน 10.0.7](whats-new-changed-10-0-7.md) |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน
เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)
