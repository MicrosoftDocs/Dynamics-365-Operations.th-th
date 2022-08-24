---
title: แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์ด้วยการใช้เท็มเพลต Excel อีกครั้ง
description: บทความนี้อธิบายวิธีแก้ไขรูปแบบการรายงานอิเล็กทรอนิกส์ (ER) ที่ถูกใช้ในการสร้างเอกสารทางธุรกิจ โดยการนำแม่แบบ Excel ที่แก้ไขไปใช้ใหม่
author: kfend
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 02423a75d96bef0452b8555f8c7a9f0aca0b6771
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283542"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>แก้ไขรูปแบบการรายงานทางอิเล็กทรอนิกส์ด้วยการใช้เท็มเพลต Excel อีกครั้ง

[!include [banner](../includes/banner.md)]

เครื่องมือการรายงานทางอิเล็กทรอนิกส์ (ER) จะถูกใช้ในการสร้างเอกสารทางธุรกิจในรูปแบบอิเล็กทรอนิกส์ ในการสร้างเอกสารทางธุรกิจ คุณต้องสร้างรูปแบบ ER และจากนั้นใช้ตัวออกแบบ ER เพื่อกำหนดโครงร่างของเอกสารทางธุรกิจ และระบุข้อมูลที่ควรรวมอยู่ในตาราง จากนั้นคุณสามารถรันรูปแบบ ER ได้ เพื่อสร้างเอกสารทางธุรกิจ

เครื่องมือ ER สามารถถูกใช้เพื่อสร้างเอกสารทางธุรกิจเป็นไฟล์ Microsoft Excel คุณสามารถใช้เอกสาร Excel เป็นเท็มเพลตสำหรับเอกสารเหล่านี้ได้ เมื่อต้องการกำหนดโครงร่างของเอกสารในตัวออกแบบ ER คุณสามารถนำเข้าเนื้อหาของเอกสาร Excel ที่คุณต้องการใช้เป็นเท็มเพลตลงในรูปแบบ ER ที่กำหนดได้ สำหรับรายละเอียดเพิ่มเติม และเพื่อฝึกฝนสถานการณ์จำลองนี้ เล่นคู่มืองาน **ER ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML** (ส่วนหนึ่งของ 7.5.4.3 จัดหา/พัฒนาบริการด้านไอที/องค์ประกอบโซลูชัน (10677) กระบวนการทางธุรกิจ) ในขั้นตอนคู่มืองานที่คุณนำเข้าเทมเพลต Excel ใช้เทมเพลตเริ่มต้นของแฟ้ม Excel การชำระเงิน [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx)

ถ้าคุณแก้ไขเอกสาร Excel ที่ถูกใช้เป็นเท็มเพลตสำหรับเอกสารทางธุรกิจ ฟังก์ชัน ER ใหม่ช่วยให้คุณสามารถนำเท็มเพลตที่ปรับปรุงแล้วไปใช้กับรูปแบบ ER ได้ จากนั้น รูปแบบ ER ได้รับการปรับปรุงเพื่อให้ได้สอดคล้องกับเท็มเพลตที่มีการอัพเดต สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ เล่นคู่มืองาน **ER ปรับเปลี่ยนรูปแบบตามการนำเท็มเพลต Excel ไปใช้** (ส่วนหนึ่งของ 7.5.5.3 บริการ/โซลูชัน IT รับ/การจัดทำคอมโพเนนต์ (10683) กระบวนการทางธุรกิจ) ในขั้นตอนคู่มืองานที่คุณนำเข้าเทมเพลตที่อัพเดตแล้ว ใช้เทมเพลตที่อัพเดตแล้วของแฟ้ม Excel การชำระเงิน [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[อัปเดตเทมเพลต](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
