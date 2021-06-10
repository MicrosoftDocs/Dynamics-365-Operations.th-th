---
title: รีเซ็ตชุดงานที่ติดค้าง
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาที่มีชุดงานที่ติดขัด
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053526"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="4bac4-103">รีเซ็ตชุดงานที่ติดค้าง</span><span class="sxs-lookup"><span data-stu-id="4bac4-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="4bac4-104">ออก</span><span class="sxs-lookup"><span data-stu-id="4bac4-104">Issue</span></span>

<span data-ttu-id="4bac4-105">Microsoft Dynamics 365 Human Resources สามารถพบปัญหาเกี่ยวกับชุดงานที่ติดขัดในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4bac4-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="4bac4-106">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="4bac4-106">Resolution</span></span>

<span data-ttu-id="4bac4-107">เมื่อชุดงานติดค้างอยู่ในสถานะ **กำลังดำเนินการ** หรือ **กำลังยกเลิก** คุณสามารถรีเซ็ตสถานะโดยการบังคับการยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="4bac4-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="4bac4-108">หลังจากที่คุณยกเลิกชุดงานแล้ว คุณสามารถรีเซ็ตชุดงานได้โดยการตั้งค่าเป็นสถานะ **กำลังรอ**</span><span class="sxs-lookup"><span data-stu-id="4bac4-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="4bac4-109">จากนั้น จะถูกเลือกอีกครั้งสำหรับการดำเนินการในการรันชุดงานที่จัดกำหนดการไว้ถัดไป</span><span class="sxs-lookup"><span data-stu-id="4bac4-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="4bac4-110">ในพื้นที่ทำงาน **การจัดการระบบ** ให้เลือกหน้า **ลิงค์** และเลือก **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="4bac4-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="4bac4-111">ในหน้ารายการ **ชุดงาน** ให้เลือกงานที่ต้องถูกรีเซ็ต</span><span class="sxs-lookup"><span data-stu-id="4bac4-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="4bac4-112">บน Ribbon การดำเนินการ เลือก **บังคับให้ยกเลิก** และยืนยันการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4bac4-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4bac4-113">การดำเนินการ **บังคับให้ยกเลิก** จะพร้อมใช้งานเฉพาะเมื่อชุดงานที่เลือกมีสถานะเป็น **กำลังดำเนินการ** หรือ **กำลังยกเลิก** และไม่มีการรันการดำเนินการชุดงานหรือกระบวนการยกเลิกสำหรับงาน</span><span class="sxs-lookup"><span data-stu-id="4bac4-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="4bac4-114">บน Ribbon การดำเนินการ เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="4bac4-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="4bac4-115">บนหน้า **เลือกสถานะใหม่** ให้เลือก **กำลังรอ** แล้วจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4bac4-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![เลือกสถานะชุดงานใหม่](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="4bac4-117">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4bac4-117">See also</span></span>

[<span data-ttu-id="4bac4-118">ปรับปรุงประสิทธิภาพการทำงานโดยการจัดกำหนดการชุดงานหลังเวลาทำการ</span><span class="sxs-lookup"><span data-stu-id="4bac4-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="4bac4-119">ปรับปรุงประสิทธิภาพการทำงานด้วยงานการล้างข้อมูลอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="4bac4-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
