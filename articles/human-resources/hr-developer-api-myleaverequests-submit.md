---
title: ส่งคำขอลางานไปที่ลำดับงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถใช้แอปพลิเคชัน โปรแกรมมิ่ง อินเทอร์เฟส (API) ของ MyLeaveRequests submit () เพื่อส่งการร้องขอการลางานให้กับลำดับงาน
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba2867646ac03953a43404984a5d04d4edb1f5ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687008"
---
# <a name="submit-a-leave-request-to-workflow"></a>ส่งคำขอลางานไปที่ลำดับงาน


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ใน Microsoft Dynamics 365 Human Resources คุณสามารถใช้แอปพลิเคชัน โปรแกรมมิ่ง อินเทอร์เฟส (API) ของ MyLeaveRequests submit () เพื่อส่งการร้องขอการลางานให้กับลำดับงาน API นี้มีการเปิดเผยเป็นการดำเนินการบนเอนทิตี้ MyLeaveRequests OData

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ต้องบันทึกการร้องขอการลางานไว้ในฐานข้อมูลและต้องเรียกผ่านเอนทิตี้ MyLeaveRequests

## <a name="permissions"></a>สิทธิ์การได้รับอนุญาต

ต้องมีสิทธิ์อย่างใดอย่างหนึ่งต่อไปนี้ในการเรียก API นี้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์และวิธีการเลือก ให้ดูที่ [การรับรองความถูกต้อง](hr-developer-api-authentication.md)

| ชนิดสิทธิ์                    | สิทธิ (จากสิทธิ์น้อยที่สุดไปยังสิทธิ์มากที่สุด) |
|------------------------------------|--------------------------------------------------------|
| มอบหมาย (บัญชีงานหรือโรงเรียน) | ผู้ใช้\_การเลียนแบบ                                    |

## <a name="https-request"></a>คำขอ HTTPS

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

คำขอสอดคล้องกับมาตรฐาน OData พารามิเตอร์ {requestId}, {leaveType}, {leaveDate} และ {dataArea} อ้างอิงถึงฟิลด์ที่ประกอบเป็นคีย์ธรรมชาติสำหรับเอนทิตี้ MyLeaveRequests

> [!NOTE]
> ในขณะที่ฟิลด์สำหรับเอนทิตี้ MyLeaveRequests อ้างอิงถึงบรรทัดใดบรรทัดหนึ่งในการร้องขอการลางาน ให้เรียกการส่ง API จะส่งคำขอการลางานทั้งหมด (บรรทัดทั้งหมด) ไปยังลำดับงาน

### <a name="request-headers"></a>ส่วนหัวของคำขอ

| หัวข้อ         | Value                     |
|----------------|---------------------------|
| การอนุญาต  | ภาระ {token} (จำเป็น) |
| เนื้อหา-ชนิด   | แอปพลิเคชัน/json          |

### <a name="request-body"></a>เนื้อหาของคำขอ

ห้ามจัดหาเนื้อหาของคำขอไว้สำหรับวิธีการนี้

### <a name="response"></a>การตอบสนอง

การตอบสนองที่สำเร็จอยู่เสมอคือการตอบสนอง **204 ไม่มีเนื้อหา**

ผู้ติดต่อที่ไม่ได้รับอนุญาตจะได้รับการตอบสนอง **401 ไม่ได้รับอนุญาต** หรือ **403 ไม่ได้รับอนุญาติ**

ถ้าการส่งไม่สำเร็จ (เนื่องจากการตรวจสอบความถูกต้อง ตัวอย่างเช่น) การตอบสนองจะเป็น **500 ข้อผิดพลาดของเซิร์ฟเวอร์** และเนื้อหาของการตอบสนองจะรวมออบเจ็กต์ JSON ที่มีรายละเอียดเพิ่มเติม

## <a name="example"></a>ตัวอย่าง

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a>การตรวจสอบความถูกต้องและข้อผิดพลาด

ในฐานะที่เป็นส่วนหนึ่งของการเรียกเพื่อส่ง API, ทรัพยากรบุคคลจะทำการตรวจสอบความถูกต้องของตรรกะทางธุรกิจก่อนที่จะส่ง ซึ่งช่วยให้มั่นใจว่าคำขอการลางานอยู่ในสถานะที่ถูกต้องสำหรับการส่ง ข้อความแสดงข้อผิดพลาดที่เป็นไปได้ที่คุณอาจได้รับในการตอบสนองถ้าการตรวจสอบความถูกต้องล้มเหลวดังนี้:

 - คำขอจะวางยอดดุล '{LeaveTypeId}' อยู่ต่ำกว่ายอดดุลขั้นต่ำที่อนุญาตใน {date}
 - คำขอหยุดพักในสถานะเสร็จสมบูรณ์ไม่สามารถส่งได้
 - ไม่สามารถส่งหรือบันทึกคำขอได้เนื่องจากไม่มีการเปลี่ยนแปลงใดๆ เพิ่มหรืออัปเดตจำนวนหรือชนิดการลางาน แล้วลองอีกครั้ง
 - คำขอหยุดพักที่ป้อนไว้ประกอบด้วยวันอย่างน้อยหนึ่งวันที่มีวันที่เดียวกันและชนิดลาเป็นคำขอที่ค้างอยู่ที่มีอยู่ โปรดเรียกคืนคำขอที่มีอยู่เพื่อทำการเปลี่ยนแปลง
 - รหัสเหตุผล '{ReasonCodeId}' ไม่ใช้กับชนิดการลางานใดๆ ในคำขอ
 - ชนิดการลา '{LeaveTypeId} ต้องมีรหัสเหตุผล เลือกชนิดและรหัสเหตุผลที่เหมาะสม
 - การหยุดพักไม่ได้ถูกส่งเป็นที่เรียบร้อย การหยุดพักถูกบันทึกเป็นคำขอฉบับร่าง

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ภาพรวมของ MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [การรับรองความถูกต้อง](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
