---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management รุ่น 10.0.18 (พฤษภาคม 2021)
description: บทความนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Dynamics 365 Supply Chain Management 10.0.18
author: kamaybac
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 484d791d7386599acca3579ab3a59fd6a17d155e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875465"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10018-may-2021"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management รุ่น 10.0.18 (พฤษภาคม 2021)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management 10.0.18 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.793 และพร้อมใช้งานดังนี้:

- **การนำออกใช้ของการแสดงตัวอย่าง:** มีนาคม 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตด้วยตนเอง):** เมษายน 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** พฤษภาคม 2021

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

คุณลักษณะต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้ ไปตามลิงก์ [แผนนำออกใช้](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) เพื่อดูวันที่นำออกใช้อย่างเป็นทางการสำหรับแต่ละคุณลักษณะการทำงาน

- การนำออกใช้ใบสั่งซื้อโดยอัตโนมัติ (การปรับปรุง [การปฏิบัติการกับคลังสินค้าด้วยหน่วยสเกลในระบบคลาวด์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud))<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ปริมาณงานในการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-warehousing.md)

- [สร้างและดูใบรับรองบนอินเทอร์เฟสการทำงานร่วมกันกับผู้จัดจำหน่าย](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/create-view-certifications-vendor-collaboration-interface)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รักษาใบรับรองของผู้จัดจำหน่าย](../../finance/public-sector/manage-vendor-certification.md)

- [การปรับปรุงประสิทธิภาพสินค้าคงคลังในระดับองค์กรและการเก็บถาวร](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enterprise-scale-inventory-performance-improvements-archiving)<br> - สำหรับข้อมูลเพิ่มเติมเกี่ยว ให้ดูที่ [เก็บถาวรข้อมูลธุรกรรมของสินค้าคงคลัง](../inventory/archive-inventory-transactions.md)

- [การจัดการเงินคืน](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/rebate-management)<br> - สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมโมดูลการจัดการเงินคืน](../rebate-management/rebate-management-overview.md)

- [นโยบายการตั้งค่าการส่งออกเอนทิตี้ข้อมูลการขาย](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-data-entity-export-setup-policy)

- [การลงทะเบียนรายการใบสั่งส่งคืนการขายด้วยความแม่นยำของทศนิยมที่มีและไม่มีน้ำหนักจริง](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight)

- [การยืนยันใบสั่งขายด้วยคลิกเดียว](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation)

- [นโยบายการลบรายการใบสั่งขายสำหรับใบสั่งซื้อ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy)

- อินเทอร์เฟสแบบง่ายเฉพาะเมื่อตอกบัตรเข้าและออกเท่านั้น (การปรับปรุง [อินเทอร์เฟสการดำเนินการผลิตขั้นสูงของการผลิต](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing))<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-configure.md)

คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้

## <a name="new-and-updated-documentation-resources"></a>ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัพเดต

เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัปเดตบทความความช่วยเหลือต่อไปนี้อย่างมาก ไม่จำเป็นต้องมีความเกี่ยวข้องกับลักษณะการทำงานใหม่ที่เพิ่มสำหรับรุ่นนี้ ตามที่แสดงรายการไว้ในส่วนก่อนหน้านี้ แต่อาจช่วยให้คุณสามารถเพิ่มเติมจากลักษณะการทำงานที่มีอยู่ได้

- [Add-in การแสดงผลสินค้าคงคลัง](../inventory/inventory-visibility.md)
- [โมดูลต้นทุนแฝง](../landed-cost/landed-cost-overview.md)
- [อินเทอร์เฟสเครื่องมือจัดการวัสดุ (MHAX)](../warehousing/mhax.md)
- [การวิเคราะห์ความเหมาะสมของการเพิ่มประสิทธิภาพการวางแผน](../master-planning/planning-optimization/planning-optimization-fit-analysis.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>การอัปเดตแพลตฟอร์มสำหรับแอปการเงินและการดำเนินงาน

Microsoft Dynamics 365 Supply Chain Management 10.0.18 รวมถึง Platform update เมื่อต้องการเรียนรู้เพิ่มเติม ดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.18 ของแอปการเงินและการดำเนินงาน (พฤษภาคม 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.18 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=561679&dbType=3&qc=13bb1641c1be430ead8b21ae3d4e0f800d5b81c39b3a56e890db1de7ede59e46)

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ตรวจสอบ [Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1](/dynamics365-release-plan/2021wave1/) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

บทความ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในบทความ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
