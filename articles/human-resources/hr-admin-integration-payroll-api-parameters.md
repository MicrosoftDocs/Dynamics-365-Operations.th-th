---
title: พารามิเตอร์การรวมบัญชีเงินเดือน
description: หัวข้อนี้อธิบายพารามิเตอร์การรวมบัญชีเงินเดือน Dynamics 365 Human Resources
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
ms.openlocfilehash: 0c489b99d5d05ddac46d222e701512288aeb10583a5e829212e0e1c924622f16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712084"
---
# <a name="payroll-integration-parameters"></a>พารามิเตอร์การรวมบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ก่อนใช้การรวมบัญชีเงินเดือน Dynamics 365 Human Resources คุณต้องตั้งค่าพารามิเตอร์ที่อธิบายไว้ในหัวข้อนี้

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
