---
title: FAQ เกี่ยวกับลำดับงาน
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงาน
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0188e8ed3cbbfd7dbccd7d13cf6129e146a919ac
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772708"
---
# <a name="workflow-faq"></a><span data-ttu-id="9a39a-103">FAQ เกี่ยวกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a39a-104">หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="9a39a-105">ทำไมได้รับการแจ้งเตือนจำนวนมากเมื่อรายการงานถูกปฏิเสธ?</span><span class="sxs-lookup"><span data-stu-id="9a39a-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="9a39a-106">เมื่อรายการงานถูกปฏิเสธ รายการงานถูกทำให้เสร็จสมบูรณ์เป็นถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="9a39a-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="9a39a-107">รายการงานอีกรายการถูกสร้างขึ้น และถูกกำหนดให้กับผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="9a39a-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="9a39a-108">นี่หมายความว่า มีการแจ้งเตือนไปยังผู้ริเริ่มสำหรับรายการงานที่ถูกปฏิเสธ และการแจ้งเตือนแบบแยกต่างหากของผู้ใช้ที่กำหนดให้กับรายการงาน "การเปลี่ยนแปลงที่ร้องขอ" ใหม่</span><span class="sxs-lookup"><span data-stu-id="9a39a-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="9a39a-109">การแจ้งเตือนแต่ละรายการมีไว้สำหรับรายการงานที่แตกต่างกัน แต่ความคล้ายคลึงอาจก่อให้เกิดความสับสน</span><span class="sxs-lookup"><span data-stu-id="9a39a-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="9a39a-110">เรากำลังดูที่วิธีการปรับปรุงรายการนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="9a39a-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="9a39a-111">เหตุใดการส่งออกลำดับงานของฉันจึงล้มเหลว?</span><span class="sxs-lookup"><span data-stu-id="9a39a-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="9a39a-112">ขณะนี้มีข้อจำกัดในลักษณะการทำงานในการส่งออกลำดับงานที่ป้องกันไม่ให้ชื่อลำดับงานเกิน 48 อักขระ</span><span class="sxs-lookup"><span data-stu-id="9a39a-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="9a39a-113">การใช้ชื่อที่ยาวกว่า 48 อักขระอาจส่งผลให้เกิดข้อผิดพลาด "เซิร์ฟเวอร์ล้มเหลวในการรับรองความถูกต้องคำขอ" และ/หรือ ป้องกันไม่ให้ไฟล์ถูกส่งออกโดยไม่มีชนิดของไฟล์</span><span class="sxs-lookup"><span data-stu-id="9a39a-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="9a39a-114">โพสต์บล็อกต่อไปนี้ให้รายละเอียดเพิ่มเติม [การแก้ไขปัญหาการส่งออกลำดับงาน](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="9a39a-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="9a39a-115">ผู้ส่งของลำดับงานสามารถอนุมัติลำดับงานได้ด้วยใช่หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="9a39a-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="9a39a-116">ใช่ ผู้ส่งของลำดับงานยังสามารถอนุมัติลำดับงานได้ด้วย ถ้ามีการตั้งค่าคอนฟิกด้วยวิธีการนั้น</span><span class="sxs-lookup"><span data-stu-id="9a39a-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="9a39a-117">เมื่อต้องการป้องกันไม่ให้เกิดคุณลักษณะนี้ ตั้งค่า **พารามิเตอร์ลำดับงาน > ทั่วไป > ผู้อนุมัติ > ไม่อนุญาตให้มีการอนุมัติโดยผู้ส่ง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9a39a-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="9a39a-118">ฉันสามารถเพิ่มการแจ้งเตือนไปยังลำดับงานเพื่อให้การแจ้งเตือนแก่ผู้ใช้ได้หรือไม่?</span><span class="sxs-lookup"><span data-stu-id="9a39a-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="9a39a-119">ต่อไปนี้เป็นพื้นที่สำคัญบางประการที่ต้องทราบเกี่ยวกับการเพิ่มการแจ้งเตือนไปยังลำดับงานเพื่อให้การแจ้งเตือน:</span><span class="sxs-lookup"><span data-stu-id="9a39a-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="9a39a-120">การแจ้งเตือนเทียบกับกลไกการแจ้งเตือนลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="9a39a-121">สามารถตั้งค่าข้อความแจ้งเตือนสำหรับการเปลี่ยนแปลงของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="9a39a-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="9a39a-122">ลำดับงานเปลี่ยนแปลงเรกคอร์ด จึงเป็นไปได้ที่จะตั้งค่าการแจ้งเตือนที่เกี่ยวข้องกับการเปลี่ยนแปลงเรกคอร์ดที่มีสาเหตุมาจากลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="9a39a-123">อย่างไรก็ตาม เนื่องจากลำดับงานมีตัวเลือกการแจ้งเตือนภายในที่แตกต่างกัน การใช้ข้อความแจ้งเตือนจึงไม่ได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="9a39a-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="9a39a-124">การแจ้งเตือนมาตรฐานจากลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="9a39a-125">ลำดับงานได้สร้างขึ้นในการแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="9a39a-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="9a39a-126">ลูกค้าสามารถตั้งค่าคอนฟิกการแจ้งเตือน เพื่อให้ผู้ใช้ส่งอีเมลได้</span><span class="sxs-lookup"><span data-stu-id="9a39a-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="9a39a-127">การแจ้งเตือนเหล่านั้นจะไม่ทำให้เกิดข้อความของศูนย์ปฏิบัติการสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9a39a-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="9a39a-128">ในการปรับปรุงในอนาคต เราจะเพิ่มข้อความของศูนย์ปฏิบัติการ เพื่อให้ผู้ใช้ได้รับการกำหนดรายการงานของลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="9a39a-129">การเพิ่มการแจ้งเตือนไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="9a39a-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="9a39a-130">สามารถสร้างข้อความของศูนย์ปฏิบัติการสำหรับผู้ใช้เฉพาะ เช่น ข้อความที่สร้างขึ้นจากลำดับงานใน X++</span><span class="sxs-lookup"><span data-stu-id="9a39a-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="9a39a-131">[ลำดับงานมีเหตุการณ์ทางธุรกิจ](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) ที่ลูกค้าสามารถใช้เพื่อทริกเกอร์โฟลว์ให้มีการแจ้งเตือนที่พวกเขากำลังค้นหา</span><span class="sxs-lookup"><span data-stu-id="9a39a-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="9a39a-132">โดยสรุป ถ้าผู้ใช้ไม่ได้รับการแจ้งเตือนที่เหมาะสมจากศูนย์ปฏิบัติการ เมื่อมีการกำหนดรายการงานของลำดับงาน ให้ใช้ [เหตุการณ์ทางธุรกิจของลำดับงาน](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) ที่มี Microsoft Power Automate เพื่อให้การแจ้งเตือนเพิ่มเติมหรือการแจ้งเตือนที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="9a39a-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>
