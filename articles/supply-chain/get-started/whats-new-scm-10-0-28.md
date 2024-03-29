---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.28 (สิงหาคม 2022)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management 10.0.28
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 184da494b9998e3e1cf6bd1639b452192d7e7857
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427832"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Supply Chain Management 10.0.28 (สิงหาคม 2022)

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลงอย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Supply Chain Management รุ่น 10.0.28 รุ่นนี้มีหมายเลขบิลด์เป็น 10.0.1264 และพร้อมใช้งานในกำหนดการต่อไปนี้:

- **การนำออกใช้ของการแสดงตัวอย่าง:** พฤษภาคม 2022
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตด้วยตนเอง):** กรกฎาคม 2022
- **ความพร้อมใช้งานทั่วไปของการนำออกใช้ (การอัปเดตอัตโนมัติ):** กรกฎาคม 2022

## <a name="features-included-in-this-release"></a>คุณลักษณะที่รวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้แสดงรายการคุณลักษณะที่ถูกรวมอยู่ในการนำออกใช้นี้ เราอาจอัปเดตบทความนี้เพื่อรวมคุณลักษณะที่จะเพิ่มลงในบิลด์หลังจากที่มีการเผยแพร่บทความนี้ในครั้งแรก

| พื้นที่คุณลักษณะ | คุณลักษณะ | ข้อมูลเพิ่มเติม | เปิดใช้งานโดย |
|---|---|---|---|
| สินค้าคงคลังและลอจิสติกส์ | [เอนทิตีการรวมต้นทุนแฝงเกี่ยวกับผู้ขนส่งสินค้าของบุคคลที่สาม](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [ภาพรวมของเอนทิตีต้นทุนแฝง](../landed-cost/landed-cost-entities-overview.md) | เปิดใช้งานตามค่าเริ่มต้น |
| การวางแผน | [การวางแผนความต้องการวัสดุที่ขับเคลื่อนด้วยความต้องการ (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [ภาพรวมการวางแผนความต้องการวัสดุที่ขับเคลื่อนด้วยอุปสงค์](../master-planning/planning-optimization/ddmrp-overview.md) | การจัดการคุณลักษณะ:<br>*(พรีวิว) DDMRP สำหรับการเพิ่มประสิทธิภาพการวางแผน* |
| การวางแผน | [การรองรับการเพิ่มประสิทธิภาพการวางแผนสำหรับปริมาณที่สามารถสัญญาได้ (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | [คํานวณวันที่จัดส่งสินค้าตามใบสั่งขายโดยใช้ CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) | การจัดการคุณลักษณะ:<br>*(พรีวิว) CTP สำหรับการเพิ่มประสิทธิภาพการวางแผน* |
| การวางแผน | [การสนับสนุนการเพิ่มประสิทธิภาพการวางแผนสำหรับอายุการเก็บ](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | [การวางแผนหลักของผลิตภัณฑ์ที่มีอายุการเก็บที่จํากัด](../master-planning/planning-optimization/shelf-life.md) | เปิดใช้งานตามค่าเริ่มต้น |

## <a name="feature-enhancements-included-in-this-release"></a>การปรับปรุงคุณลักษณะรวมอยู่ในการนำออกใช้นี้

ตารางต่อไปนี้แสดงรายการการปรับปรุงคุณลักษณะที่ถูกรวมอยู่ในการนำออกใช้นี้ การปรับปรุงเหล่านี้แต่ละรายการให้การปรับปรุงส่วนเพิ่มให้กับคุณลักษณะที่มีอยู่ เนื่องจากเป็นการปรับปรุงเท่านั้น จึงไม่ถูกแสดงรายการใน [แผนการนำออกใช้](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) อย่างไรก็ตาม เพื่อให้แน่ใจว่าการปรับปรุงเหล่านี้จะไม่ขัดแย้งกับการเลือกเองหรือคุณลักษณะที่มีอยู่ของคุณ แต่ละรายการจะถูกปิดตามค่าเริ่มต้น (เว้นแต่จะไม่ได้ระบุไว้เป็นอย่างอื่น)

หากคุณต้องการเปิดหรือปิดคุณลักษณะใดๆ เหล่านี้ คุณต้องทำเช่นนั้นใน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

| โมดูล | ชื่อคุณลักษณะในการจัดการคุณลักษณะ | ข้อมูลเพิ่มเติม |
|---|---|---|
| การจัดการสินค้าคงคลังและคลังสินค้า | เปิดใช้งานปริมาณคงเหลือระหว่างบริษัทเพื่อแสดงปริมาณคงเหลือที่ไม่ใช่ศูนย์เท่านั้น | คุณลักษณะการเช่นนี้จะช่วยให้คุณสามารถเลือกได้ว่า ควรรวมสินค้าที่มีปริมาณคงคลังคงเหลือเป็นศูนย์ไว้ในรายการปริมาณคงคลังคงเหลือระหว่างบริษัทหรือไม่ คุณสามารถควบคุมตัวเลือกนี้โดยใช้การตั้งค่า **อย่าแสดงสินค้าที่มีปริมาณคงคลังคงเหลือเป็นศูนย์ในรายการปริมาณคงคลังคงเหลือระหว่างบริษัท** ซึ่งคุณลักษณะการนี้เพิ่มที่หน้า **พารามิเตอร์ Warehouse Management และคลังสินค้า** |
| การจัดการสินค้าคงคลังและคลังสินค้า | (อินเดีย) สำหรับกฎราคาการโอนย้าย ให้ละเว้นสถานที่ตั้งเมื่อตั้งค่า "รหัสคลังสินค้าเริ่มต้น" เป็น "ทั้งหมด" | <p>คุณลักษณะนี้จะใช้กับการแปลเป็นภาษาท้องถิ่นของอินเดียเท่านั้น ซึ่งช่วยให้กระบวนการตั้งค่าราคาโอนของสินค้าในการโอนย้ายสินค้าคงคลังมีหลายรายการมากขึ้น</p><p>คุณตั้งค่าราคาโอนย้ายโดยการตั้งค่าคอนฟิกสินค้าแต่ละรายการด้วยกฎการกําหนดราคาโอนย้าย วิธีการหนึ่งในการกําหนดค่าคอนฟิกนี้จะรวมรายการกฎที่มีการตั้งค่าฟิลด์ **รหัสคลังสินค้าเริ่มต้น** เป็น *ทั้งหมด* การตั้งค่านี้บ่งชี้ว่าราคาโอนที่กําหนดโดยรายการควรใช้โดยไม่พิจารณาคลังสินค้าที่จะใช้ในการเบิกสินค้า เมื่อคุณลักษณะนี้เปิดใช้งาน กฎราคาโอนย้ายที่มีการตั้งค่าฟิลด์ **รหัสคลังสินค้าเริ่มต้น** เป็น *ทั้งหมด* จะละเว้นการตั้งค่า **ที่ตั้ง** ดังนั้น กฎจะใช้โดยไม่พิจารณาที่ตั้งที่ระบุไว้บนใบสั่งโอนย้าย ลักษณะการทำงานเช่นนี้อาจเป็นสิ่งที่ต้องการ เนื่องจากที่ตั้งอยู่ใต้คลังสินค้าในลำดับชั้นมิติการจัดเก็บ</p><p>หากไม่มีคุณลักษณะนี้ ระบบจะให้ใช้กฎชนิดนี้เฉพาะเมื่อที่ตั้งในใบสั่งโอนย้ายตรงกับที่ตั้งที่ตั้งค่าไว้ของกฎเท่านั้น (หากตั้งค่าที่ตั้งที่ว่างเปล่าสำหรับกฎ ระบบจะใช้กฎนี้กับใบสั่งโอนย้ายที่เป็นค่าว่างเปล่าของที่ตั้งนั้นด้วยเท่านั้น)</p> |
| การจัดการสินค้าคงคลังและคลังสินค้า | การล้างข้อมูลรายงานปริมาณคงเหลือของสินค้าคงคลัง | คุณลักษณะนี้มีวิธีการล้างข้อมูลที่ใช้เพื่อสร้างรายงาน *การจัดเก็บรายงานปริมาณสินค้าคงคลังคงเหลือ* |
| การควบคุมการผลิต | กำหนดกิจกรรมโครงการสำหรับข้อตกลงการบริการและรายการใบสั่งบริการ | คุณลักษณะนี้จะเพิ่มฟิลด์ที่ตั้งชื่อเป็น **กิจกรรมของโครงการ** ในข้อตกลงการให้บริการและบรรทัดใบสั่งบริการ เพื่อให้คุณสามารถตั้งค่ากิจกรรมโครงการได้ คุณลักษณะนี้จะช่วยป้องกันข้อผิดพลาดการบล็อคเมื่อคุณลงรายการบัญชีสมุดรายวันโครงการการจัดการงานบริการที่ต้องการให้ตั้งค่ากิจกรรมโครงการ  |
| การจัดการคลังสินค้า | บริการการเลือกรายการโอนย้ายด้วยตนเองสำหรับผู้ดูแลระบบหรือผู้ใช้ที่ไว้ใจได้ที่คล้ายกัน | คุณลักษณะนี้ยังอนุญาตให้ผู้ดูแลระบบเลือกธุรกรรมสินค้าคงคลังที่เกี่ยวข้องกับบรรทัดการโอนย้ายด้วยตนเองได้ รายการเหล่านี้ที่ถูกนำออกใช้ไปยังคลังสินค้าแล้ว ผู้ดูแลระบบควรทำการเบิกสินค้านี้เฉพาะในกรณีที่เป็นกรณีพิเศษเท่านั้น เช่น เมื่อระบบอยู่ในสถานะได้รับความเสียหาย สำหรับข้อมูลเพิ่มเติม ให้ดู [จัดการข้อยกเว้นของการเลือกรายการขายและการโอนย้ายด้วยตนเอง](../warehousing/manual-order-line-picking-exception-handling.md) |

## <a name="new-and-updated-documentation-resources"></a>ทรัพยากรคู่มือใหม่และคู่มือที่มีการอัปเดต

เมื่อเร็ว ๆ นี้เรามีการเพิ่มหรืออัปเดตบทความความช่วยเหลือต่อไปนี้อย่างมาก บทความเหล่านี้อาจไม่เกี่ยวข้องกับคุณลักษณะใหม่ที่ถูกเพิ่มให้กับการนำออกใช้นี้ ตามที่แสดงรายการในส่วนก่อนหน้านี้ อย่างไรก็ตาม รายการเหล่านั้นอาจช่วยให้คุณใช้ประโยชน์ได้มากขึ้นจากคุณลักษณะที่มีอยู่

| พื้นที่คุณลักษณะ | บทความใหม่หรือที่อัปเดต |
|---|---|
| การจัดการต้นทุน | [ราคาการรับสินค้าแบบคงที่](../cost-management/fixed-receipt-price.md) |
| การจัดการต้นทุน | [คำถามที่ถามบ่อยเกี่ยวกับการคิดต้นทุนสินค้าคงคลัง](../cost-management/inventory-costing-faq.md) |
| การจัดการต้นทุน | [หลักการบัญชีสำหรับลงรายการบัญชีค่าใช้จ่าย](../cost-management/post-to-charge-account-accounting-principle.md) |
| การบริหารสินค้าคงคลัง | [รายละเอียดธุรกรรมสินค้าคงคลัง](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

### <a name="platform-updates-for-finance-and-operations-apps"></a>การอัปเดตแพลตฟอร์มสำหรับแอปการเงินและการดำเนินงาน

Microsoft Dynamics 365 Supply Chain Management 10.0.28 รวมถึง Platform update หากต้องการเรียนรู้เพิ่มเติม โปรดดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น 10.0.28 ของแอปการเงินและการดำเนินงาน (สิงหาคม 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md)

### <a name="bug-fixes"></a>การแก้ไขปัญหา

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการแก้ไขบักที่รวมอยู่ในการอัปเดตแต่ละรายการที่เป็นส่วนหนึ่งของ 10.0.28 ให้ลงชื่อเข้าใช้ Lifecycle Services (LCS) และดู [บทความ KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438)

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 และระบบคลาวด์อุตสาหกรรม: 2022 แผนเวฟการนำออกใช้ 1

สงสัยเกี่ยวกับความสามารถที่กำลังจะเกิดขึ้นและที่เผยแพร่เมื่อเร็วๆ นี้ในแอปหรือแพลตฟอร์มทางธุรกิจใดๆ ของเราใช่ไหม

ดู [Dynamics 365 และระบบคลาวด์อุตสาหกรรม: 2022 แผนเวฟการนำออกใช้ 1](/dynamics365-release-plan/2022wave1/) เราได้บันทึกทุกรายละเอียดอย่างครอบคลุมตั้งแต่ต้นจนจบในเอกสารเดียวที่คุณสามารถใช้สำหรับการวางแผนได้

### <a name="removed-and-deprecated-supply-chain-management-features"></a>คุณลักษณะ Supply Chain Management ที่ถูกลบและที่ถูกยกเลิกการใช้

บทความ [คุณลักษณะที่ถูกลบและที่ถูกยกเลิกการใช้ใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) จะอธิบายถึงคุณลักษณะที่ได้รับหรือถูกจัดกำหนดการให้ถูกลบหรือถูกยกเลิกการใช้สำหรับ Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

ก่อนที่คุณลักษณะใดๆ จะถูกลบออกจากผลิตภัณฑ์ จะมีการประกาศการแจ้งเตือนการยกเลิกการใช้ในบทความ [คุณลักษณะที่ถูกลบหรือที่ถูกเลิกใช้งานใน Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 เดือนก่อนการลบ

สำหรับการจำแนกการเปลี่ยนแปลงที่มีผลกระทบเฉพาะต่อเวลาการคอมไพล์ แต่เป็นไบนารีที่เข้ากันได้กับสภาพแวดล้อม sandbox และสภาพแวดล้อมการผลิต เวลาในการยกเลิกการใช้จะน้อยกว่า 12 เดือน โดยทั่วไป รายการเหล่านี้คือการอัปเดตการทำงานที่จำเป็นต้องทำกับคอมไพเลอร์

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

