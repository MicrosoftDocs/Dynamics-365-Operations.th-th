---
title: โฮมเพจแอพบนมือถือ
description: หัวข้อนี้อธิบายถึงแอป Finance and Operations สำหรับอุปกรณ์เคลื่อนที่และแสดงลิงค์ไปยังทรัพยากรที่สามารถช่วยให้คุณปรับใช้งานในองค์กรของคุณ
author: sericks007
manager: AnnBe
ms.date: 11/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: aaff4e3b3bfb079e183a12a5a85e452eed6df51d
ms.sourcegitcommit: e30ced8f136ef23017d2d8215a756236e42eec25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853943"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="70cdb-103">โฮมเพจแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="70cdb-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70cdb-104">หัวข้อนี้อธิบายถึงแอป Finance and Operations สำหรับอุปกรณ์เคลื่อนที่และแสดงลิงค์ไปยังทรัพยากรที่สามารถช่วยให้คุณปรับใช้งานในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="70cdb-104">This topic describes the Finance and Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="70cdb-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="70cdb-105">Overview</span></span>
--------

<span data-ttu-id="70cdb-106">แอพบนมือถือช่วยให้องค์กรของคุณสามารถทำให้กระบวนการทางธุรกิจพร้อมใช้งานบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="70cdb-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="70cdb-107">หลังจากที่ผู้ดูแลระบบไอทีของคุณเปิดใช้งานพื้นที่ทำงานแบบเคลื่อนที่สำหรับองค์กรของคุณแล้ว ผู้ใช้สามารถเข้าสู่ในแอพลิเคชันและเริ่มต้นรันกระบวนการทางธุรกิจจากอุปกรณ์เคลื่อนที่ของตนได้ทันที</span><span class="sxs-lookup"><span data-stu-id="70cdb-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="70cdb-108">แอพบนมือถือมีคุณลักษณะซึ่งจะช่วยให้เพิ่มประสิทธิภาพได้ ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="70cdb-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="70cdb-109">ผู้ใช้สามารถดู แก้ไข และดำเนินการกับข้อมูลทางธุรกิจ แม้ว่าจะมีการเชื่อมต่อเครือข่ายเป็นช่วง ๆ หรืออุปกรณ์เคลื่อนที่ทำงานแบบออฟไลน์โดยสิ้นเชิงก็ตาม</span><span class="sxs-lookup"><span data-stu-id="70cdb-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="70cdb-110">เมื่ออุปกรณ์สร้างการเชื่อมต่อเครือข่ายใหม่ การดำเนินงานข้อมูลแบบออฟไลน์จะซิงโครไนส์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="70cdb-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="70cdb-111">ผู้ดูแลระบบไอทีหรือนักพัฒนาสามารถสร้างและเผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ที่ได้รับการออกแบบมาเพื่อองค์กรของตน</span><span class="sxs-lookup"><span data-stu-id="70cdb-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="70cdb-112">แอพลิเคชันใช้สินทรัพย์ของรหัสที่มีอยู่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="70cdb-112">The app uses your existing code assets.</span></span> <span data-ttu-id="70cdb-113">ดังนั้น คุณไม่จำเป็นต้องนำกระบวนการตรวจสอบ ตรรกะทางธุรกิจ หรือการตั้งค่าคอนฟิกความปลอดภัยของคุณไปใช้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="70cdb-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="70cdb-114">ผู้ดูแลระบบไอทีหรือนักพัฒนาสามารถออกแบบพื้นที่ทำงานแบบเคลื่อนที่ได้อย่างง่ายดายโดยใช้โปรแกรมพื้นที่ทำงานแบบชี้และคลิกซึ่งรวมอยู่ในเว็บไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="70cdb-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="70cdb-115">ผู้ดูแลระบบไอทีหรือนักพัฒนาสามารถเลือกที่จะเพิ่มประสิทธิภาพความสามารถของพื้นที่ทำงานแบบออฟไลน์ได้โดยใช้กรอบงานความสามารถในการขยายตรรกะทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="70cdb-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="70cdb-116">เนื่องจากข้อมูลจะยังคงถูกประมวลผลในขณะที่อุปกรณ์อยู่ในโหมดออฟไลน์ สถานการณ์จำลองการเคลื่อนที่ของคุณจะยังคงหลากหลายและเป็นของเหลว แม้ว่าอุปกรณ์จะไม่ได้เชื่อมต่อเครือข่ายอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="70cdb-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="70cdb-117">องค์ประกอบของแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="70cdb-117">Elements of the mobile app</span></span>
<span data-ttu-id="70cdb-118">การนำทางในแอพบนมือถือประกอบด้วยแนวคิดพื้นฐานสี่อย่าง: แดชบอร์ด พื้นที่ทำงาน หน้า และการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="70cdb-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="70cdb-119">[![แนวคิดการนำทางในแอพบนมือถือ](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="70cdb-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="70cdb-120">เมื่อคุณเริ่มต้นแอพ ให้ไปที่ **แดชบอร์ด**</span><span class="sxs-lookup"><span data-stu-id="70cdb-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="70cdb-121">บนแดชบอร์ด คุณสามารถดูรายการของ **พื้นที่ทำงาน** ที่ถูกเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="70cdb-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="70cdb-122">ในแต่ละพื้นที่ทำงาน คุณสามารถดูรายการของ **หน้า** ที่พร้อมใช้งานสำหรับพื้นที่ทำงานนั้นได้</span><span class="sxs-lookup"><span data-stu-id="70cdb-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="70cdb-123">หลังจากที่คุณอยู่ในหน้าที่ คุณสามารถทำการดำเนินการหลายอย่าง</span><span class="sxs-lookup"><span data-stu-id="70cdb-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="70cdb-124">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="70cdb-124">Here are some examples:</span></span>

    - <span data-ttu-id="70cdb-125">ดูข้อมูลรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="70cdb-125">View detailed data.</span></span>
    - <span data-ttu-id="70cdb-126">นำทางไปยังหน้าอื่นสำหรับข้อมูลที่เกี่ยวข้อง เช่น รายละเอียดเอนทิตี้หรือรายการ</span><span class="sxs-lookup"><span data-stu-id="70cdb-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="70cdb-127">ดูรายการของ **การดำเนินการ** ที่พร้อมใช้งานสำหรับหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="70cdb-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="70cdb-128">การดำเนินการช่วยให้คุณสามารถสร้างหรือแก้ไขข้อมูลที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="70cdb-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="70cdb-129">กระบวนการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="70cdb-129">Implementation process</span></span>
<span data-ttu-id="70cdb-130">แผนภาพต่อไปนี้แสดงกระบวนการปฏิบัติตามพื้นที่ทำงานแบบเคลื่อนที่ทั้งสองที่ซึ่งจัดเตรียมให้โดย Microsoft และพื้นที่ทำงานแบบเคลื่อนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="70cdb-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="70cdb-131">[![กระบวนการใช้งานแอพบนมือถือ](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="70cdb-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="70cdb-132">ตารางต่อไปนี้มีการเชื่อมโยงกับทรัพยากรซึ่งช่วยให้คุณสามารถใช้พื้นที่ทำงานแบบเคลื่อนที่ทั้งสองที่ซึ่งจัดเตรียมไว้โดย Microsoft และพื้นที่ทำงานแบบเคลื่อนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="70cdb-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="70cdb-133">ตัวเลขในคอลัมน์แรกตรงกับขั้นตอนที่ระบุหมายเลขในภาพประกอบก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="70cdb-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70cdb-134">ขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="70cdb-134">Step</span></span></th>
<th><span data-ttu-id="70cdb-135">บทบาท</span><span class="sxs-lookup"><span data-stu-id="70cdb-135">Role</span></span></th>
<th><span data-ttu-id="70cdb-136">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="70cdb-136">Action</span></span></th>
<th><span data-ttu-id="70cdb-137">ทรัพยากรที่จะช่วยให้คุณทำการดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="70cdb-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70cdb-138">1</span><span class="sxs-lookup"><span data-stu-id="70cdb-138">1</span></span></td>
<td><span data-ttu-id="70cdb-139">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-139">System administrator</span></span></td>
<td><span data-ttu-id="70cdb-140">นำแอพ Finance and Operations ไปปรับใช้ในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="70cdb-140">Implement Finance and Operations apps in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="70cdb-141">ถ้าคุณยังไม่ได้ปรับใช้รุ่นของ Microsoft Dynamics 365 ให้ดูที่ <a href="../deployment/deploy-demo-environment.md">ปรับใช้สภาพแวดล้อมสาธิต</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="70cdb-142">เมื่อต้องการดูรายการพื้นที่ทำงานแบบเคลื่อนที่ที่สามารถใช้ได้ ให้ดูที่ <a href="mobile-workspaces-released.md">พื้นที่ทำงานแบบเคลื่อนที่ที่นำออกใช้เมื่อเร็ว ๆ นี้</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cdb-143">2</span><span class="sxs-lookup"><span data-stu-id="70cdb-143">2</span></span></td>
<td><span data-ttu-id="70cdb-144">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-144">System administrator</span></span></td>
<td><span data-ttu-id="70cdb-145"><strong>ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Operations รุ่น 1611:</strong> ดาวน์โหลด และติดตั้ง KB ที่เปิดใช้งานพื้นที่ทำงานแบบเคลื่อนที่ที่สามารถใช้ได้บน Microsoft</span><span class="sxs-lookup"><span data-stu-id="70cdb-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="70cdb-146">ให้ดูที่หัวข้อต่อไปนี้ สำหรับข้อมูลเพิ่มเติม:</span><span class="sxs-lookup"><span data-stu-id="70cdb-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="70cdb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่การควบคุมต้นทุน</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="70cdb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่ของปริมาณคงคลังคงเหลือ</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="70cdb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่ใบสั่งขาย</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="70cdb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่ของการทำงานร่วมกันกับผู้จัดจำหน่าย</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="70cdb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่สำหรับการป้อนข้อมูลเวลาโครงการ</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="70cdb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">พื้นที่ทำงานแบบเคลื่อนที่สำหรับการจัดการค่าใช้จ่าย</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cdb-153">3</span><span class="sxs-lookup"><span data-stu-id="70cdb-153">3</span></span></td>
<td><span data-ttu-id="70cdb-154">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-154">System administrator</span></span></td>
<td><span data-ttu-id="70cdb-155">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ที่สามารถใช้ได้บน Microsoft</span><span class="sxs-lookup"><span data-stu-id="70cdb-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="70cdb-156"><a href="publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a>
</span><span class="sxs-lookup"><span data-stu-id="70cdb-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cdb-157">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70cdb-157">4</span></span></td>
<td><span data-ttu-id="70cdb-158">นักพัฒนาหรือผู้ขายซอฟต์แวร์อิสระ (ISV)</span><span class="sxs-lookup"><span data-stu-id="70cdb-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="70cdb-159">ใช้แพลตฟอร์มเคลื่อนที่เพื่อสร้างพื้นที่ทำงานแบบเคลื่อนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="70cdb-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="70cdb-160"><a href="platform/mobile-platform-home-page.md">แพลตฟอร์มเคลื่อนที่</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cdb-161">5</span><span class="sxs-lookup"><span data-stu-id="70cdb-161">5</span></span></td>
<td><span data-ttu-id="70cdb-162">ISV</span><span class="sxs-lookup"><span data-stu-id="70cdb-162">ISV</span></span></td>
<td><span data-ttu-id="70cdb-163">สร้างแพคเกจที่สามารถปรับใช้ได้ที่ประกอบด้วยพื้นที่ทำงานแบบเคลื่อนที่ที่กำหนดเอง และอัพโหลดแพคเกจไปยัง Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="70cdb-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="70cdb-164"><a href="../deployment/create-apply-deployable-package.md">สร้างแพคเกจที่สามารถปรับใช้ได้</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cdb-165">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="70cdb-165">6</span></span></td>
<td><span data-ttu-id="70cdb-166">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-166">System administrator</span></span></td>
<td><span data-ttu-id="70cdb-167">ใช้แพคเกจที่สามารถปรับใช้ได้ที่ประกอบด้วยพื้นที่ทำงานที่กำหนดโดยผู้ขายซอฟต์แวร์อิสระ (ISV)</span><span class="sxs-lookup"><span data-stu-id="70cdb-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="70cdb-168"><a href="../deployment/apply-deployable-package-system.md">ใช้แพคเกจที่สามารถปรับใช้ได้</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cdb-169">7</span><span class="sxs-lookup"><span data-stu-id="70cdb-169">7</span></span></td>
<td><span data-ttu-id="70cdb-170">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-170">System administrator</span></span></td>
<td><span data-ttu-id="70cdb-171">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ที่กำหนดเองที่สามารถใช้ได้บน ISV</span><span class="sxs-lookup"><span data-stu-id="70cdb-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="70cdb-172"><a href="publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70cdb-173">8</span><span class="sxs-lookup"><span data-stu-id="70cdb-173">8</span></span></td>
<td><span data-ttu-id="70cdb-174">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="70cdb-174">User</span></span></td>
<td><span data-ttu-id="70cdb-175">ดาวน์โหลดและติดตั้งแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="70cdb-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="70cdb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">แอป Finance and Operations สำหรับ Android</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="70cdb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">แอป Finance and Operations สำหรับ iOS</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="70cdb-178">(Windows Phone ที่ไม่สนับสนุน)</span><span class="sxs-lookup"><span data-stu-id="70cdb-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70cdb-179">9</span><span class="sxs-lookup"><span data-stu-id="70cdb-179">9</span></span></td>
<td><span data-ttu-id="70cdb-180">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="70cdb-180">User</span></span></td>
<td><span data-ttu-id="70cdb-181">ล็อกอิน และใช้แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="70cdb-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="70cdb-182">แอพมีพื้นที่ทำงานแบบเคลื่อนที่ที่เผยแพร่โดยผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="70cdb-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="70cdb-183">เมื่อต้องการดูรายการพื้นที่ทำงานแบบเคลื่อนที่ที่สามารถใช้ได้ที่จัดเตรียมไว้โดย Microsoft ให้ดูที่ <a href="mobile-workspaces-released.md">พื้นที่ทำงานแบบเคลื่อนที่ที่นำออกใช้เมื่อเร็ว ๆ นี้</a></span><span class="sxs-lookup"><span data-stu-id="70cdb-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="70cdb-184">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="70cdb-184">Troubleshooting</span></span>
[<span data-ttu-id="70cdb-185">ทรัพยากรแพลตฟอร์มเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="70cdb-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
