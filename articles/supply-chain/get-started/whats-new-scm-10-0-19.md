---
title: การแสดงตัวอย่าง Dynamics 365 Supply Chain Management 10.0.19 (กรกฎาคม 2021)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Supply Chain Management 10.0.19
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961692"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>การแสดงตัวอย่าง Dynamics 365 Supply Chain Management 10.0.19 (กรกฎาคม 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

หัวข้อนี้แสดงรายการคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ในพรีวิว Microsoft Dynamics 365 Supply Chain Management ของรุ่น 10.0.19 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.837 และพร้อมใช้งานดังนี้:

- **การนำออกใช้ของการแสดงตัวอย่าง:** เมษายน 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตด้วยตนเอง):** มิถุนายน 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** กรกฎาคม 2021

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้มีคุณลักษณะที่รวมอยู่ในการนำออกใช้นี้ คอลัมน์ *คุณลักษณะ* จะแสดงลิงค์ไปยัง [แผนการนำออกใช้](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) ซึ่งคุณสามารถดูวันที่นำออกใช้ที่เป็นทางการของแต่ละคุณลักษณะได้ คอลัมน์ *ข้อมูลเพิ่มเติม* จะแสดงลิงค์ไปที่เอกสารที่เกี่ยวข้อง

คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้ คุณลักษณะที่แสดงรายการบางอย่างยังคงอยู่ในพรีวิว ในขณะที่บางรายการอาจพร้อมใช้งานโดยทั่วไปอยู่แล้ว

| พื้นที่คุณลักษณะ | ลักษณะการทำงาน | ข้อมูลเพิ่มเติม |
|---|---|---|
| สินค้าคงคลังและลอจิสติกส์ | [การเพิ่มประสิทธิภาพการส่งออกเอนทิตี้ข้อมูลบุคคลที่ติดต่อ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *ไม่พร้อมใช้งาน* |
| สินค้าคงคลังและลอจิสติกส์ | [การปรับปรุงส่วนเพิ่มสำหรับความสามารถในการดำเนินงานคลังสินค้าที่มีสเกลยูนิต](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[ข้อความตัวประมวลผลข้อความ](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[การปรับปรุงสินค้าคงคลังของคลังสินค้า](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[ปริมาณงานการจัดการคลังสินค้าสำหรับสเกลยูนิตในระบบคลาวด์และ Edge](../cloud-edge/cloud-edge-workload-warehousing.md) |
| สินค้าคงคลังและลอจิสติกส์ | [ฟังก์ชันการค้นหาเกี่ยวกับฟิลด์บทนําของเอกสารและบทสรุปของเอกสารในหน้าใบเสนอราคาขาย](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *ไม่พร้อมใช้งาน* |
| สินค้าคงคลังและลอจิสติกส์ | [การดำเนินการของคลังสินค้าที่มีหน่วยสเกล edge บนฮาร์ดแวร์ที่ออกแบบเองของคุณ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [ปรับใช้หน่วยสเกล edge บนฮาร์ดแวร์แบบกำหนดเองโดยใช้ LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| การผลิต | [การดำเนินการของการผลิตที่มีหน่วยสเกล edge บนฮาร์ดแวร์ที่ออกแบบเองของคุณ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [ปรับใช้หน่วยสเกล edge บนฮาร์ดแวร์แบบกำหนดเองโดยใช้ LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| การวางแผน | การยืนยันแผนการใบสั่งตามการสอบถาม | [ยืนยันแผนการใบสั่ง](../master-planning/planning-optimization/planned-order-firming.md) |
| การจัดการข้อมูลผลิตภัณฑ์ | [การปรับปรุงหน้าคำแนะนำตัวแปร](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัพเดต

เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัพเดตส่วนความช่วยเหลือต่อไปนี้อย่างมาก ไม่จำเป็นต้องมีความเกี่ยวข้องกับลักษณะการทำงานใหม่ที่เพิ่มสำหรับรุ่นนี้ ตามที่แสดงรายการไว้ในส่วนก่อนหน้านี้ แต่อาจช่วยให้คุณสามารถเพิ่มเติมจากลักษณะการทำงานที่มีอยู่ได้

| พื้นที่คุณลักษณะ | หัวข้อใหม่หรือที่อัปเดต |
|---|---|
| การจัดการการเปลี่ยนแปลงทางวิศวกรรม | [คำถามที่ถามบ่อยเกี่ยวกับการจัดการการเปลี่ยนแปลงทางวิศวกรรม](../engineering-change-management/change-management-faq.md) |
| การจัดซื้อและการจัดหา | [คำขอประเภทจากผู้จัดจำหน่าย](../procurement/category-requests-from-vendors.md) |
| การจัดการข้อมูลผลิตภัณฑ์ | [จัดการหน่วยวัด](../pim/tasks/manage-unit-measure.md)<br><br>[การคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์](../pim/config-model-calculations.md) |
| การควบคุมการผลิต | [ลำดับหมายเลขแบบรวมสำหรับรหัสงาน](../production-control/unified-job-ids.md) |
| การจัดการการขนส่ง | [คลาส LTL](../transportation/ltl-class.md)<br><br>[รหัส NMFC](../transportation/nmfc-codes.md) |
| การจัดการคลังสินค้า | [แก้ไขปัญหาเกี่ยวกับชุดงานคลังสินค้าและลำดับชั้นการจองแบบตามลำดับ](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| การจัดการคลังสินค้า การสร้างเวฟ และการประมวลผล | [การสร้างและการประมวลผลเวฟ](../warehousing/wave-processing.md)<br><br>[พารามิเตอร์คลังสินค้าสำหรับการประมวลผลเวฟ](../warehousing/wave-warehouse-parameters.md)<br><br>[เท็มเพลตเวฟ](../warehousing/wave-templates.md)<br><br>[การปันส่วนเวฟ](../warehousing/wave-allocation-method.md)<br><br>[จัดกำหนดการสร้างงานระหว่างเวฟ](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[การบรรจุลงตู้บรรจุสินค้า](../warehousing/wave-containerization.md)<br><br>[การแจ้งเตือนการดำเนินการเวฟ](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platform update สำหรับแอป Finance and Operations

Microsoft Dynamics 365 Supply Chain Management 10.0.19 รวมถึง Platform update เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [Platform update สำหรับรุ่น10.0.19 ของแอป Finance and Operations (กรกฎาคม 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.19 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415)

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ตรวจสอบ [Dynamics 365: 2021 แผนเวฟการนำออกใช้ 1](/dynamics365-release-plan/2021wave1/) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

หัวข้อ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในหัวข้อ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
