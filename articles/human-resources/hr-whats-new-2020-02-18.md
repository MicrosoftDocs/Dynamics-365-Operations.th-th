---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (18 กุมภาพันธ์ 2020)
description: บทความนี้อธิบายคุณลักษณะใหม่หรือที่เปลี่ยนแปลงใน Microsoft Dynamics 365 Human Resources สำหรับวันที่ 18 กุมภาพันธ์ 2020
author: andreabichsel
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec7d8dbc73dce57d3968c4d239a51d27673a2493
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066297"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Human Resources (18 กุมภาพันธ์ 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Human Resources การเปลี่ยนแปลงที่ใช้เพื่อสร้างหมายเลข 8.1.2903 ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนของ LCS สำหรับการอ้างอิง

## <a name="platform-update-32"></a>แพลตฟอร์ม update 32 

การปรับปรุงแพลตฟอร์ม 32 พร้อมใช้งานแล้วในขณะนี้ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรในการอัปเดตแพลตฟอร์ม 32 สำหรับการเงินและการดำเนินงาน (กุมภาพันธ์ 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md)

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>ค่าการค้นหาจะถูกจดจำเมื่อมีการเปลี่ยนแปลงตัวเลือกมุมมองในฟอร์มพนักงานที่มีประสิทธิภาพ (383833)

ขณะนี้ฟอร์ม **ผู้ปฏิบัติงาน** ใหม่จะจดจำค่าการค้นหาเมื่อคุณเปลี่ยนตัวเลือกมุมมองและใช้การเปลี่ยนแปลง

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>ไทล์สรุปการจัดการค่าตอบแทนในคุณลักษณะการแสดงตัวอย่างจะเปลี่ยนเส้นทางไปยังฟอร์มที่ไม่ถูกต้อง (401861)

ไทล์การจัดการค่าตอบแทนคงที่และผันแปรแสดงเรกคอร์ดที่ถูกต้องในฟอร์ม **ผู้ปฏิบัติงาน** ใหม่ในขณะนี้ ใช้กับคุณลักษณะการแสดงตัวอย่างฟอร์มพนักงานที่มีประสิทธิภาพเท่านั้น คุณสามารถเปิดใช้งานคุณลักษณะการแสดงตัวอย่างนี้ได้ใน **การจัดการคุณลักษณะ** สำหรับข้อมูลเพิ่มเติม โปรดดู [จัดการผู้คุณลักษณะ](hr-admin-manage-features.md)

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>ฟิลด์สถานะว่างเปล่าสำหรับเรกคอร์ดคำขอลางานบางรายการใน Dataverse (414915)

การเปลี่ยนแปลงนี้แก้ไขปัญหาใน Dataverse เมื่อฟิลด์ **สถานะ** ในคำขอลางานถูกตั้งค่าเป็น **ตรวจทาน** Dataverse ขณะนี้แสดงสถานะ

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>การวิเคราะห์ช่องว่างของทักษะเป็นไปได้สำหรับงานที่มอบหมายเท่านั้น (411390)

ขณะนี้คุณสามารถทำการวิเคราะห์ช่องว่างของทักษะสำหรับงานใดๆ ที่กำหนดไว้ในทรัพยากรบุคคล

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>สกุลเงินของระบบไม่ซิงค์จาก Dataverse ไปยังทรัพยากรบุคคลในสภาพแวดล้อมใหม่ (418011)

ขณะนี้สกุลเงินของระบบใน Dataverse สามารถซิงค์กับทรัพยากรบุคคลได้

## <a name="in-preview"></a>ในการแสดงตัวอย่าง

- [คุณลักษณะการแสดงตัวอย่างการลางานและการขาดงาน](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [คุณลักษณะการแสดงตัวอย่างของการจัดการสวัสดิการ](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>เร็วๆ นี้

### <a name="updated-dataverse-solution"></a>โซลูชัน Dataverse ที่ปรับปรุง

โซลูชัน Dataverse ใหม่จะพร้อมใช้งานเร็วๆ นี้ โดยมีการเปลี่ยนแปลงต่อไปนี้:

| คำอธิบาย | เปลี่ยน |
| ----------------------------------------- | --- |
| เอนทิตี **งาน/ตำแหน่ง** เปลี่ยนแปลง | **ภูมิภาคของค่าตอบแทน** ที่เพิ่ม</br>**มิติทางการเงิน** ที่เพิ่ม |
| เอนทิตี **ผู้ปฏิบัติงาน** เปลี่ยนแปลง | **ลำดับชื่อ** ที่เพิ่ม</br>เพิ่ม **การทำงานจากที่บ้าน** แล้ว</br>**ภาษา** ที่เพิ่ม</br>**วันที่ของอายุงาน** ที่เพิ่ม</br>**วันที่ครบรอบปี** ที่เพิ่ม</br>เพิ่ม **วันที่จ้างงานเดิม** แล้ว |
| เอนทิตี **การจ้างงาน** เปลี่ยนแปลง | **มิติทางการเงิน** ที่เพิ่ม</br>**เหตุผลการสิ้นสุดการจ้างงาน** ที่เพิ่ม</br>**วันที่สิ้นสุดการจ้างงาน** เปลี่ยนชื่อจาก **วันที่เปลี่ยนแปลง**</br>**วันที่ทดลองงาน** ที่เพิ่ม |
| เอนทิตี **ที่อยู่ผู้ปฏิบัติงาน** เปลี่ยนแปลง | **ที่อยู่ถนน** ที่เพิ่ม</br>**บรรทัดที่อยู่ 1** **บรรทัดที่อยู่ 2** และ **บรรทัดที่อยู่ 3** ที่ทำเครื่องหมายสำหรับค่าเสื่อมราคา |
| เอนทิตีการตั้งค่าค่าตอบแทนผันแปรใหม่ | **ชนิดแผนตัวแปรค่าตอบแทน**</br>**แผนค่าตอบแทนผันแปร**</br>**กฎสิทธิพึงได้**</br>**ระดับแผนตัวแปรค่าตอบแทน** |
| เอนทตี **การจ้างงานในปฏิทินของผู้ปฏิบัติงาน** ใหม่ | เพิ่ม **เอนทิตีปฏิทินงาน** แล้ว |
| เอนทตี **รายละเอียดตำแหน่งที่มีค่าจ้าง** ใหม่ | เพิ่ม **รายละเอียดตำแหน่งที่มีค่าจ้าง** แล้ว |
| เอนทิตี้ **ชื่อ** ใหม่ | เพิ่ม **ชื่อ** แล้ว เอนทิตี **ชื่อเรื่อง** ใหม่ จะรวมอยู่ในกระบวนการซิงค์ระหว่างทรัพยากรบุคคลและ Dataverse จะไม่มีการอ้างอิงจากเอนทิตี **ตำแหน่งงาน** หรือ **งาน** ในตอนแรก |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[มีอะไรใหม่หรือมีอะไรเปลี่ยนแปลงใน Human Resources](hr-admin-whats-new.md)</br>
[ภาพรวมของ Dynamics 365 Human Resources 2019 ปล่อยเวฟ 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[อัปเดตกระบวนการ](hr-admin-setup-update-process.md)</br>
[จัดการคุณลักษณะ](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
