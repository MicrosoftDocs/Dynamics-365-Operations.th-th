---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (14 พฤษภาคม 2020)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 14 พฤษภาคม 2020
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127860"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (14 พฤษภาคม 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.3244 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุน Lifecycle Services (LCS) สำหรับการอ้างอิง

## <a name="platform-changes"></a>การเปลี่ยนแปลงแพลตฟอร์ม

การเปลี่ยนแปลงของแพลตฟอร์มจะรวมอยู่ในการนำออกใช้ของสัปดาห์นี้ เมื่อต้องการเรียนรู้เพิ่มเติม ให้ดูที่ [การอัปเดตแพลตฟอร์มสำหรับรุ่น10.0.10 ของแอป Finance and Operations (พฤษภาคม 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34) การนำออกใช้นี้รวมถึงการแก้ไขข้อผิดพลาดและการเปลี่ยนแปลงในมุมมองที่บันทึกไว้
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>ตรวจสอบให้แน่ใจว่ารายการเบิกสินค้า Dataverse สอดคล้องกับ Leave Enum (436343)

ขณะนี้รายการเบิกสินค้า Dataverse สอดคล้องกับ Leave Enum

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>อนุญาตให้ผู้ใช้ตั้งค่าคอนฟิกลำดับงานคำร้องขอการลาหยุดตามจำนวนที่ร้องขอ (300044)

ผู้ใช้สามารถตั้งค่าคอนฟิกลำดับงานคำร้องขอการลาหยุดตามจำนวนที่ร้องขอ
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>แบบฟอร์มผู้ปฏิบัติงานใหม่แสดงข้อมูลผ่านทางเมนูมุมมองเมื่อมีการเปิดใช้งานการรักษาความปลอดภัยขั้นสูง (403185)

รุ่นนี้จะแก้ไขวิธีการดูผู้ปฏิบัติงานในระหว่างการทำงานของนิติบุคคลเมื่อมีการเปิดใช้งานการเข้าถึงขั้นสูงและผู้ปฏิบัติงานในบริษัทอื่นสามารถเข้าถึงได้

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>อนุญาตให้รันการลางานคงค้างสำหรับแผนเดียวหรือบริษัทเดียว (318844)

ด้วยการเปลี่ยนแปลงนี้คุณสามารถรันการคงค้างสำหรับบริษัทหรือแผน
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>แสดงการเทียบเท่าเต็มเวลาของตำแหน่งงาน (FTE) ในแบบฟอร์มผู้ปฏิบัติงานที่ลงทะเบียน (414658)

ค่า FTE จากตำแหน่งของผู้ปฏิบัติงานจะกำหนดอัตราคงค้างของผู้ปฏิบัติงานเมื่อมีการเปิดใช้งานตัวเลือก FTE บนชนิดการลางาน ขณะนี้ฟิลด์นี้จะรวมอยู่ในแบบฟอร์ม **ผู้ปฏิบัติงานที่ลงทะเบียนแล้ว** และกบ่องโต้ตอบ **การลงทะเบียนโดยรวม**

## <a name="add-leave-balance-expiration-batch-job-431266"></a>เพิ่มชุดงานการหมดอายุของยอดดุลการลา (431266)

ขณะนี้ชุดงานใหม่พร้อมใช้งาน ซึ่งจะรันรายวัน ซึ่งจะลดยอดดุลการลางานที่เหลือเมื่อวันหมดอายุเป็นปัจจุบัน

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>การส่งออกรายชื่อผู้ติดต่อส่วนบุคคลสำหรับพนักงานโดยใช้เอนทิตีผู้ติดต่อส่วนบุคคลของผู้ปฏิบัติงานจะไม่ส่งออกผู้ติดต่อส่วนบุคคลที่มีชนิดความสัมพันธ์หลัก (345893)

เอนทิตีข้อมูล **ผู้ติดต่อส่วนบุคคลผู้ปฏิบัติงาน** (**HcmPersonalContactPersonEntity** ใน DMF และ **PersonalContactPerson** ใน OData) ไม่สามารถส่งออกผู้ติดต่อส่วนบุคคลที่มีชนิดความสัมพันธ์ของข้อมูล **หลัก** ได้รับการแก้ไขปัญหานี้สำหรับผู้ติดต่อส่วนบุคคลที่สร้างขึ้นหลังจากการเปลี่ยนแปลงนี้ ผู้ติดต่อส่วนบุคคลที่มีอยู่ของชนิดข้อมูล **หลัก** จะได้รับการแก้ไขในการนำออกใช้ในภายหลัง

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>รหัสเหตุผลแสดงอยู่ระหว่างสถานการณ์จำลองต่างๆ เมื่อมีการทำเครื่องหมายเป็นการลางานและการขาดงานและมีการเปิดใช้งานแบบฟอร์มพนักงานที่มีการพัฒนา (434163)

การเปลี่ยนแปลงนี้จะจำกัดรหัสเหตุผลให้เป็นรหัสการลาหยุดและการขาดงานเฉพาะเมื่อคุณเปิดใช้งานการป้อนข้อมูลพนักงานที่มีการพัฒนา

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>คุณลักษณะในการแสดงตัวอย่างกำหนดแผนการลางานให้กับพนักงานในอนาคตแสดงข้อผิดพลาด (433555)

การเปลี่ยนแปลงนี้จะแก้ไขข้อผิดพลาดเมื่อแผนการลาออกมีการกำหนดชนิดของการลางานสองชนิดและคุณพยายามกำหนดพนักงาน

## <a name="getting-started-banner-appears-for-all-users-441731"></a>ป้ายโฆษณาการเริ่มต้นใช้งานจะปรากฏสำหรับผู้ใช้ทั้งหมด (441731)

เมื่อมีการเปลี่ยนแปลงนี้ ป้ายโฆษณาเริ่มต้นถูกซ่อนไว้สำหรับผู้ใช้ที่ไม่ใช่ผู้ดูแลระบบหรือผู้ดูแลระบบจัดการข้อมูล 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>เอนทิตีที่อยู่ของผู้ปฏิบัติงาน Dataverse ทำงานแตกต่างกันในแง่ของวันที่ที่มีผลบังคับใช้ในทรัพยากรบุคคล (425071)

การเปลี่ยนแปลงนี้จะช่วยให้ข้อมูลที่อยู่สอดคล้องกับการจัดตำแหน่งในบางสถานการณ์ ตามวันที่ของที่อยู่

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>ไม่สามารถเพิ่มเอกสารแนบให้กับคำขอการลางานที่ได้รับอนุมัติ (425407)

เมื่อมีการนำออกใช้ของสัปดาห์นี้ คุณสามารถเพิ่มไฟล์แนบลงในคำขอที่ได้รับอนุมัติโดยไม่มีการเปลี่ยนแปลงคำขอลางาน

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

## <a name="leave-suspension"></a>การระงับการลางาน

คุณสามารถระงับการลางานและการขาดงานในทรัพยากรบุคคลสำหรับพนักงาน การระงับการลางานจะหยุดการรับรู้การลางานสำหรับชนิดการลางานที่เลือก ถ้าการระงับเกิดขึ้นหลังจากที่มีการประมวลผลการรับรู้ การระงับการลางานจะสร้างการปรับปรุงตามสัดส่วนให้กับยอดดุลการลางานของพนักงาน สำหรับข้อมูลเพิ่มเติม โปรดดู [ระงับการลางาน](hr-leave-and-absence-suspend-leave.md)

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>อัพเดตประสบการณ์ผู้ใช้เพื่อบ่งชี้ว่ารายการคงค้างถูกระงับแล้ว (429550)

ประสบการณ์ผู้ใช้บ่งชี้ว่าการคงค้างถูกระงับสำหรับแผนแล้ว

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>ระงับการคงค้างของการลางานสำหรับชนิดการลางานที่ระบุ (272447)

ในรุ่นนี้ HR สามารถสร้างกฎเพื่อระงับการคงค้างของการลางานสำหรับพนักงานที่มีคำขอลางานที่ป้อนไว้สำหรับการลางานที่ยังไม่ได้ชำระเงิน การลางานที่ยังไม่ได้ชำระสามารถเป็นชนิดได้ แต่ไม่จำเป็นต้องเป็น คุณสามารถระงับการลางานใดๆ ตามชนิดการลางานอื่นได้

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>เอนทิตี DMF ที่พร้อมใช้งานสำหรับการระงับการคงค้าง (429549)

ในปัจจุบันเอนทิตี DMF พร้อมใช้งานสำหรับการระงับการคงค้าง

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>เพิ่มรหัสเหตุผลให้กับการระงับการคงค้าง (429547)

รหัสเหตุผลถูกเพิ่มเข้าในการระงับการคงค้าง

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>เริ่มต้นการเปลี่ยนจากพารามิเตอร์ทรัพยากรบุคคลเป็นพารามิเตอร์การลางานและการขาดงาน

การนำออกใช้นี้จะเริ่มต้นโดยรวมพารามิเตอร์ทรัพยากรบุคคลที่มีพารามิเตอร์การลางานและการขาดงาน

## <a name="carry-forward-rules"></a>กฎการยกยอดไป

คุณสามารถระบุชนิดของการลางานที่ยกยอดไปสำหรับการยกยอดดุลที่ซึ่งมีการโอนย้ายการปรับปรุงแบบยกยอดไป ตัวอย่างเช่น ถ้าพนักงานยกไปข้างหน้า 10 วัน คุณสามารถเลือกชนิดของการลางานที่แตกต่างกันได้สำหรับทั้ง 10 วัน สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน](hr-leave-and-absence-types.md)

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]