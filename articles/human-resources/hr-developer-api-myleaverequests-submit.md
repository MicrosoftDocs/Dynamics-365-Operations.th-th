---
title: ส่งคำขอลางานไปที่ลำดับงาน
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010778"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="6558a-102">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6558a-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="6558a-103">ใน Microsoft Dynamics 365 Human Resources คุณสามารถใช้แอปพลิเคชัน โปรแกรมมิ่ง อินเทอร์เฟส (API) ของ MyLeaveRequests submit () เพื่อส่งการร้องขอการลางานให้กับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6558a-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="6558a-104">API นี้มีการเปิดเผยเป็นการดำเนินการบนเอนทิตี้ MyLeaveRequests OData</span><span class="sxs-lookup"><span data-stu-id="6558a-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6558a-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6558a-105">Prerequisites</span></span>

<span data-ttu-id="6558a-106">ต้องบันทึกการร้องขอการลางานไว้ในฐานข้อมูลและต้องเรียกผ่านเอนทิตี้ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6558a-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="6558a-107">สิทธิ์การได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="6558a-107">Permissions</span></span>

<span data-ttu-id="6558a-108">ต้องมีสิทธิ์อย่างใดอย่างหนึ่งต่อไปนี้ในการเรียก API นี้</span><span class="sxs-lookup"><span data-stu-id="6558a-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6558a-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์และวิธีการเลือก ให้ดูที่ [การรับรองความถูกต้อง](hr-developer-api-authentication.md)</span><span class="sxs-lookup"><span data-stu-id="6558a-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="6558a-110">ชนิดสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="6558a-110">Permission type</span></span>                    | <span data-ttu-id="6558a-111">สิทธิ (จากสิทธิ์น้อยที่สุดไปยังสิทธิ์มากที่สุด)</span><span class="sxs-lookup"><span data-stu-id="6558a-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="6558a-112">มอบหมาย (บัญชีงานหรือโรงเรียน)</span><span class="sxs-lookup"><span data-stu-id="6558a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6558a-113">ผู้ใช้\_การเลียนแบบ</span><span class="sxs-lookup"><span data-stu-id="6558a-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="6558a-114">คำขอ HTTPS</span><span class="sxs-lookup"><span data-stu-id="6558a-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="6558a-115">คำขอสอดคล้องกับมาตรฐาน OData</span><span class="sxs-lookup"><span data-stu-id="6558a-115">The request conforms to OData standards.</span></span> <span data-ttu-id="6558a-116">พารามิเตอร์ {requestId}, {leaveType}, {leaveDate} และ {dataArea} อ้างอิงถึงฟิลด์ที่ประกอบเป็นคีย์ธรรมชาติสำหรับเอนทิตี้ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6558a-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="6558a-117">ในขณะที่ฟิลด์สำหรับเอนทิตี้ MyLeaveRequests อ้างอิงถึงบรรทัดใดบรรทัดหนึ่งในการร้องขอการลางาน ให้เรียกการส่ง API จะส่งคำขอการลางานทั้งหมด (บรรทัดทั้งหมด) ไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="6558a-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="6558a-118">ส่วนหัวของคำขอ</span><span class="sxs-lookup"><span data-stu-id="6558a-118">Request headers</span></span>

| <span data-ttu-id="6558a-119">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="6558a-119">Header</span></span>         | <span data-ttu-id="6558a-120">Value</span><span class="sxs-lookup"><span data-stu-id="6558a-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="6558a-121">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="6558a-121">Authorization</span></span>  | <span data-ttu-id="6558a-122">ภาระ {token} (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="6558a-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="6558a-123">เนื้อหา-ชนิด</span><span class="sxs-lookup"><span data-stu-id="6558a-123">Content-Type</span></span>   | <span data-ttu-id="6558a-124">แอปพลิเคชัน/json</span><span class="sxs-lookup"><span data-stu-id="6558a-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="6558a-125">เนื้อหาของคำขอ</span><span class="sxs-lookup"><span data-stu-id="6558a-125">Request body</span></span>

<span data-ttu-id="6558a-126">ห้ามจัดหาเนื้อหาของคำขอไว้สำหรับวิธีการนี้</span><span class="sxs-lookup"><span data-stu-id="6558a-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="6558a-127">การตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="6558a-127">Response</span></span>

<span data-ttu-id="6558a-128">การตอบสนองที่สำเร็จอยู่เสมอคือการตอบสนอง **204 ไม่มีเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="6558a-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="6558a-129">ผู้ติดต่อที่ไม่ได้รับอนุญาตจะได้รับการตอบสนอง **401 ไม่ได้รับอนุญาต** หรือ **403 ไม่ได้รับอนุญาติ**</span><span class="sxs-lookup"><span data-stu-id="6558a-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="6558a-130">ถ้าการส่งไม่สำเร็จ (เนื่องจากการตรวจสอบความถูกต้อง ตัวอย่างเช่น) การตอบสนองจะเป็น **500 ข้อผิดพลาดของเซิร์ฟเวอร์** และเนื้อหาของการตอบสนองจะรวมออบเจ็กต์ JSON ที่มีรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6558a-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="6558a-131">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="6558a-131">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="6558a-132">การตรวจสอบความถูกต้องและข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="6558a-132">Validation and error messages</span></span>

<span data-ttu-id="6558a-133">ในฐานะที่เป็นส่วนหนึ่งของการเรียกเพื่อส่ง API, ทรัพยากรบุคคลจะทำการตรวจสอบความถูกต้องของตรรกะทางธุรกิจก่อนที่จะส่ง ซึ่งช่วยให้มั่นใจว่าคำขอการลางานอยู่ในสถานะที่ถูกต้องสำหรับการส่ง</span><span class="sxs-lookup"><span data-stu-id="6558a-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="6558a-134">ข้อความแสดงข้อผิดพลาดที่เป็นไปได้ที่คุณอาจได้รับในการตอบสนองถ้าการตรวจสอบความถูกต้องล้มเหลวดังนี้:</span><span class="sxs-lookup"><span data-stu-id="6558a-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="6558a-135">คำขอจะวางยอดดุล '{LeaveTypeId}' อยู่ต่ำกว่ายอดดุลขั้นต่ำที่อนุญาตใน {date}</span><span class="sxs-lookup"><span data-stu-id="6558a-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="6558a-136">คำขอหยุดพักในสถานะเสร็จสมบูรณ์ไม่สามารถส่งได้</span><span class="sxs-lookup"><span data-stu-id="6558a-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="6558a-137">ไม่สามารถส่งหรือบันทึกคำขอได้เนื่องจากไม่มีการเปลี่ยนแปลงใดๆ</span><span class="sxs-lookup"><span data-stu-id="6558a-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="6558a-138">เพิ่มหรืออัพเดตจำนวนหรือชนิดการลางาน แล้วลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="6558a-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="6558a-139">คำขอหยุดพักที่ป้อนไว้ประกอบด้วยวันอย่างน้อยหนึ่งวันที่มีวันที่เดียวกันและชนิดลาเป็นคำขอที่ค้างอยู่ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="6558a-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="6558a-140">โปรดเรียกคืนคำขอที่มีอยู่เพื่อทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="6558a-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="6558a-141">รหัสเหตุผล '{ReasonCodeId}' ไม่ใช้กับชนิดการลางานใดๆ ในคำขอ</span><span class="sxs-lookup"><span data-stu-id="6558a-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="6558a-142">ชนิดการลา '{LeaveTypeId} ต้องมีรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="6558a-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="6558a-143">เลือกชนิดและรหัสเหตุผลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6558a-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="6558a-144">การหยุดพักไม่ได้ถูกส่งเป็นที่เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="6558a-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="6558a-145">การหยุดพักถูกบันทึกเป็นคำขอฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="6558a-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="6558a-146">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="6558a-146">See also</span></span>

- [<span data-ttu-id="6558a-147">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6558a-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="6558a-148">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6558a-148">Authentication</span></span>](hr-developer-api-authentication.md)