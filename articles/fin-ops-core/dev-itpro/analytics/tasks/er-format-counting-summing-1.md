---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1 - สร้างรูปแบบ)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1742582057cc912d8e6f90eb14e9e4cdcd193608
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684726"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1 - สร้างรูปแบบ)

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ 

เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์

กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>เข้าถึงรายการของการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft
1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
    * ตรวจสอบให้แน่ใจว่า "Litware, Inc." พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน  
2. เลือก "Litware, Inc." ผู้ให้บริการ
3. คลิก ที่เก็บ
    * ถ้ามีที่เก็บชนิด "ทรัพยากรการดำเนินงาน" อยู่แล้ว ให้ข้ามขั้นตอนที่เหลือของงานย่อยปัจจุบัน  
4. คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง
5. ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'
6. คลิกสร้างที่จัดเก็บ
7. คลิก ตกลง

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>เรียกการตั้งค่าคอนฟิกอินทราสแทตที่จัดเตรียมให้โดย Microsoft
1. คลิก เปิด
2. ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'
3. คลิก นำเข้า
    * คลิก นำเข้าสำหรับรุ่น 1.1 ของการจัดโครงแบบที่เลือก  
4. คลิก ใช่
5. ปิดหน้า
6. ปิดหน้า
7. คลิก การตั้งค่าคอนฟิกการรายงาน
8. ในแผนภูมิ ขยาย 'Intrastat model'
9. ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]