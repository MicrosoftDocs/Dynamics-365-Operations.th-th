---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.13 (ตุลาคม 2020)
description: บทความนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Dynamics 365 Supply Chain Management 10.0.13
author: kamaybac
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7fd1cf208b9bae86bf25b19f4652890c15a617c9
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2022
ms.locfileid: "9125001"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10013-october-2020"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.13 (ตุลาคม 2020)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management 10.0.13 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.569 และพร้อมใช้งานดังนี้:

- **การนำออกใช้ของการแสดงตัวอย่าง:** สิงหาคม 2020
- **ความพร้อมใช้งานทั่วไป (การอัปเดตด้วยตนเอง):** กันยายน 2020
- **อัปเดทอัตโนมัติ:** ตุลาคม 2020

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

คุณลักษณะต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้ ชื่อเรื่องของคุณลักษณะลิงค์ไปยังข้อมูลเพิ่มเติมบนไซต์ [แผนการนำออกใช้](/dynamics365/release-plans/) ลิงค์เพิ่มเติมชี้ไปที่เอกสารเพิ่มเติมที่พร้อมใช้งานในปัจจุบันสำหรับคุณลักษณะนั้น คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้

- [เปลี่ยนคำศัพท์ของ "การยกเลิกการปิดบัญชีสินค้าคงคลัง" เป็น "การย้อนกลับการปิดบัญชีสินค้าคงคลัง"](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปิดบัญชีสินค้าคงคลัง](../cost-management/inventory-close.md)

- [ยืนยันการจัดส่งขาออกจากชุดงาน](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/confirm-outbound-shipments-batch-jobs)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยืนยันการจัดส่งขาออกจากชุดงาน](../warehousing/confirm-outbound-shipments-from-batch-jobs.md)

- [การมอบหมายรายการงานการจัดซื้อหลายรายการ](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/delegation-multiple-purchasing-work-items)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มอบหมายรายการงานในลำดับงาน](../../fin-ops-core/fin-ops/organization-administration/tasks/delegate-work-items-workflow.md)

- [ป้อนหมายเลขลำดับประจำสินค้าขณะมีการรายงานการเสร็จงานจากอุปกรณ์บัตรงาน](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/enter-serial-numbers-while-reporting-as-finished-job-card-device)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รายงานเมื่อเสร็จสมบูรณ์จากอุปกรณ์บัตรงาน](../production-control/report-finished-job-device.md)

- [มิติสินค้าคงคลังใหม่สำหรับการติดตามรุ่นผลิตภัณฑ์และความสามารถในการเพิ่มฟังก์ชันเพิ่มเติม](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/new-inventory-dimensions-product-version-tracking-enhanced-extensibility)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มิติของผลิตภัณฑ์](../pim/product-dimensions.md)

- [การจองที่กำหนดให้กับใบสั่งตามป้ายทะเบียน](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/order-committed-reservation-based-license-plates-lp-picking-processing)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจองป้ายทะเบียนแบบยืดหยุ่น](../warehousing/flexible-warehouse-level-dimension-reservation.md#flexible-license-plate-reservation)

- [ภาพรวมของรายการเลือกงาน](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/work-pick-line-overview)

- [การปรับปรุงนโยบายงานสำหรับงานขาเข้า](/dynamics365-release-plan/2020wave2/finance-operations/dynamics365-supply-chain-management/work-policy-enhancements-inbound-work)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่  [นโยบายของคลังสินค้า](../warehousing/warehouse-work-policies.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>การอัปเดตแพลตฟอร์มสำหรับแอปการเงินและการดำเนินงาน

Microsoft Dynamics 365 Supply Chain Management 10.0.13 รวมถึง Platform update หากต้องการเรียนรู้เพิ่มเติม โปรดดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.13 ของแอปการเงินและการดำเนินงาน (ตุลาคม 2020)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.13 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=476824&dbType=3&qc=18d329e7d9887a622bada690791f5814dbbef22bb6f4eaada3718299f40132fd) 

### <a name="dynamics-365-2020-release-wave-2-plan"></a>Dynamics 365: 2020 แผนเวฟการนำออกใช้ 2

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ตรวจสอบ [Dynamics 365: 2020 แผนเวฟการนำออกใช้ 2](/dynamics365-release-plan/2020wave2/index) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

บทความ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในบทความ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
