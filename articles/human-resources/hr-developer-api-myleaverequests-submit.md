---
title: ส่งคำขอลางานไปที่ลำดับงาน
description: ใน Microsoft Dynamics 365 Human Resources คุณสามารถใช้แอปพลิเคชัน โปรแกรมมิ่ง อินเทอร์เฟส (API) ของ MyLeaveRequests submit () เพื่อส่งการร้องขอการลางานให้กับลำดับงาน
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bd82bef29e5d1d33c1dc1aa3a039833741c1fdaf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793644"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="c0922-103">ส่งคำขอลางานไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c0922-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c0922-104">ใน Microsoft Dynamics 365 Human Resources คุณสามารถใช้แอปพลิเคชัน โปรแกรมมิ่ง อินเทอร์เฟส (API) ของ MyLeaveRequests submit () เพื่อส่งการร้องขอการลางานให้กับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c0922-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="c0922-105">API นี้มีการเปิดเผยเป็นการดำเนินการบนเอนทิตี้ MyLeaveRequests OData</span><span class="sxs-lookup"><span data-stu-id="c0922-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c0922-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="c0922-106">Prerequisites</span></span>

<span data-ttu-id="c0922-107">ต้องบันทึกการร้องขอการลางานไว้ในฐานข้อมูลและต้องเรียกผ่านเอนทิตี้ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="c0922-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="c0922-108">สิทธิ์การได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="c0922-108">Permissions</span></span>

<span data-ttu-id="c0922-109">ต้องมีสิทธิ์อย่างใดอย่างหนึ่งต่อไปนี้ในการเรียก API นี้</span><span class="sxs-lookup"><span data-stu-id="c0922-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="c0922-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์และวิธีการเลือก ให้ดูที่ [การรับรองความถูกต้อง](hr-developer-api-authentication.md)</span><span class="sxs-lookup"><span data-stu-id="c0922-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="c0922-111">ชนิดสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="c0922-111">Permission type</span></span>                    | <span data-ttu-id="c0922-112">สิทธิ (จากสิทธิ์น้อยที่สุดไปยังสิทธิ์มากที่สุด)</span><span class="sxs-lookup"><span data-stu-id="c0922-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c0922-113">มอบหมาย (บัญชีงานหรือโรงเรียน)</span><span class="sxs-lookup"><span data-stu-id="c0922-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c0922-114">ผู้ใช้\_การเลียนแบบ</span><span class="sxs-lookup"><span data-stu-id="c0922-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="c0922-115">คำขอ HTTPS</span><span class="sxs-lookup"><span data-stu-id="c0922-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="c0922-116">คำขอสอดคล้องกับมาตรฐาน OData</span><span class="sxs-lookup"><span data-stu-id="c0922-116">The request conforms to OData standards.</span></span> <span data-ttu-id="c0922-117">พารามิเตอร์ {requestId}, {leaveType}, {leaveDate} และ {dataArea} อ้างอิงถึงฟิลด์ที่ประกอบเป็นคีย์ธรรมชาติสำหรับเอนทิตี้ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="c0922-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="c0922-118">ในขณะที่ฟิลด์สำหรับเอนทิตี้ MyLeaveRequests อ้างอิงถึงบรรทัดใดบรรทัดหนึ่งในการร้องขอการลางาน ให้เรียกการส่ง API จะส่งคำขอการลางานทั้งหมด (บรรทัดทั้งหมด) ไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c0922-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="c0922-119">ส่วนหัวของคำขอ</span><span class="sxs-lookup"><span data-stu-id="c0922-119">Request headers</span></span>

| <span data-ttu-id="c0922-120">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="c0922-120">Header</span></span>         | <span data-ttu-id="c0922-121">Value</span><span class="sxs-lookup"><span data-stu-id="c0922-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="c0922-122">การอนุญาต</span><span class="sxs-lookup"><span data-stu-id="c0922-122">Authorization</span></span>  | <span data-ttu-id="c0922-123">ภาระ {token} (จำเป็น)</span><span class="sxs-lookup"><span data-stu-id="c0922-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="c0922-124">เนื้อหา-ชนิด</span><span class="sxs-lookup"><span data-stu-id="c0922-124">Content-Type</span></span>   | <span data-ttu-id="c0922-125">แอปพลิเคชัน/json</span><span class="sxs-lookup"><span data-stu-id="c0922-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="c0922-126">เนื้อหาของคำขอ</span><span class="sxs-lookup"><span data-stu-id="c0922-126">Request body</span></span>

<span data-ttu-id="c0922-127">ห้ามจัดหาเนื้อหาของคำขอไว้สำหรับวิธีการนี้</span><span class="sxs-lookup"><span data-stu-id="c0922-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="c0922-128">การตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="c0922-128">Response</span></span>

<span data-ttu-id="c0922-129">การตอบสนองที่สำเร็จอยู่เสมอคือการตอบสนอง **204 ไม่มีเนื้อหา**</span><span class="sxs-lookup"><span data-stu-id="c0922-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="c0922-130">ผู้ติดต่อที่ไม่ได้รับอนุญาตจะได้รับการตอบสนอง **401 ไม่ได้รับอนุญาต** หรือ **403 ไม่ได้รับอนุญาติ**</span><span class="sxs-lookup"><span data-stu-id="c0922-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="c0922-131">ถ้าการส่งไม่สำเร็จ (เนื่องจากการตรวจสอบความถูกต้อง ตัวอย่างเช่น) การตอบสนองจะเป็น **500 ข้อผิดพลาดของเซิร์ฟเวอร์** และเนื้อหาของการตอบสนองจะรวมออบเจ็กต์ JSON ที่มีรายละเอียดเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c0922-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="c0922-132">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="c0922-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="c0922-133">การตรวจสอบความถูกต้องและข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="c0922-133">Validation and error messages</span></span>

<span data-ttu-id="c0922-134">ในฐานะที่เป็นส่วนหนึ่งของการเรียกเพื่อส่ง API, ทรัพยากรบุคคลจะทำการตรวจสอบความถูกต้องของตรรกะทางธุรกิจก่อนที่จะส่ง ซึ่งช่วยให้มั่นใจว่าคำขอการลางานอยู่ในสถานะที่ถูกต้องสำหรับการส่ง</span><span class="sxs-lookup"><span data-stu-id="c0922-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="c0922-135">ข้อความแสดงข้อผิดพลาดที่เป็นไปได้ที่คุณอาจได้รับในการตอบสนองถ้าการตรวจสอบความถูกต้องล้มเหลวดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c0922-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="c0922-136">คำขอจะวางยอดดุล '{LeaveTypeId}' อยู่ต่ำกว่ายอดดุลขั้นต่ำที่อนุญาตใน {date}</span><span class="sxs-lookup"><span data-stu-id="c0922-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="c0922-137">คำขอหยุดพักในสถานะเสร็จสมบูรณ์ไม่สามารถส่งได้</span><span class="sxs-lookup"><span data-stu-id="c0922-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="c0922-138">ไม่สามารถส่งหรือบันทึกคำขอได้เนื่องจากไม่มีการเปลี่ยนแปลงใดๆ</span><span class="sxs-lookup"><span data-stu-id="c0922-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="c0922-139">เพิ่มหรืออัพเดตจำนวนหรือชนิดการลางาน แล้วลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c0922-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="c0922-140">คำขอหยุดพักที่ป้อนไว้ประกอบด้วยวันอย่างน้อยหนึ่งวันที่มีวันที่เดียวกันและชนิดลาเป็นคำขอที่ค้างอยู่ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="c0922-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="c0922-141">โปรดเรียกคืนคำขอที่มีอยู่เพื่อทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c0922-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="c0922-142">รหัสเหตุผล '{ReasonCodeId}' ไม่ใช้กับชนิดการลางานใดๆ ในคำขอ</span><span class="sxs-lookup"><span data-stu-id="c0922-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="c0922-143">ชนิดการลา '{LeaveTypeId} ต้องมีรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="c0922-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="c0922-144">เลือกชนิดและรหัสเหตุผลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="c0922-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="c0922-145">การหยุดพักไม่ได้ถูกส่งเป็นที่เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="c0922-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="c0922-146">การหยุดพักถูกบันทึกเป็นคำขอฉบับร่าง</span><span class="sxs-lookup"><span data-stu-id="c0922-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0922-147">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="c0922-147">See also</span></span>

- [<span data-ttu-id="c0922-148">ภาพรวมของ MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="c0922-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="c0922-149">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="c0922-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]