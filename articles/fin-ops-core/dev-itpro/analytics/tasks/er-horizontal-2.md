---
title: ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์เวิร์กชีต OPENXML (Excel) (ส่วนที่ 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c13179f424d570b23615fe81ca5ddfb7afed582d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093487"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)

[!include [banner](../../includes/banner.md)]

ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน  สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF 

เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการตามขั้นตอนในกระบวนงาน "ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอนเพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1: ออกแบบรูปแบบ)" ให้เสร็จสมบูรณ์

กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611


## <a name="find-created-format"></a>ค้นหารูปแบบที่สร้างขึ้น
1. ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก
2. ในแผนภูมิ ขยาย 'Financial dimensions sample model'
3. ในแผนภูมิ เลือก 'Financial dimensions sample model\Sample report with horizontally expandable ranges'

## <a name="execute-format-to-create-excel-output"></a>ดำเนินการรูปแบบเพื่อสร้างผลลัพธ์ Excel
1. คลิก เรียกใช้
2. ในฟิลด์ชื่อมิติ พิมพ์ 'BusinessUnit;CostCenter;Department'
    * ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า   เมื่อต้องการเลือกมิติทั้งหมดสำหรับบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. ขยายเรกคอร์ดเพื่อที่จะรวมส่วน
4. คลิกตัวกรอง 
5. เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน
6. ในฟิลด์เกณฑ์ ให้พิมพ์ '00057..00058'
    * 00057..00058  
7. คลิก ตกลง
8. คลิก ตกลง
    * ตรวจทานผลลัพธ์ที่สร้างขึ้น  โปรดทราบว่าไฟล์ Excel ที่สร้างขึ้นใหม่มีจำนวนคอลัมน์ที่เลือกสำหรับมิติทางการเงินเท่ากัน  ส่วนหัวของรายงานในคอลัมน์เหล่านั้นแสดงถึงชื่อของมิติทางการเงิน รายการของธุรกรรมในคอลัมน์เหล่านั้นแสดงถึงมิติทางการเงิน รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]