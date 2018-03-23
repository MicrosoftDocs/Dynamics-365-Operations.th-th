---
title: "พื้นที่ทำงานแบบเคลื่อนที่สำหรับการอนุมัติใบสั่งซื้อ"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานการอนุมัติใบสั่งซื้อแบบเคลื่อนที่ ที่ให้คุณดูใบสั่งซื้อและตอบสนองได้โดยใช้การดำเนินการ ตัวอย่างเช่น คุณสามารถอนุมัติ หรือปฏิเสธใบสั่งซื้อ"
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 24a17d3734e39815684098f694a77e96cdbc1cfe
ms.openlocfilehash: d366ae53f4a9d8e676c3bc19e0450baa254cb716
ms.contentlocale: th-th
ms.lasthandoff: 03/07/2018

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="fe607-104">พื้นที่ทำงานแบบเคลื่อนที่สำหรับการอนุมัติใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fe607-104">Purchase order approval mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="fe607-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานของ **การอนุมัติใบสั่งซื้อ** แบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="fe607-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="fe607-106">พื้นที่ทำงานนี้ช่วยให้คุณสามารถดูใบสั่งซื้อ และตอบสนองได้โดยใช้การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="fe607-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="fe607-107">ตัวอย่างเช่น คุณสามารถอนุมัติ หรือปฏิเสธใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fe607-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="fe607-108">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fe607-108">Overview</span></span> 
<span data-ttu-id="fe607-109">ใบสั่งซื้อที่ต้องมีการอนุมัติเพื่อเข้าถึงลำดับงานการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fe607-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="fe607-110">ลำดับงานอาจรวมถึงขั้นตอนต่าง ๆ ที่จำเป็นที่บุคคลหนึ่งคนหรือมากกว่านั้นต้องดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="fe607-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="fe607-111">ตัวอย่างเช่น บุคคลอาจต้องทำงานหรืออนุมัติใบสั่งซื้อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fe607-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="fe607-112">พื้นที่ทำงานแบบเคลื่อนที่ของ **อนุมัติใบสั่งซื้อ** ช่วยให้คุณสามารถดูและตอบสนองใบสั่งจากอุปกรณ์เคลื่อนซื้อได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="fe607-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="fe607-113">พื้นที่ทำงานนี้ช่วยให้คุณสามารถใช้การดำเนินเกี่ยวกับการลำดับงานเช่นเดียวกันกับที่คุณสามารถได้รับจากเว็บเคลแอนต์ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="fe607-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe607-114">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fe607-114">Prerequisites</span></span>
<span data-ttu-id="fe607-115">ข้อกำหนดเบื้องต้นเปลี่ยนแปลง โดยขึ้นอยู่กับเวอร์ชันของ Finance and Operations ที่นำไปใช้งานสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="fe607-116">ข้อกำหนดเบื้องต้นหากคุณใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="fe607-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span></span> 
<span data-ttu-id="fe607-117">ถ้า Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ถูกปรับใช้สำหรับองค์กรของคุณแล้ว ผู้ดูแลระบบต้องเผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ **การอนุมัติใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="fe607-117">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="fe607-118">สำหรับคำแนะนำ ให้ดูที่ [เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)</span><span class="sxs-lookup"><span data-stu-id="fe607-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="fe607-119">ข้อกำหนดเบื้องต้นถ้าคุณใช้ Microsoft Dynamics 365 for Operations รุ่น 1611 ที่มีการอัพเดตแพลตฟอร์ม 3 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="fe607-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="fe607-120">ถ้ามีการปรับใช้ Microsoft Dynamics 365 for Operations รุ่น 1611 ที่มีการอัพเดตแพลตฟอร์ม 3 หรือรุ่นที่ใหม่กว่าสำหรับองค์กรของคุณ ผู้ดูแลระบบต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe607-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe607-121">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fe607-121">Prerequisite</span></span></th>
<th><span data-ttu-id="fe607-122">บทบาท</span><span class="sxs-lookup"><span data-stu-id="fe607-122">Role</span></span></th>
<th><span data-ttu-id="fe607-123">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fe607-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe607-124">การใช้ KB 4017918</span><span class="sxs-lookup"><span data-stu-id="fe607-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="fe607-125">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="fe607-125">System administrator</span></span></td>
<td><span data-ttu-id="fe607-126">KB 4017918 คือการอัพเดต X ++ หรือโปรแกรมแก้ไขด่วนแบบข้อมูลเมตาที่ประกอบด้วยพื้นที่ทำงานแบบเคลื่อนที่ของ <strong>การอนุมัติใบสั่งซื้อ</strong></span><span class="sxs-lookup"><span data-stu-id="fe607-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="fe607-127">เมื่อต้องการใช้ KB 4017918 ผู้ดูแลระบบต้องทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="fe607-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="fe607-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">ดาวน์โหลดโปรแกรมแก้ไขด่วนแบบข้อมูลเมตาจาก Microsoft Dynamics Lifecycle Services (LCS)</a></span><span class="sxs-lookup"><span data-stu-id="fe607-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="fe607-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">ติดตั้งโปรแกรมแก้ไขด่วนแบบข้อมูลเมตา</a></span><span class="sxs-lookup"><span data-stu-id="fe607-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="fe607-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">สร้างแพคเกจที่สามารถปรับใช้ได้</a> ที่ประกอบด้วยแบบจำลอง <strong>SCMMobile</strong> แล้วอัพโหลดแพคเกจที่สามารถปรับใช้ได้กับ LCS</span><span class="sxs-lookup"><span data-stu-id="fe607-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="fe607-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">ใช้แพคเกจที่สามารถปรับใช้ได้</a></span><span class="sxs-lookup"><span data-stu-id="fe607-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe607-132">เผยแพร่ <strong>พื้นที่ทำงานแบบเคลื่อนที่สำหรับการอนุมัติใบสั่งซื้อ</strong></span><span class="sxs-lookup"><span data-stu-id="fe607-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="fe607-133">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="fe607-133">System administrator</span></span></td>
<td><span data-ttu-id="fe607-134">ดู <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a></span><span class="sxs-lookup"><span data-stu-id="fe607-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="fe607-135">ดาวน์โหลดและติดตั้งแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="fe607-135">Download and install the mobile app</span></span>
<span data-ttu-id="fe607-136">ดาวน์โหลดและติดตั้งแอพบนมือถือ Microsoft Dynamics 365 for Unified Operations</span><span class="sxs-lookup"><span data-stu-id="fe607-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="fe607-137">สำหรับโทรศัพท์ Androids</span><span class="sxs-lookup"><span data-stu-id="fe607-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="fe607-138">สำหรับ iPhone</span><span class="sxs-lookup"><span data-stu-id="fe607-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="fe607-139">ล็อกอินเข้าสู่แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="fe607-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="fe607-140">เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="fe607-141">ป้อน URL ของ Microsoft Dynamics 365 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="fe607-142">ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="fe607-143">ป้อนข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-143">Enter your credentials.</span></span>
4. <span data-ttu-id="fe607-144">หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="fe607-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="fe607-145">หมายเหตุว่าถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="fe607-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![พื้นที่ทำงานการอนุมัติใบสั่งในรายการของพื้นที่ทำงานที่พร้อมใช้งาน](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="fe607-147">ดูใบสั่งที่กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="fe607-148">บนอุปกรณ์เคลื่อนที่ ให้เลือกพื้นที่ทำงาน **การอนุมัติใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="fe607-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="fe607-149">เลือก **ใบสั่งซื้อที่กำหนดให้กับฉัน** เพื่อดูใบสั่งซื้อทั้งหมดที่คุณได้รับการร้องขอให้ดำเนินการในลำดับงานการอนุมัติใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fe607-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="fe607-150">เลือกใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fe607-150">Select an order.</span></span> <span data-ttu-id="fe607-151">ในหน้า **รายละเอียดใบสั่ง** คุณจะเห็นข้อมูลส่วนหัวของใบสั่งและรายการ</span><span class="sxs-lookup"><span data-stu-id="fe607-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="fe607-152">คุณยังสามารถค้นหาคำแนะนำจากงานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="fe607-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="fe607-153">เลือก **การกระจายการลงบัญชี** เพื่อเปิดหน้า **ส่วนหัวของกระจายการลงบัญชี**</span><span class="sxs-lookup"><span data-stu-id="fe607-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="fe607-154">กลับไปยังหน้า **รายละเอียดใบสั่ง** และเลือกรายการ</span><span class="sxs-lookup"><span data-stu-id="fe607-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="fe607-155">จากรายละเอียดรายการใบสั่ง คุณสามารถสำรวจการกระจายการลงบัญชีเฉพาะรายการได้</span><span class="sxs-lookup"><span data-stu-id="fe607-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="fe607-156">ดำเนินการในใบสั่งซื้อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fe607-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="fe607-157">หลังจากที่คุณได้ดูรายการใบสั่งซื้อที่กำหนดให้กับคุณ และอ่านคำแนะนำลำดับงาน คุณควรพร้อมที่จะดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="fe607-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="fe607-158">บนอุปกรณ์เคลื่อนที่ ให้เลือกพื้นที่ทำงาน **การอนุมัติใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="fe607-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="fe607-159">เลือก **ใบสั่งซื้อที่กำหนดให้กับฉัน** เพื่อดูใบสั่งซื้อทั้งหมดที่คุณได้รับการร้องขอให้ดำเนินการในลำดับงานการอนุมัติใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fe607-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="fe607-160">เลือกใบสั่ง และดูหน้ารายละเอียด</span><span class="sxs-lookup"><span data-stu-id="fe607-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="fe607-161">เลือก **การดำเนินการ** เพื่อแสดงการดำเนินการที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fe607-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="fe607-162">การดำเนินการที่พร้อมใช้งานขึ้นอยู่กับงานที่ได้กำหนดให้กับคุณ</span><span class="sxs-lookup"><span data-stu-id="fe607-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="fe607-163">การดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="fe607-163">Task action</span></span>    | <span data-ttu-id="fe607-164">การดำเนินการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fe607-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="fe607-165">เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fe607-165">Complete</span></span>       | <span data-ttu-id="fe607-166">อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="fe607-166">Approve</span></span>          |
    | <span data-ttu-id="fe607-167">การส่งคืน</span><span class="sxs-lookup"><span data-stu-id="fe607-167">Return</span></span>         | <span data-ttu-id="fe607-168">ปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="fe607-168">Reject</span></span>           |
    | <span data-ttu-id="fe607-169">ร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="fe607-169">Request change</span></span> | <span data-ttu-id="fe607-170">ร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="fe607-170">Request change</span></span>   |
    | <span data-ttu-id="fe607-171">มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="fe607-171">Delegate</span></span>       | <span data-ttu-id="fe607-172">มอบหมาย</span><span class="sxs-lookup"><span data-stu-id="fe607-172">Delegate</span></span>         |

5. <span data-ttu-id="fe607-173">เลือกการดำเนินการที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fe607-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="fe607-174">ในหน้า **งานที่เสร็จสมบูรณ์** ให้ป้อนข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="fe607-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="fe607-175">โปรดจำไว้ว่า ถ้าคุณเลือกการดำเนินการ **การมอบหมาย** คุณต้องเลือกผู้ใช้ที่จะมอบหมายงานให้</span><span class="sxs-lookup"><span data-stu-id="fe607-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="fe607-176">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="fe607-176">Select **Done**.</span></span> <span data-ttu-id="fe607-177">หลังจากที่คุณรีเฟรชพื้นที่ทำงานของคุณ ใบสั่งซื้อจะไม่อยู่ในรายการของคุณอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="fe607-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

