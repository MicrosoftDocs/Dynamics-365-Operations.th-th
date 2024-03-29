---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.20 (สิงหาคม 2021)
description: บทความนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Dynamics 365 Supply Chain Management 10.0.20
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d99a7a7d0261ba0afd19efbb237dff329527723d
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219168"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.20 (สิงหาคม 2021)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.20 รุ่นนี้มีหมายเลขการสร้างเป็น 10.0.886 และพร้อมใช้งานดังนี้:

- **การนำออกใช้ของการแสดงตัวอย่าง:** พฤษภาคม 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตด้วยตนเอง):** กรกฎาคม 2021
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** สิงหาคม 2021

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้มีคุณลักษณะที่รวมอยู่ในการนำออกใช้นี้ คอลัมน์ *คุณลักษณะ* จะแสดงลิงค์ไปยัง [แผนการนำออกใช้](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) ซึ่งคุณสามารถดูวันที่นำออกใช้ที่เป็นทางการของแต่ละคุณลักษณะได้ คอลัมน์ *ข้อมูลเพิ่มเติม* จะแสดงข้อมูลและ/หรือลิงค์เพิ่มเติมไปที่เอกสารที่เกี่ยวข้อง

คุณลักษณะเหล่านี้ส่วนใหญ่ต้องถูกเปิดใช้งานโดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ก่อนที่คุณจะสามารถใช้งานได้

| พื้นที่คุณลักษณะ | ลักษณะการทำงาน | ข้อมูลเพิ่มเติม |
|---|---|---|
| สินค้าคงคลัง&nbsp;และ&nbsp;ลอจิสติกส์ | [การปรับปรุงประสิทธิภาพรายละเอียดใบสั่งขาย](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | คุณลักษณะนี้ช่วยให้อินเทอร์เฟสผู้ใช้มีมากมายเมื่อเปิดใบสั่งขาย โดยเฉพาะใบสั่งที่มีหลายบรรทัด |
| การผลิต | [เรียกขั้นตอนระบบอัตโนมัติของกระบวนการเพื่อสร้างใบสั่งตรวจสอบคุณภาพ](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [เรียกขั้นตอนระบบอัตโนมัติของกระบวนการเพื่อสร้างใบสั่งตรวจสอบคุณภาพ](../production-control/process-automation-quality-orders.md ) |
| การผลิต | [อินเทอร์เฟสการดำเนินการผลิตขั้นสูงสำหรับการผลิต](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [ตั้งค่าคอนฟิกอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-configure.md) |
| การวางแผน | [การจัดกำหนดการความสามารถรองรับที่ไม่จำกัดสำหรับการเพิ่มประสิทธิภาพการวางแผน](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [การจัดกำหนดการที่มีกำลังการผลิตแบบไม่จำกัด](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| การจัดการข้อมูลผลิตภัณฑ์ | [จัดการการเปลี่ยนแปลงในสูตรและส่วนผสมของสูตร](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [จัดการการเปลี่ยนแปลงในสูตรและส่วนผสมของสูตร](../engineering-change-management/manage-formula-changes.md) |
| การจัดการข้อมูลผลิตภัณฑ์ | [การตรวจสอบความพร้อมของผลิตภัณฑ์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [ความพร้อมของผลิตภัณฑ์](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>การปรับปรุงคุณลักษณะรวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้มีการปรับปรุงคุณลักษณะที่รวมอยู่ในการนำออกใช้นี้ แต่ละประเภทมีการปรับปรุงส่วนเพิ่มให้กับคุณลักษณะที่มีอยู่ เนื่องจากเป็นการปรับปรุงเท่านั้น จึงไม่มีอยู่ใน [แผนการนำออกใช้](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) อย่างไรก็ตาม เพื่อให้แน่ใจว่าการปรับปรุงเหล่านี้จะไม่ขัดแย้งกับการเลือกเองหรือคุณลักษณะที่มีอยู่ของคุณ แต่ละรายการจะถูกปิดตามค่าเริ่มต้น (เว้นแต่จะไม่ได้ระบุไว้เป็นอย่างอื่น) หากคุณต้องการใช้คุณลักษณะเหล่านี้ คุณต้องเปิดใช้งานคุณลักษณะเหล่านี้อย่างชัดแจ้งใน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

| โมดูล | ชื่อ&nbsp;คุณลักษณะ&nbsp;ในการจัดการ&nbsp;คุณลักษณะ | ข้อมูลเพิ่มเติม |
|---|---|---|
| การวางแผนหลัก | การอนุมัติการคาดการณ์ความต้องการที่ปรับแล้วแบบคู่ขนาน | คุณลักษณะการทำงานนี้จะอนุญาตให้สร้างการคาดการณ์ความต้องการที่ปรับปรุงแล้วพร้อมกันได้จากหน้า **การคาดการณ์ความต้องการที่ปรับปรุงแล้ว** วัตถุประสงค์ของคุณลักษณะการได้รับอนุญาตนี้คือการเพิ่มประสิทธิภาพการได้รับอนุญาตเมื่อมีการอนุมัติการคาดการณ์จํานวนมาก เมื่อทำการอนุมัติ ผู้ใช้สามารถระบุ **จํานวนของเธรด** ในกล่องโต้ตอบการยืนยันได้ |
| การวางแผนหลัก | การยืนยันและการรวมบัญชีที่สามารถทำงานแบบชุดงานสำหรับใบสั่งชุดงานรวมจำนวนมากที่วางแผนไว้ | คุณลักษณะนี้ช่วยให้คุณสามารถใช้งานของชุดงานเพื่อยืนยันและรวมบัญชีใบสั่งชุดงานรวมจำนวนมากที่วางแผนไว้ |
| การควบคุมการผลิต | คัดลอกเส้นทางทั่วไป | คุณลักษณะนี้จะช่วยปรับปรุงฟังก์ชันคัดลอกกระบวนการผลิตเพื่ออนุญาตให้ผู้ใช้คัดลอกกระบวนการผลิตที่ไม่ได้เจาะจงสินค้า ซึ่งช่วยให้ระบบสามารถอัปเดตข้อมูลที่เกี่ยวข้องทั้งหมด (เช่น ไซต์ กลุ่มของกระบวนการผลิต ความต้องการทรัพยากร และเวลาต่างๆ) หลังจากใช้ฟังก์ชันคัดลอกกระบวนการผลิตเพื่อบันทึกทับกระบวนการผลิตที่ยังไม่ได้มอบหมายให้กับสินค้า |
| การควบคุมการผลิต | อัปเดตความต้องการทรัพยากรที่เกี่ยวข้องเมื่อมีการเปลี่ยนแปลงการดำเนินการเส้นทาง | คุณลักษณะนี้ช่วยให้ระบบสามารถอัปเดตความต้องการทรัพยากรที่เกี่ยวข้องหลังจากที่ผู้ใช้เปลี่ยนการดำเนินการของขั้นตอนเส้นทางที่มีอยู่ |
| การจัดการข้อมูลผลิตภัณฑ์ | การประมวลผลล่วงหน้าของรายงานสูตรการผลิตเพื่อป้องกันการหมดเวลา | คุณลักษณะการทำงานนี้จะส่งผลให้รายงานสูตรการผลิตได้รับการประมวลผลล่วงหน้า ซึ่งจะหลีกเลี่ยงปัญหาการหมดเวลาเมื่อมีการโหลดข้อมูลขนาดใหญ่ของรายงาน |
| การจัดซื้อและการจัดหา | เปิดใช้งานการรีเซ็ตเวิร์กโฟลว์ที่เกี่ยวข้องกับการจัดซื้อ | คุณลักษณะการแสดงตัวอย่างนี้จะช่วยให้คุณสามารถรีเซ็ตเวิร์กโฟลว์ต่อไปนี้เป็นสถานะร่างได้ ได้แก่ ใบสั่งซื้อ การเปลี่ยนแปลงของผู้จัดจำหน่าย และใบขอซื้อ |
| การจัดการการขนส่ง | เปิดใช้งานการสร้างสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายเมื่อละทิ้งบิลค่าขนส่ง | เมื่อเปิดใช้งานคุณลักษณะนี้ จะมีการสร้างสมุดรายวันใบแจ้งหนี้ของผู้จัดจำหน่ายที่ตรงกันเพื่อเหตุผลการกระทบยอดเมื่อคุณใช้ตัวเลือก "การชำระเงินผู้จัดจำหน่าย" เท่านั้น หรือจะมีการสร้างสมุดรายวันใบแจ้งหนี้เสมอ |
| การจัดการคลังสินค้า | ตรวจสอบความถูกต้องของเท็มเพลตที่เลือกสำหรับงานการเติมสินค้า | คุณลักษณะนี้ช่วยให้มั่นใจว่าผู้ใช้เลือกแม่แบบการเติมสินค้าที่ถูกต้องเมื่อตั้งค่างานการเติมสินค้า ซึ่งป้องกันผู้ใช้จากการสร้างงานการเติมสินค้าที่ไม่มีแม่แบบและเลือกแม่แบบที่มีชนิดเป็น *ความต้องการเวฟ* ซึ่งจะไม่สร้างงานการเติมสินค้า และอาจใช้เวลายาวนานในการประมวลผล |

## <a name="new-and-updated-documentation-resources"></a>ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัพเดต

เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัปเดตบทความความช่วยเหลือต่อไปนี้อย่างมาก ไม่จำเป็นต้องมีความเกี่ยวข้องกับลักษณะการทำงานใหม่ที่เพิ่มสำหรับรุ่นนี้ ตามที่แสดงรายการไว้ในส่วนก่อนหน้านี้ แต่อาจช่วยให้คุณสามารถเพิ่มเติมจากลักษณะการทำงานที่มีอยู่ได้

| พื้นที่คุณลักษณะ | บทความใหม่หรือที่อัปเดต |
|---|---|
| การจัดการการเปลี่ยนแปลงทางวิศวกรรม | [สถานะของวงจรการใช้และธุรกรรมผลิตภัณฑ์](../engineering-change-management/product-lifecycle-state-transactions.md) |
| การบริหารสินค้าคงคลัง | [Add-in การแสดงผลสินค้าคงคลัง](../inventory/inventory-visibility.md)<br><br>[ภาพรวมการจัดการคุณภาพและความไม่สอดคล้องกัน](../inventory/quality-management-processes.md) (บวกบทความการจัดการคุณภาพที่เกี่ยวข้องทั้งหมด) |
| การจัดซื้อและการจัดหา | [รักษาใบรับรองของผู้จัดจำหน่าย](../../finance/public-sector/manage-vendor-certification.md) |
| การควบคุมการผลิต | [ออกแบบอินเทอร์เฟสการดำเนินการผลิต](../production-control/production-floor-execution-styles.md) |
| การจัดการคลังสินค้า | [กําหนดไอคอนและชื่อขั้นตอนสำหรับแอป Warehouse Management บนมือถือ](../warehousing/step-icons-titles.md)<br><br>[การประมวลผลความเคลื่อนไหวของสินค้าคงคลังด้วยตนเองที่รอการตัดบัญชี](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>การอัปเดตแพลตฟอร์มสำหรับแอปการเงินและการดำเนินงาน

Microsoft Dynamics 365 Supply Chain Management 10.0.20 รวมถึง Platform update หากต้องการเรียนรู้เพิ่มเติม โปรดดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.20 ของแอปการเงินและการดำเนินงาน (กรกฎาคม 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.20 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) 

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

