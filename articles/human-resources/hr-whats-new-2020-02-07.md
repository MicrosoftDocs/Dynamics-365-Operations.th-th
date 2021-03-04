---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (7 กุมภาพันธ์ 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 7 กุมภาพันธ์ 2020
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fac6e34db10efb047b4cb0fc3c7752330e5bcf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526962"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (7 กุมภาพันธ์ 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2835 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>การเรียนรู้การวิเคราะห์ไม่แสดงหลักสูตรถ้าห้องเรียนว่างเปล่า (388289)

หน้าการเรียนรู้การวิเคราะห์แสดงหลักสูตรในขณะนี้ถ้าห้องเรียนว่างเปล่า

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>การค้นหาตำแหน่งไม่ใช้โซนเวลาลงในบัญชี (405344)

การค้นหาสำหรับตำแหน่งงานที่เปิดในขณะนี้คำนึงถึงโซนเวลาเมื่อตรวจสอบความถูกต้องว่ามีตำแหน่งเปิดอยู่หรือไม่

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>มุมมองการวิเคราะห์ยอดคงเหลือปัจจุบันไม่ได้อัพเดตด้วยยอดดุลคงเหลือการลางานปัจจุบันที่ถูกต้องหลังจากที่ส่งการร้องขอเวลาหยุดพัก (409756)

ยอดดุลปัจจุบันขณะนี้รวมการร้องขอเวลาหยุดพักที่ส่งแล้ว

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ตัวอย่างคุณลักษณะต่อไปนี้จะพร้อมใช้งานในวันที่ 3 กุมภาพันธ์ 2020:

- **ตัวอย่างคุณลักษณะการลางานและขาดงาน** - สำหรับข้อมูลเพิ่มเติมโปรดดู [ตัวอย่างคุณลักษณะการลางานและขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **คุณลักษณะการแสดงตัวอย่างการจัดการสวัสดิการ** - สำหรับข้อมูลเพิ่มเติม ซึ่งรวมทั้งปัญหาที่ทราบ โปรดดู [ภาพรวมการจัดการสวัสดิการ](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="platform-update-32"></a>แพลตฟอร์ม update 32 

แพลตฟอร์มที่อัพเดต 32 จะพร้อมใช้งานในไม่ช้า [ค้นหาข้อมูลเพิ่มเติมเกี่ยวกับแพลตฟอร์มที่อัพเดต 32 ได้ที่นี่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)

### <a name="updated-common-data-service-solution"></a>อัพเดตโซลูชัน Common Data Service

โซลูชัน Common Data Service ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:

| คำอธิบาย | เปลี่ยน |
| ----------------------------------------- | --- |
| เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง | **ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</br>**มิติทางการเงิน** ที่เพิ่ม |
| เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง | **ลำดับชื่อ** ที่เพิ่ม</br>เพิ่ม **การทำงานจากที่บ้าน** แล้ว</br>**ภาษา** ที่เพิ่ม</br>**วันที่ของอายุงาน** ที่เพิ่ม</br>**วันที่ครบรอบปี** ที่เพิ่ม</br>เพิ่ม **วันที่จ้างงานเดิม** แล้ว |
| เอนทิตี **การจ้างงาน** เปลี่ยนแปลง | **มิติทางการเงิน** ที่เพิ่ม</br>**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</br>**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</br>**วันที่ทดลองงาน** ที่เพิ่ม |
| เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง | **ที่อยู่ถนน** ที่เพิ่ม</br>**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา |
| เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่ | **ชนิดแผนตัวแปรค่าตอบแทน**</br>**แผนค่าตอบแทนผันแปร**</br>**กฎสิทธิพึงได้**</br>**ระดับแผนตัวแปรค่าตอบแทน** |
| เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่ | เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว |
| เอนทตี **รายละเอียดตำแหน่งที่มีค่าจ้าง** ใหม่ | เพิ่ม **รายละเอียดตำแหน่งที่มีค่าจ้าง** แล้ว |
| เอนทิตี้ **ชื่อ** ใหม่ | เพิ่ม **ชื่อ** แล้ว เอนทิตี **ชื่อเรื่อง** ใหม่ จะรวมอยู่ในกระบวนการซิงค์ระหว่างทรัพยากรบุคคลและ Common Data Service จะไม่มีการอ้างอิงจากเอนทิตี **ตำแหน่งงาน** หรือ **งาน** ในตอนแรก |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]