---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.24 (กุมภาพันธ์ 2022)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management 10.0.24
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9b4b538e6d50013626739e19fee2a050b630bf7f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334819"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.24 (กุมภาพันธ์ 2022)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.24 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.1084 และพร้อมใช้งานดังนี้:

- **ตัวอย่างการนำออกใช้:** ธันวาคม 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตเอง):** มกราคม 2022
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** กุมภาพันธ์ 2022

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้แสดงรายการคุณลักษณะที่ถูกรวมอยู่ในการนำออกใช้นี้ เราอาจอัปเดตบทความนี้เพื่อรวมคุณลักษณะที่ทำให้เกิดการสร้าง หลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก

| พื้นที่คุณลักษณะ | คุณลักษณะ | ข้อมูลเพิ่มเติม | เปิดใช้งานโดย |
|---|---|---|---|
| โทโพโลยีแบบไฮบริดแบบกระจาย | [ปริมาณงานการดำเนินการคลังสินค้าที่ปรับปรุงบนสเกลยูนิต](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [ปริมาณงานการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-warehousing.md) | เปิดใช้งานตามค่าเริ่มต้น |
| โทโพโลยีแบบไฮบริดแบบกระจาย | [เริ่มต้นใบสั่งผลิตในปริมาณงานในการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [ปริมาณงานการดำเนินการผลิตสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง](../cloud-edge/cloud-edge-workload-manufacturing.md) | การจัดการคุณลักษณะ (*เริ่มต้นใบสั่งผลิตในปริมาณงานในการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง*)  |
| การวางแผน | [การสนับสนุนการเพิ่มประสิทธิภาพการวางแผนของกําไรขั้นต้นของการสั่งซื้อใหม่และการตัดสินค้าจากคลัง](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [ค่าเผื่อความปลอดภัย](../master-planning/planning-optimization/safety-margins.md) | เปิดใช้งานตามค่าเริ่มต้น |

## <a name="feature-enhancements-included-in-this-release"></a>การปรับปรุงคุณลักษณะรวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้แสดงรายการการปรับปรุงคุณลักษณะที่ถูกรวมอยู่ในการนำออกใช้นี้ การปรับปรุงเหล่านี้แต่ละรายการให้การปรับปรุงส่วนเพิ่มให้กับคุณลักษณะที่มีอยู่ เนื่องจากเป็นการปรับปรุงเท่านั้น จึงไม่ถูกแสดงรายการใน [แผนการนำออกใช้](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) อย่างไรก็ตาม เพื่อให้แน่ใจว่าการปรับปรุงเหล่านี้จะไม่ขัดแย้งกับการเลือกเองหรือคุณลักษณะที่มีอยู่ของคุณ แต่ละรายการจะถูกปิดตามค่าเริ่มต้น (เว้นแต่จะไม่ได้ระบุไว้เป็นอย่างอื่น)

หากคุณต้องการเปิดหรือปิดคุณลักษณะใดๆ เหล่านี้ คุณต้องทำใน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

| โมดูล | ชื่อคุณลักษณะในการจัดการคุณลักษณะ | ข้อมูลเพิ่มเติม |
|---|---|---|
| การควบคุมการผลิต | การตรวจสอบความพร้อมใช้งานของวัสดุตามความต้องการสำหรับใบสั่งผลิต | คุณลักษณะนี้ช่วยให้การเปิดหน้า **ใบสั่งผลิตที่จะนำออกใช้** ซึ่งมีอยู่ในพื้นที่ทำงาน **การจัดการระบบการผลิต** หากไม่มีคุณลักษณะนี้ ระบบจะตรวจสอบโดยอัตโนมัติว่าวัสดุพร้อมใช้สำหรับใบสั่งผลิตที่แสดงไว้ทั้งหมดหรือไม่ในทันทีที่คุณเปิดหน้านี้ ซึ่งอาจใช้เวลามากถ้าคุณมีใบสั่งจํานวนมาก เมื่อคุณลักษณะนี้เปิดใช้งาน ระบบจะแสดงปุ่มแถบเครื่องมือแทน ซึ่งคุณสามารถใช้เริ่มต้นการตรวจสอบวัสดุได้เฉพาะกับใบสั่งที่เลือกและเมื่อจำเป็นเท่านั้น |
| การควบคุมการผลิต | ลงทะเบียนปริมาณการใช้วัสดุบนส่วนติดต่อการดำเนินการของระบบการผลิต (non-WMS) | คุณลักษณะนี้ช่วยให้ผู้ปฏิบัติงานสามารถใช้อินเทอร์เฟสการดำเนินการของระบบการผลิตเพื่อลงทะเบียนปริมาณการใช้วัสดุ หมายเลขชุดงาน และหมายเลขลำดับประจำสินค้า คุณลักษณะนี้รองรับเฉพาะสินค้าที่ไม่ได้เปิดใช้งานการใช้กระบวนการ Warehouse Management (WMS) การสนับสนุนสินค้าที่เปิดใช้งาน WMS มีการจัดกำหนดการสำหรับรุ่นในอนาคต<p>ผู้ผลิตบางราย โดยเฉพาะผู้ผลิตที่อยู่ในอุตสาหกรรมการแปรรูปต้องลงทะเบียนจํานวนของวัสดุที่ใช้ไปในแต่ละชุดงานหรือใบสั่งผลิตอย่างชัดแจ้ง ตัวอย่างเช่น ผู้ปฏิบัติงานอาจใช้เครื่องชั่งเพื่อชั่งปริมาณวัสดุที่ใช้ไปเมื่อทำงาน องค์กรเหล่านี้ยังต้องลงทะเบียนว่าใช้หมายเลขชุดงานใดเมื่อผลิตผลิตภัณฑ์แต่ละรายการ เพื่อให้แน่ใจว่าสืบย้อนวัสดุทั้งหมดได้ |
| การควบคุมการผลิต | รายงานเมื่อเสร็จสิ้นสำหรับปริมาณงานในการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และแบบปลายทาง | คุณลักษณะนี้ให้ผู้ปฏิบัติงานสามารถใช้แอป Warehouse Management บนมือถือเพื่อรายงานใบสั่งผลิตหรือชุดงานเมื่อเสร็จสิ้นเมื่อมีการเรียกใช้แอปกับปริมาณงานการจัดการคลังสินค้าบนสเกลยูนิตในระบบคลาวด์และแบบปลายทาง ดูข้อมูลเพิ่มเติมที่ [รายงานเมื่อเสร็จสิ้นและการสำรองสินค้าในสเกลยูนิต](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF) |
| การจัดการคลังสินค้า | หน้าเวิร์กเบนช์การวางแผนการบรรทุกใหม่ | เพิ่มหน้าเวิร์กเบนช์การวางแผนการบรรทุกใหม่สองหน้า: **เวิร์กเบนช์การวางแผนการบรรทุกขาเข้า** และ **เวิร์กเบนช์การวางแผนการบรรทุกขาออก** |

## <a name="new-and-updated-documentation-resources"></a>ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัปเดต

เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัปเดตบทความความช่วยเหลือต่อไปนี้อย่างมาก บทความเหล่านี้อาจไม่เกี่ยวข้องกับคุณลักษณะใหม่ที่ถูกเพิ่มให้กับการนำออกใช้นี้ ตามที่แสดงรายการในส่วนก่อนหน้านี้ อย่างไรก็ตาม รายการเหล่านั้นอาจช่วยให้คุณใช้ประโยชน์ได้มากขึ้นจากคุณลักษณะที่มีอยู่

| พื้นที่คุณลักษณะ | บทความใหม่หรือที่อัปเดต |
|---|---|
| การจัดการต้นทุน | [รายงานมูลค่าสินค้าคงคลัง](../cost-management/inventory-value-report-storage.md) |
| การจัดการต้นทุน | [ตัวอย่างและตรรกะของรายงานมูลค่าของสินค้าคงคลัง](../cost-management/inventory-value-report-examples.md) |
| การวางแผนหลัก | [พารามิเตอร์วันที่และเวลาที่ใช้โดยการเพิ่มประสิทธิภาพการวางแผน](../master-planning/planning-optimization/date-time-used.md) |
| การวางแผนหลัก | [การตั้งค่าการคาดการณ์ความต้องการ](../master-planning/demand-forecasting-setup.md) |
| การวางแผนหลัก | [ใช้สมุดรายวันปริมาณสินค้าคงคลังที่ปลอดภัยเพื่ออัปเดตความครอบคลุมขั้นต่ำสำหรับสินค้า](../master-planning/safety-stock-journal.md) |
| การควบคุมการผลิต | [กำหนดอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-customize.md) |
| การควบคุมการผลิต | [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-styles.md) |
| การขายและการตลาด | [จัดกำหนดการล้างข้อมูลประวัติการขาย](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| การจัดการคลังสินค้า | [บัญชีผู้ใช้ของอุปกรณ์เคลื่อนที่](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>การอัปเดตแพลตฟอร์มสำหรับแอปการเงินและการดำเนินงาน

Microsoft Dynamics 365 Supply Chain Management 10.0.24 รวมถึงการอัปเดตแพลตฟอร์ม หากต้องการเรียนรู้เพิ่มเติม โปรดดูที่ [การอัปเดตแพลทฟอร์มสำหรับรุ่น 10.0.24 ของแอปการเงินและการดำเนินงาน (กุมภาพันธ์ 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.24 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f)

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 และระบบคลาวด์อุตสาหกรรม: 2021 แผนเวฟการนำออกใช้ 2

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ดู [Dynamics 365 และระบบคลาวด์อุตสาหกรรม: 2021 แผนเวฟการนำออกใช้ 2](/dynamics365-release-plan/2021wave2/) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

บทความ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในบทความ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

