---
title: "พื้นที่ทำงานการเคลื่อนคงเหลือของสินค้าคงคลัง"
description: "หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานแบบเคลื่อนที่ของปริมาณคงคลังคงเหลือ พื้นที่ทำงานนี้ช่วยให้คุณได้รับข้อมูลเชิงลึกเคลื่อนที่ในสินค้าคงคลังที่จองไว้และพร้อมใช้งานได้ตลอดเวลา และที่ใดก็ได้"
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 6e062ffa459b7d008fc5d24f27538f8df04d7e82
ms.contentlocale: th-th
ms.lasthandoff: 08/10/2017

---

# <a name="inventory-on-hand-mobile-workspace"></a><span data-ttu-id="31ebb-104">พื้นที่ทำงานการเคลื่อนคงเหลือของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="31ebb-104">Inventory on-hand mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31ebb-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานแบบเคลื่อนที่ของ **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="31ebb-105">This topic provides information about the **Inventory on-hand** mobile workspace.</span></span> <span data-ttu-id="31ebb-106">พื้นที่ทำงานนี้ช่วยให้คุณได้รับข้อมูลเชิงลึกในสินค้าคงคลังที่จองไว้และพร้อมใช้งานได้ตลอดเวลา และที่ใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="31ebb-106">This workspace helps you gain insights into reserved and available inventory anytime and anywhere.</span></span>

<span data-ttu-id="31ebb-107">พื้นที่ทำงานนี้จัดทำขึ้นสำหรับใช้กับแอพบนมือถือ Microsoft Dynamics 365 for Unified Operations</span><span class="sxs-lookup"><span data-stu-id="31ebb-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="31ebb-108">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="31ebb-108">Overview</span></span>
<span data-ttu-id="31ebb-109">โดยทั่วไป บริษัทจะมีการจัดส่งและการรับสินค้าคงคลังหลายครั้งทุกวัน</span><span class="sxs-lookup"><span data-stu-id="31ebb-109">Typically, companies have multiple shipments and multiple receipts of inventory every day.</span></span> <span data-ttu-id="31ebb-110">ความเคลื่อนไหวเหล่านี้จะเปลี่ยนสถานะปริมาณคงคลังคงเหลืออย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="31ebb-110">These movements constantly change the on-hand inventory status.</span></span> <span data-ttu-id="31ebb-111">พื้นที่ทำงานแบบเคลื่อนที่ของ **ปริมาณคงคลังคงเหลือ** ช่วยให้คุณเห็นสถานะปริมาณคงคลังคงเหลือระหว่างบริษัท เพื่อที่คุณจะได้รับข้อมูลเชิงลึกล่าสุดในข้อมูลสินค้าคงคลังบนอุปกรณ์เคลื่อนที่ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="31ebb-111">The **Inventory on-hand** mobile workspace lets you see the cross-company on-hand inventory status, so that you can gain the latest insights into inventory data on the mobile device of your choice.</span></span> <span data-ttu-id="31ebb-112">โดยไม่คำนึงถึงว่าคุณทำงานในคลังสินค้า การซื้อ การขาย การผลิต หรือการจัดการ หรือมีบทบาทอื่น คุณสามารถเข้าถึงข้อมูลปริมาณคงคลังคงเหลือได้ทุกเมื่อใด และที่ใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="31ebb-112">Regardless of whether you work in the warehouse, purchasing, sales, manufacturing, or management, or have other roles, you can access on-hand inventory data anytime and anywhere.</span></span> 

<span data-ttu-id="31ebb-113">พื้นที่ทำงานแบบเคลื่อนที่แสดงมุมมองฉับพลันของสถานะคงคลังคงเหลือของสิ่งอำนวยความสะดวกต่างๆ</span><span class="sxs-lookup"><span data-stu-id="31ebb-113">The mobile workspace provides an instant view of the on-hand status across facilities.</span></span> <span data-ttu-id="31ebb-114">ซึ่งช่วยให้คุณสามารถดูปริมาณสินค้าคงคลังคงเหลือของสิ่งอำนวยความสะดวกต่างๆ การจองวัตถุดิบปัจจุบัน และปริมาณคงคลังคงเหลือที่ไม่ได้จอง</span><span class="sxs-lookup"><span data-stu-id="31ebb-114">It lets you view on-hand inventory across facilities, current material reservations, and unreserved on-hand inventory.</span></span> <span data-ttu-id="31ebb-115">นอกจากนี้คุณยังสามารถป้อนหมายเลขเพื่อสอบถามปริมาณคงคลังคงเหลือ และสามารถทำการค้นหาผลิตภัณฑ์คงคลังคงเหลือหรือตัวแปรที่ถูกกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="31ebb-115">You can also enter item numbers to query on-hand inventory, and can do a filtered search for on-hand products or variants.</span></span> 

<span data-ttu-id="31ebb-116">โดยเฉพาะอย่างยิ่ง พื้นที่ทำงานแบบเคลื่อนที่จะมีคุณลักษณะเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="31ebb-116">Specifically, the mobile workspace provides these features:</span></span>

-   <span data-ttu-id="31ebb-117">คุณสามารถค้นหาตามหมายเลขผลิตภัณฑ์หรือชื่อผลิตภัณฑ์เพื่อค้นหาผลิตภัณฑ์เพื่อดูสถานะสำหรับปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="31ebb-117">You can search by product number or product name to find products to view the on-hand inventory status for.</span></span>
-   <span data-ttu-id="31ebb-118">สำหรับผลิตภัณฑ์ที่เลือก คุณสามารถดูข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="31ebb-118">For the selected products, you can view the following information:</span></span>

    -   <span data-ttu-id="31ebb-119">ปริมาณคงคลังคงเหลือต่อไซต์</span><span class="sxs-lookup"><span data-stu-id="31ebb-119">On-hand inventory per site</span></span>
    -   <span data-ttu-id="31ebb-120">ปริมาณคงคลังคงเหลือต่อคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="31ebb-120">On-hand inventory per warehouse</span></span>
    -   <span data-ttu-id="31ebb-121">ปริมาณคงคลังคงเหลือต่อสถานที่</span><span class="sxs-lookup"><span data-stu-id="31ebb-121">On-hand inventory per location</span></span>
    -   <span data-ttu-id="31ebb-122">ปริมาณคงคลังคงเหลือต่อชุดงาน (สำหรับผลิตภัณฑ์ที่มีการควบคุมชุดงาน)</span><span class="sxs-lookup"><span data-stu-id="31ebb-122">On-hand inventory per batch (for batch-controlled products)</span></span>
    -   <span data-ttu-id="31ebb-123">ปริมาณคงคลังคงเหลือต่อสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="31ebb-123">On-hand inventory per inventory status</span></span>
    
-   <span data-ttu-id="31ebb-124">ปริมาณคงคลังคงเหลือของผลิตภัณฑ์จะแสดงอยู่ในวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="31ebb-124">Product on-hand inventory is shown in the following ways:</span></span>

    -   <span data-ttu-id="31ebb-125">ตามสินค้าคงคลังทางกายภาพ (มุมมองนี้แสดงยอดเงินรวม)</span><span class="sxs-lookup"><span data-stu-id="31ebb-125">By physical inventory (This view represents the total amount.)</span></span>
    -   <span data-ttu-id="31ebb-126">ตามสินค้าคงคลังที่จองไว้ (มุมมองนี้แสดงยอดเงินที่จองไว้)</span><span class="sxs-lookup"><span data-stu-id="31ebb-126">By physical reserved (This view represents the reserved amount.)</span></span>
    -   <span data-ttu-id="31ebb-127">ตามรายการที่มีอยู่จริง (มุมมองนี้แสดงถึงจำนวนที่ใช้ที่ไม่มีการจอง)</span><span class="sxs-lookup"><span data-stu-id="31ebb-127">By available physical (This view represents available amount that has no reservations.)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="31ebb-128">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="31ebb-128">Prerequisites</span></span>
<span data-ttu-id="31ebb-129">ข้อกำหนดเบื้องต้นที่แตกต่างกันขึ้นอยู่กับรุ่นของ Microsoft Dynamics 365 ที่นำไปใช้งานสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="31ebb-129">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="31ebb-130">ข้อกำหนดเบื้องต้นหากคุณใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition การอัพเดตของเดือนกรกฎาคม 2017</span><span class="sxs-lookup"><span data-stu-id="31ebb-130">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span> 
<span data-ttu-id="31ebb-131">ถ้า Microsoft Dynamics 365 for Finance and Operations, Enterprise edition การอัพเดพเดือนกรกฎาคม 2017 ถูกปรับใช้สำหรับองค์กรของคุณแล้ว ผู้ดูแลระบบต้องเผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="31ebb-131">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update has been deployed for your organization, the system administrator must publish the **Inventory on-hand** mobile workspace.</span></span> <span data-ttu-id="31ebb-132">สำหรับคำแนะนำ ให้ดูที่ [เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace)</span><span class="sxs-lookup"><span data-stu-id="31ebb-132">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="31ebb-133">ข้อกำหนดเบื้องต้นถ้าคุณใช้ Microsoft Dynamics 365 for Operations รุ่น 1611 ที่มีการอัพเดตแพลตฟอร์ม 3 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="31ebb-133">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="31ebb-134">ถ้ามีการปรับใช้ Microsoft Dynamics 365 for Operations รุ่น 1611 ที่มีการอัพเดตแพลตฟอร์ม 3 หรือรุ่นที่ใหม่กว่าสำหรับองค์กรของคุณ ผู้ดูแลระบบต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="31ebb-134">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="31ebb-135">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="31ebb-135">Prerequisite</span></span></th>
<th><span data-ttu-id="31ebb-136">บทบาท</span><span class="sxs-lookup"><span data-stu-id="31ebb-136">Role</span></span></th>
<th><span data-ttu-id="31ebb-137">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="31ebb-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="31ebb-138">การใช้ KB 4013633</span><span class="sxs-lookup"><span data-stu-id="31ebb-138">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="31ebb-139">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="31ebb-139">System administrator</span></span></td>

<td><span data-ttu-id="31ebb-140">KB 4013633 คือการอัพเดต X ++ หรือโปรแกรมแก้ไขด่วนแบบข้อมูลเมตาที่ประกอบด้วยพื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ปริมาณคงคลังคงเหลือ</strong></span><span class="sxs-lookup"><span data-stu-id="31ebb-140">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Inventory on-hand</strong> mobile workspace.</span></span> <span data-ttu-id="31ebb-141">เมื่อต้องการใช้ KB 4013633 ผู้ดูแลระบบต้องทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="31ebb-141">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="31ebb-142"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">ดาวน์โหลดโปรแกรมแก้ไขด่วนแบบข้อมูลเมตาจาก Microsoft Dynamics Lifecycle Services (LCS)</a></span><span class="sxs-lookup"><span data-stu-id="31ebb-142"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="31ebb-143"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">ติดตั้งโปรแกรมแก้ไขด่วนแบบข้อมูลเมตา</a></span><span class="sxs-lookup"><span data-stu-id="31ebb-143"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="31ebb-144"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">สร้างแพคเกจที่สามารถปรับใช้ได้</a> ที่ประกอบด้วยแบบจำลอง <strong>SCMMobile</strong> แล้วอัพโหลดแพคเกจที่สามารถปรับใช้ได้กับ LCS</span><span class="sxs-lookup"><span data-stu-id="31ebb-144"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="31ebb-145"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">ใช้แพคเกจที่สามารถปรับใช้ได้</a></span><span class="sxs-lookup"><span data-stu-id="31ebb-145"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="31ebb-146">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ปริมาณคงคลังคงเหลือ</strong></span><span class="sxs-lookup"><span data-stu-id="31ebb-146">Publish the <strong>Inventory on-hand</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="31ebb-147">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="31ebb-147">System administrator</span></span></td>
<td><span data-ttu-id="31ebb-148">ดู <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a></span><span class="sxs-lookup"><span data-stu-id="31ebb-148">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="31ebb-149">ดาวน์โหลดและติดตั้งแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="31ebb-149">Download and install the mobile app</span></span>

<span data-ttu-id="31ebb-150">ดาวน์โหลดและติดตั้งแอพบนมือถือ Dynamics 365 for Unified Operations</span><span class="sxs-lookup"><span data-stu-id="31ebb-150">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="31ebb-151">สำหรับโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="31ebb-151">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="31ebb-152">สำหรับ iPhone</span><span class="sxs-lookup"><span data-stu-id="31ebb-152">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="31ebb-153">ล็อกอินเข้าสู่แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="31ebb-153">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="31ebb-154">เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="31ebb-154">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="31ebb-155">ป้อน URL ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="31ebb-155">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="31ebb-156">ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="31ebb-156">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="31ebb-157">ป้อนข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="31ebb-157">Enter your credentials.</span></span>
4.  <span data-ttu-id="31ebb-158">หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="31ebb-158">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="31ebb-159">หมายเหตุว่าถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="31ebb-159">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="31ebb-160">[![ดึงเพื่อรีเฟรช](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="31ebb-160">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a><span data-ttu-id="31ebb-161">ดูปริมาณคงคลังคงเหลือสำหรับผลิตภัณฑ์โดยใช้พื้นที่ทำงานแบบเคลื่อนที่ของปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="31ebb-161">View the on-hand inventory for a product by using the Inventory on-hand mobile workspace</span></span>

1.  <span data-ttu-id="31ebb-162">บนอุปกรณ์เคลื่อนที่ เลือกพื้นที่ทำงาน **ปริมาณคงคลังคงเหลือ**</span><span class="sxs-lookup"><span data-stu-id="31ebb-162">On your mobile device, select the **Inventory on-hand** workspace.</span></span>

2.  <span data-ttu-id="31ebb-163">เลือก **ตรวจสอบปริมาณคงคลังคงเหลือสำหรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="31ebb-163">Select **Check on-hand for an item**.</span></span> <span data-ttu-id="31ebb-164">คุณเห็นรายการของผลิตภัณฑ์ที่ถูกโหลดลงในแอพของคุณสำหรับการใช้งานแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="31ebb-164">You see a list of the products that are loaded into your app for offline use.</span></span> <span data-ttu-id="31ebb-165">โดยค่าเริ่มต้น จะมีการโหลดไว้ 50 รายการ แต่นักพัฒนาสามารถเปลี่ยนแปลงจำนวนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="31ebb-165">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="31ebb-166">สำหรับข้อมูลเพิ่มเติม นักพัฒนาควรดูที่ [แพลตฟอร์มเคลื่อนที่](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page)</span><span class="sxs-lookup"><span data-stu-id="31ebb-166">For more information, developers should see [Mobile platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).</span></span>
3.  <span data-ttu-id="31ebb-167">ถ้าสินค้าของคุณไม่ได้อยู่ในรายการ เลือก **ค้นหาข้อมูลเพิ่มเติม**</span><span class="sxs-lookup"><span data-stu-id="31ebb-167">If your item isn't in the list, select **Search more**.</span></span> <span data-ttu-id="31ebb-168">ค้นหาโดยใช้หมายเลขผลิตภัณฑ์ หรือสลับไปยังการค้นหาตามชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="31ebb-168">Search by product number, or switch to a search by product name.</span></span>

4.  <span data-ttu-id="31ebb-169">เลือกผลิตภัณฑ์ > </span><span class="sxs-lookup"><span data-stu-id="31ebb-169">Select a product.</span></span> <span data-ttu-id="31ebb-170">ถ้าสินค้ามีรูปภาพ รูปภาพจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="31ebb-170">If the item has an image, the image is shown.</span></span>
5.  <span data-ttu-id="31ebb-171">เลือกหนึ่งในตัวเลือกต่อไปนี้เพื่อดูสถานะของปริมาณคงคลังคงเหลือ:</span><span class="sxs-lookup"><span data-stu-id="31ebb-171">Select one of the following options to view the status of on-hand inventory:</span></span>

    -   <span data-ttu-id="31ebb-172">ดูปริมาณคงคลังคงเหลือต่อไซต์</span><span class="sxs-lookup"><span data-stu-id="31ebb-172">View on-hand per site</span></span>
    -   <span data-ttu-id="31ebb-173">ดูปริมาณคงคลังคงเหลือต่อคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="31ebb-173">View on-hand per warehouse</span></span>
    -   <span data-ttu-id="31ebb-174">ดูปริมาณคงคลังคงเหลือต่อสถานที่</span><span class="sxs-lookup"><span data-stu-id="31ebb-174">View on-hand per location</span></span>
    -   <span data-ttu-id="31ebb-175">ดูปริมาณคงคลังคงเหลือต่อชุดงาน (สำหรับผลิตภัณฑ์ที่มีการควบคุมชุดงาน)</span><span class="sxs-lookup"><span data-stu-id="31ebb-175">View on-hand per batch (for batch-controlled products)</span></span>
    -   <span data-ttu-id="31ebb-176">ดูปริมาณคงคลังคงเหลือต่อสถานะสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="31ebb-176">View on-hand per inventory status</span></span>

    <span data-ttu-id="31ebb-177">ปริมาณคงคลังคงเหลือของผลิตภัณฑ์จะแสดงอยู่ในวิธีการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="31ebb-177">Product on-hand inventory is shown in the following ways:</span></span>
    -   <span data-ttu-id="31ebb-178">ตามสินค้าคงคลังทางกายภาพ (มุมมองนี้แสดงยอดเงินรวม)</span><span class="sxs-lookup"><span data-stu-id="31ebb-178">By physical inventory (This view represents the total amount.)</span></span>
    -   <span data-ttu-id="31ebb-179">ตามสินค้าคงคลังที่จองไว้ (มุมมองนี้แสดงยอดเงินที่จองไว้)</span><span class="sxs-lookup"><span data-stu-id="31ebb-179">By physical reserved (This view represents the reserved amount.)</span></span>
    -   <span data-ttu-id="31ebb-180">ตามรายการที่มีอยู่จริง (มุมมองนี้แสดงถึงจำนวนที่ใช้ที่ไม่มีการจอง)</span><span class="sxs-lookup"><span data-stu-id="31ebb-180">By available physical (This view represents the available amount that has no reservations.)</span></span>

