---
title: พารามิเตอร์การรวมบัญชีเงินเดือน
description: บทความนี้อธิบายพารามิเตอร์การรวมบัญชีเงินเดือน Dynamics 365 Human Resources
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896118"
---
# <a name="payroll-integration-parameters"></a>พารามิเตอร์การรวมบัญชีเงินเดือน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ก่อนใช้การรวมบัญชีเงินเดือน Dynamics 365 Human Resources คุณต้องตั้งค่าพารามิเตอร์ที่อธิบายไว้ในบทความนี้

## <a name="enable-payroll-address"></a>เปิดใช้งานที่อยู่ในบัญชีเงินเดือน

หากต้องการให้สามารถใช้ที่อยู่ในบัญชีเงินเดือนได้ คุณต้องเปิดใช้งานที่อยู่นั้นจาก [ฟอร์มพารามิเตอร์ที่ใช้ร่วมกัน](hr-setup-shared-parameters.md) บนแท็บการรวมบัญชีเงินเดือน

## <a name="define-the-identification-type"></a>กำหนดชนิดการระบุรหัสประจำตัว

เมื่อต้องการแสดงรหัสชนิดการระบุรหัสประจำตัวใน [เอนทิตีพนักงานในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-employee.md) คุณต้อง [ตั้งค่าคอนฟิกพารามิเตอร์ทรัพยากรบุคคล](hr-setup-shared-parameters.md) ของแต่ละบริษัท

1. ในพื้นที่ทำงาน **การจัดการค่าตอบแทน** ภายใต้ลิงค์ ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล** 
2. บนแท็บ **การรวมบัญชีเงินเดือน** ให้ระบุค่าของฟิลด์ต่อไปนี้

| ฟิลด์ | คำอธิบาย |
| --- | --- |
| ใช้ชนิดข้อมูลประจำตัวในการประมวลผลค่าจ้าง | เมื่อเลือกตัวเลือกนี้ รหัสชนิดที่เลือกจะแสดงในเอนทิตีของพนักงานในบัญชีเงินเดือน |
| ชนิดข้อมูลประจำตัว | ชนิดการระบุรหัสประจำตัวที่จะแสดงในฟิลด์ ซึ่ง **mshr_payrollemployeeentityid** ของ [เอนทิตีพนักงานในบัญชีเงินเดือน](hr-admin-integration-payroll-api-payroll-employee.md) |

## <a name="see-also"></a>ดูเพิ่มเติมที่

[บทนำ API การรวมบัญชีเงินเดือน](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
