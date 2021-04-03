---
title: ภาพรวมของ MyLeaveRequests
description: เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465521"
---
# <a name="myleaverequests-overview"></a>ภาพรวมของ MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม

## <a name="key"></a>คีย์

  | ชื่อคุณสมบัติ | ชนิดข้อมูล |
  |---------------|-----------|
  | dataAreaId    | สตริง    |
  | รหัสคำขอ     | สตริง    |
  | LeaveType     | สตริง    |
  | LeaveDate     | วัน เดือน      |
  
## <a name="properties"></a>คุณสมบัติ

  | ชื่อคุณสมบัติ     | ชนิดข้อมูล | ต้องระบุ |
  |-------------------|-----------|----------|
  | dataAreaId        | สตริง    | X        |
  | รหัสคำขอ         | สตริง    | X        |
  | LeaveType         | สตริง    | X        |
  | LeaveDate         | วัน เดือน      | X        |
  | ReasonCodeId      | สตริง    |          |
  | PersonnelNumber   | สตริง    | X        |
  | วันที่คำขอ       | วัน เดือน      | X        |
  | ข้อคิดเห็น           | สตริง    |          |
  | สถานะ            | Enum      | X        |
  | จำนวน            | จำนวนจริง      |          |
  | HalfDayDefinition | Enum      |          |

## <a name="actions"></a>การดำเนินการ

 | ชื่อการดำเนินการ                               | คำอธิบาย                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [ส่ง](hr-developer-api-myleaverequests-submit.md)   | ส่งคำขอที่จะประมวลผลโดยลำดับงาน |

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ส่งคำขอลางานไปที่ลำดับงาน](hr-developer-api-myleaverequests-submit.md)
- [การรับรองความถูกต้อง](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]