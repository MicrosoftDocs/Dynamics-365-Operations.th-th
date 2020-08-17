---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.9 (เมษายน 2020)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Supply Chain Management 10.0.9
author: kamaybac
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a127fcf2bf429299dc73e338cbfc3fbf8f5f2d9f
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651992"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1009-april-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Supply Chain Management 10.0.9 (เมษายน 2020)

[!include [banner](../includes/banner.md)]

หัวข้อนี้แสดงรายการคุณลักษณะที่ใหม่ หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Microsoft Dynamics 365 Supply Chain Management รุ่นการแสดงตัวอย่าง 10.0.9 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.383 และพร้อมใช้งานดังนี้:

- **แสดงตัวอย่างการนำออกใช้:** กุมภาพันธ์ 2020
- **ความพร้อมใช้งานทั่วไป (การอัพเดตด้วยตนเอง):** มีนาคม 2020
- **อัพเดตอัตโนมัติ:** เมษายน 2020

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

คุณลักษณะต่อไปนี้จะรวมอยู่ในการนำออกใช้นี้ ชื่อเรื่องของคุณลักษณะลิงค์ไปยังข้อมูลเพิ่มเติมบนไซต์ [แผนการนำออกใช้](https://docs.microsoft.com/dynamics365/release-plans/) ลิงค์เพิ่มเติมชี้ไปที่เอกสารหรือวิดีโอเพิ่มเติมที่พร้อมใช้งานในปัจจุบันสำหรับคุณลักษณะนั้น นอกจากนี้ คุณลักษณะเหล่านี้บางอย่างยังอาจถูกรวมไว้ในการนำออกใช้ส่วนเพิ่มก่อนหน้านี้ แต่ยังไม่ได้ประกาศในหัวข้อ *มีอะไรใหม่* ก่อนหน้านี้ ดังนั้นเราจึงเพิ่มไว้ที่นี่ คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้

- [การสร้างโหลดขั้นสูงในระหว่างเวฟ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/advanced-load-building-during-wave)
- [การจัดส่งที่นำออกใช้อัตโนมัติสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/auto-release-shipment-cross-dock)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การจัดส่งที่นำออกใช้อัตโนมัติสำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า](../warehousing/auto-release-shipment-for-cross-docking.md)
- [คำนวณวันที่จัดส่ง PO ตามระยะเวลารอคอยสินค้าและจำนวนวันทำงาน (ภาครัฐ)](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/calculate-po-delivery-date-based-lead-times-working-days-public-sector)
- [การดำเนินการกับผลิตภัณฑ์ตามน้ำหนักจริงด้วยการจัดการคลังสินค้า](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/catch-weight-product-processing-warehouse-management)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การประมวลผลผลิตภัณฑ์ของน้ำหนักที่เลือกได้ที่มีการจัดการคลังสินค้า](../warehousing/catch-weight-processing.md) และวิดีโอ [การปรับปรุงผลิตภัณฑ์ตามน้ำหนักจริง](https://www.microsoft.com/videoplayer/embed/RE4jzx8)
- [เปรียบเทียบการจัดเก็บราคาสินค้า](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/compare-item-price-storage)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เปรียบเทียบรายงานการจัดเก็บราคาสินค้า](../cost-management/compare-item-price.md)
- [รวมการปรับปรุงในการจัดส่ง](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/consolidate-shipment-enhancements)
- [การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/planned-cross-docking)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูวิดีโอ [การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าที่วางแผนไว้](https://www.microsoft.com/videoplayer/embed/RE4f7LF)
- การรวมตามน้ำหนักจริงเพิ่มเติม [10.0.1](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.1), [10.0.2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.2), [10.0.3](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.3), [10.0.4](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.4), [10.0.5](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.5), [10.0.6](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.6), [10.0.7](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/further-catch-weight-integration-10.0.7)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การประมวลผลผลิตภัณฑ์ของน้ำหนักที่เลือกได้ที่มีการจัดการคลังสินค้า](../warehousing/catch-weight-processing.md) และวิดีโอ [การปรับปรุงผลิตภัณฑ์ตามน้ำหนักจริง](https://www.microsoft.com/videoplayer/embed/RE4jzx8) ด้วย
- [การรวมสินทรัพย์ถาวรที่มีวงจรการจัดการสินทรัพย์](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/fixed-assets-integration-asset-management-lifecycle)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รวมการจัดการสินทรัพย์ด้วยสินทรัพย์ถาวร](../asset-management/integration-to-fixed-assets/fixed-asset-integration.md)
- [การจองในมิติระดับคลังสินค้าที่ยืดหยุ่น](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/flexible-warehouse-level-dimension-reservation)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายการจองในมิติระดับคลังสินค้าที่ยืดหยุ่น](../warehousing/flexible-warehouse-level-dimension-reservation.md)
- [อุปกรณ์สำหรับบัตรงานที่ปรับปรุง](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/improved-job-card-device)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รายงานความคืบหน้าของอุปกรณ์เคลื่อนที่ของงาน](../production-control/tasks/report-progress-mobile-job-device.md) และ [รายงานเมื่อเสร็จสมบูรณ์จากอุปกรณ์บัตรงาน](../production-control/report-finished-job-device.md)
- [การตรวจสอบคุณภาพขาเข้า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/inbound-quality-check)
- [การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/inventory-aging-report-storage)
- [ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/inventory-value-report-storage)
- [แผนภูมิ Gantt ของความคืบหน้าในการวางแผนหลัก](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/master-planning-progress-gantt-chart)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบการรันการวางแผนหลัก](../master-planning/tasks/monitor-master-planning-run.md) และรวมถึงวิดีโอ [การปรับปรุงประสิทธิภาพการทำงานและการใช้งานของ MRP](https://www.microsoft.com/videoplayer/embed/RE4myrJ)
- [เอนทิตี้ข้อมูลใหม่สำหรับพื้นที่การผลิต](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/new-data-entities-manufacturing-area)
- [การเรียงลำดับขาออก](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/outbound-sorting)
- [การจัดส่งเทียบกับมิติการจัดเก็บ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)
- [การยืนยันแบบขนานของแผนการใบสั่ง](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/parallelized-firming-planned-orders)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การยืนยันแบบพร้อมกัน](../master-planning/maintain-planned-orders.md#parallelize-firming) และรวมถึงวิดีโอ [การปรับปรุงประสิทธิภาพการทำงานและการใช้งานของ MRP](https://www.microsoft.com/videoplayer/embed/RE4myrJ)
- [การเพิ่มประสิทธิภาพในการวางแผนสำหรับการกระจาย](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/planning-optimization-distribution)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของการเพิ่มประสิทธิภาพการวางแผน](../master-planning/planning-optimization/planning-optimization-overview.md)
- [การปรับปรุงข้อตกลงการซื้อ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/purchase-agreement-enhancements)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ข้อตกลงการซื้อ](../procurement/purchase-agreements.md)
- [ย้ายเก็บคลัสเตอร์](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/put-away-clusters) <br> - สำหรับข้อมูลเพิ่มเติม ให้ดูวิดีโอ [ย้ายเก็บการจัดคลัสเตอร์](https://www.microsoft.com/videoplayer/embed/RE4f5aB)
- [วางไปที่ผนัง/ใส่ไปที่ร้านค้า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/put-wallput-store)
- [รับการจัดเรียง](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/receive-sortation)
- [การจัดส่งพัสดุขนาดเล็ก (SPS)](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/small-package-shipping-sps)
- [การประมูลของผู้จัดจำหน่าย—คำถามจากผู้จัดจำหน่ายและการตอบสนองโดยสรุป](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/vendor-bidding-questions-vendors-summarized-responses)
- [การจัดกำหนดการแบบภาพสำหรับใบสั่งงานในการจัดการสินทรัพย์](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/visual-scheduling-work-orders-asset-management)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การทำงานกับใบสั่งงานที่จัดกำหนดการโดยใช้แผนภูมิ gantt](../asset-management/work-order-scheduling/schedule-work-orders.md#gantt)
- [การแบ่งช่วงเวลาของคลังสินค้า](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-slotting)
- [การเพิ่มประสิทธิภาพในการพิมพ์ป้ายชื่อเวฟ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/wave-label-printing-enhancements)
- [รหัสขั้นตอนของเวฟ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/wave-step-code)<br> - สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รหัสขั้นตอนของเวฟ](../warehousing/wave-step-codes.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-update-33"></a>แพลตฟอร์ม update 33

Microsoft Dynamics 365 Supply Chain Management 10.0.9 รวมถึง Platform update 33 เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [คุณลักษณะการแสดงตัวอย่างใน Platform update 33](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-33.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัพเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.9 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=415034&dbType=3&qc=7bdf05cf1859a5a56f4b9c0dae88fa1653d489181b3a2c1f19429225daf5724b)

### <a name="dynamics-365-2020-release-wave-1-plan"></a>Dynamics 365: 2020 แผนเวฟการนำออกใช้ 1

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ตรวจสอบ [Dynamics 365: 2020 แผนเวฟการนำออกใช้ 1](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/index) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

หัวข้อ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในหัวข้อ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัพเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์
