---
title: นำเข้ารูปแบบสำหรับการรวมข้อมูล
description: หัวข้อนี้ให้ข้อมูลที่มีรายละเอียดเกี่ยวกับการนําเข้ารูปแบบที่ใช้เมื่อคุณรวมข้อมูลทางการเงินจากนิติบุคคลหลายราย
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a8ba65ecc27bb152b1b368e870b15544d9599968
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978547"
---
# <a name="import-format-for-consolidation"></a>นำเข้ารูปแบบสำหรับการรวมข้อมูล

[!include [banner](../includes/banner.md)]

หัวข้อนี้ให้ข้อมูลที่มีรายละเอียดเกี่ยวกับการนําเข้ารูปแบบที่ใช้เมื่อคุณรวมข้อมูลทางการเงินจากนิติบุคคลหลายราย การนําเข้ารูปแบบต้องบันทึกเป็นไฟล์ข้อความ (.txt)

## <a name="import-format"></a>รูปแบบการนำเข้า

ตารางต่อไปนี้แสดงรายการรูปแบบการนําเข้าที่คุณควรใช้เมื่อคุณรวมบัญชีระหว่างการนําเข้า

| ตารางเรกคอร์ด | รูปแบบ | บันทึกย่อ |
|--------------|---------|-------|
| 1            | 170150 ค่าความนิยม 4 | <ul><li>ตารางบันทึก</li><li>รหัสบัญชีหลักต้นทาง</li><li>แถวบัญชีหลัก</li><li>ประเภทบัญชีหลัก</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>รหัสบัญชีหลัก</li><li>วันที่ทำธุรกรรม</li><li>ชนิดรอบระยะเวลาทางบัญชี (**0** = Opening, **1** = Operating, และ **2** = Closing)</li><li>สกุลเงินของธุรกรรม</li><li>เดบิตหรือเครดิต (**0** = Debit และ **1** = Credit)</li><li>ชั้นของการลงรายการบัญชี</li><li>ยอดเงินธุรกรรม</li><li>ปริมาณ</li><li>RecID เฉพาะที่ (ค่า int64 เฉพาะที่ที่ไม่ชัดเจนและไม่ซ้ำกันของธุรกรรม)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>หมายเลขรายการ (หมายเลขธุรกรรมของหัวข้องบประมาณ)</li><li>วันที่ของหัวข้องบประมาณ</li><li>รหัสงบประมาณของรุ่น</li><li>ค่าจํานวนเต็มการแจงนับสำหรับประเภทธุรกรรม (ว่างเปล่า งบประมาณเดิม เป็นต้น)</li><li>วันที่ของรายการ</li><li>รหัสบัญชีหลักเกี่ยวกับรายการ</li><li>รหัสสกุลเงินสำหรับรายการสมุดรายวัน</li><li>ยอดเงินของรายการในธุรกรรมเกี่ยวกับสกุลเงิน</li><li>ค่าจํานวนเต็มการแจงนับสำหรับประเภทงบประมาณของรายการ (ค่าใช้จ่ายหรือรายได้)</li></ul> |
| 4            | DEMF | RecordCompany เป็นนิติบุคคลต้นทาง |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | RecordCompany เป็นนิติบุคคลต้นทาง |
| 6 ชั่วโมง            | BusinessUnit, 1 Department, 2 | แอททริบิวต์มิติทางการเงินที่กำหนดไว้ในส่วนของคำสั่ง<p>คุณสามารถใช้หน้า **ส่งออก** เพื่อตรวจสอบวิธีการกําหนดแอททริบิวต์</p> |
| 7            | 002,1,658 | <ul><li>ค่ามิติทางการเงิน</li><li>มิติทางการเงินเป็นดัชนีที่ระบุใน RecordDimensions</li><li>รหัสเรกคอร์ดเฉพาะที่ไม่ชัดเจนซึ่งเชื่อมโยงกับรหัสเรกคอร์ดเฉพาะจาก RecordTrans หรือ RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>ค่ามิติที่เชื่อมโยงกับธุรกรรมจาก RecordBudget</li><li>มิติทางการเงินเป็นดัชนีที่ระบุใน RecordDimensions</li><li>รหัสเรกคอร์ดรายการที่ไม่ชัดเจนที่สอดคล้องกับลำดับของรายการธุรกรรมในไฟล์</li></ul> |
