---
title: ภาพรวมของ MyLeaveRequests
description: เอนทิตี้ MyLeaveRequests ใน Microsoft Dynamics 365 Human Resources แสดงรายการคำขอลางานในระบบ ขอบเขต (จำกัด) ให้กับการเข้าถึงคำขอของเอนทิตี้ผู้ใช้ปัจจุบันที่สอบถาม
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070880"
---
# <a name="myleaverequests-overview"></a>ภาพรวมของ MyLeaveRequests


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
