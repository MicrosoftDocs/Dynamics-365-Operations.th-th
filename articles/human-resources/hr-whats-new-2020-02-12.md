---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (12 กุมภาพันธ์ 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 12 กุมภาพันธ์ 2020
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
ms.openlocfilehash: b89e022441f69825d9c9c56ecdbca2e09e461b9e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526955"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (12 กุมภาพันธ์ 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2867 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>สามารถเข้าถึงเอนทิตี CompFixedEmpls และ HcmPersonImage ที่มีอยู่ได้จาก OData (414178)

ด้วยการนำออกใช้ของสัปดาห์ เอนทิตี **CompFixedEmpls** และ **HcmPersonImage** ในขณะนี้เป็นแบบสาธารณะ และมีให้บริการผ่าน ODAta

## <a name="delete-employment-from-common-data-service-doesnt-work-when-employment-details-arent-active-403193"></a>การลบการจ้างงานจาก Common Data Service ไม่สามารถใช้งานได้ เมื่อรายละเอียดการจ้างงานไม่ได้ใช้งานอยู่ (403193)

การเปลี่ยนแปลงนี้ช่วยให้คุณสามารถลบการจ้างงานผ่าน Common Data Service เมื่อไม่มีรายละเอียดการจ้างงานที่ใช้งานอยู่

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>ลำดับงานการลงทะเบียนหลักสูตรจะเปลี่ยนสถานะเป็นเสร็จสมบูรณ์และข้อผิดพลาดหลังจากการอนุมัติครั้งที่สอง (409749)

มีการปรับปรุงลำดับงานการลงทะเบียนหลักสูตรเพื่ออนุญาตให้มีผู้อนุมัติหลายราย

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

ตัวอย่างคุณลักษณะต่อไปนี้จะพร้อมใช้งานในวันที่ 3 กุมภาพันธ์ 2020:

- **ตัวอย่างคุณลักษณะการลางานและขาดงาน** - สำหรับข้อมูลเพิ่มเติมโปรดดู [ตัวอย่างคุณลักษณะการลางานและขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **ตัวอย่างคุณลักษณะการจัดการสวัสดิการ** - สำหรับข้อมูลเพิ่มเติมรวมทั้งปัญหาที่ทราบโปรดดู [ภาพรวมการจัดการสวัสดิการ](hr-benefits-management-overview.md)

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