---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (18 กุมภาพันธ์ 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Human Resources
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077472"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (18 กุมภาพันธ์ 2020)

บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2903 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="platform-update-32"></a>แพลตฟอร์ม update 32 

การปรับปรุงแพลตฟอร์ม 32 พร้อมใช้งานแล้วในขณะนี้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรในการปรับปรุงแพลตฟอร์ม 32 สำหรับ Finance and Operations (กุมภาพันธ์ 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>ค่าการค้นหาจะถูกจดจำเมื่อมีการเปลี่ยนแปลงตัวเลือกมุมมองในฟอร์มพนักงานที่มีประสิทธิภาพ (383833)

ขณะนี้ฟอร์ม **ผู้ปฏิบัติงาน** ใหม่จะจดจำค่าการค้นหาเมื่อคุณเปลี่ยนตัวเลือกมุมมองและใช้การเปลี่ยนแปลง

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>ไทล์สรุปการจัดการค่าตอบแทนในคุณลักษณะการแสดงตัวอย่างจะเปลี่ยนเส้นทางไปยังฟอร์มที่ไม่ถูกต้อง (401861)

ไทล์การจัดการค่าตอบแทนคงที่และผันแปรแสดงเรกคอร์ดที่ถูกต้องในฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ในขณะนี้ ใช้กับคุณลักษณะการแสดงตัวอย่างฟอร์มพนักงานที่มีประสิทธิภาพเท่านั้น คุณสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างนี้ได้ใน **การจัดการคุณลักษณะ** สำหรับข้อมูลเพิ่มเติม โปรดดู [จัดการผู้คุณลักษณะ](hr-admin-manage-features.md)

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>ฟิลด์สถานะว่างเปล่าสำหรับเรกคอร์ดคำขอลางานบางรายการใน Common Data Service (414915)

การเปลี่ยนแปลงนี้แก้ไขปัญหาใน Common Data Service เมื่อฟิลด์ **สถานะ** ในคำขอลางานถูกตั้งค่าเป็น **ตรวจทาน** Common Data Service ขณะนี้แสดงสถานะ

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>การวิเคราะห์ช่องว่างของทักษะเป็นไปได้สำหรับงานที่มอบหมายเท่านั้น (411390)

ขณะนี้คุณสามารถทำการวิเคราะห์ช่องว่างของทักษะสำหรับงานใดๆ ที่กำหนดไว้ในทรัพยากรบุคคล

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>สกุลเงินของระบบไม่ซิงค์จาก Common Data Service ไปยังทรัพยากรบุคคลในสภาพแวดล้อมใหม่ (418011)

ขณะนี้สกุลเงินของระบบใน Common Data Service สามารถซิงค์กับทรัพยากรบุคคลได้

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

- [คุณลักษณะการแสดงตัวอย่างการลางานและการขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [คุณลักษณะการแสดงตัวอย่างของการจัดการสวัสดิการ](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="updated-common-data-service-solution"></a>โซลูชัน Common Data Service ที่ปรับปรุง

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
