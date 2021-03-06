---
title: ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน
description: 'ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ '
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 13e32c9bc77470d6b8e157e7a7805d3d72850478
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114410"
---
# <a name="enroll-and-remove-benefits-from-workers"></a>ลงทะเบียนและลบสวัสดิการจากผู้ปฏิบัติงาน



ขั้นตอนนี้สาธิตว่าผู้ปฏิบัติงานสามารถลงทะเบียนในสวัสดิการอันเดียวหรือมากกว่านั้นได้อย่างไร ตลอดจนผู้ปฏิบัติงานหลายคนสามารถลงทะเบียนได้ในสวัสดิการ  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF


## <a name="enroll-a-single-worker-in-benefits"></a>การลงทะเบียนผู้ปฏิบัติงานคนเดียวในสวัสดิการ
1. ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. คลิก สวัสดิการ
4. คลิก สร้าง
5. ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
6. ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา
7. ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา
8. ขยายส่วนผู้รับผลประโยชน์ ถ้าหากผู้รับผลประโยชน์จำเป็นต้องเพิ่มเข้าไปในสวัสดีการ  คุณสามารถเพิ่มผู้อยู่ในอุปการะจากหน้านี้ถ้าเกี่ยวข้องกับตัวสวัสดิการ
9. นอกจากนี้คุณยังสามารถแก้ไขรายละเอียดของการลงทะเบียนสวัสดิการ หรือลบการลงทะเบียนบนหน้านี้  เมื่อคุณเสร็จสิ้นการทำการเปลี่ยนแปลงกับการลงทะเบียนสวัสดิการ ปิดหน้านี้

## <a name="enroll-multiple-workers-in-a-benefit"></a>การลงทะเบียนผู้ปฏิบัติงานหลายรายในสวัสดิการ
1. ปิดหน้า
2. ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
6. คลิก ลงทะเบียนสวัสดิการ
7. ในฟิลด์สวัสดิการ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
8. ในฟิลด์วันที่เริมต้นความคุ้มครอง ให้ป้อนวันที่และเวลา
9. ในฟิลด์วันที่สิ้นสุดความคุ้มครอง ให้ป้อนวันที่และเวลา
10. คลิกลงทะเบียน
11. ปิดหน้า
12. ไปที่ฝ่ายบุคคล > สวัสดิการ > การลงทะเบียน > ผลการลงทะเบียนสวัสดิการ
13. ค้นหาบันทึกผลสวัสดิการที่กำลังมองหาอยู่
14. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
15. หน้านี้จะช่วยให้คุณดูพนักงานที่ได้ลงทะเบียนในสวัสดิการและพนักงานที่ยังไม่ได้ลงทะเบียน

