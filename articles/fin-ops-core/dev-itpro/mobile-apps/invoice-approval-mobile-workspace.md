---
title: พื้นที่ทำงานการอนุมัติใบแจ้งหนี้แบบเคลื่อนที่
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานของการอนุมัติใบแจ้งหนี้แบบเคลื่อนที่
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a7aa1a03791b8ccb7050389097d1272f5930a49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127580"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="b1969-103">พื้นที่ทำงานการอนุมัติใบแจ้งหนี้แบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b1969-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1969-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับพื้นที่ทำงานของ **การอนุมัติใบแจ้งหนี้** แบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b1969-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="b1969-105">พื้นที่ทำงานนี้แสดงรายการของใบแจ้งหนี้ที่มีการกำหนดให้กับคุณผ่านขั้นตอนลำดับงานส่วนหัวของใบแจ้งหนี้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b1969-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="b1969-106">พื้นที่ทำงานแบบเคลื่อนที่นี้มีจุดมุ่งหมายเพื่อใช้กับแอปสำหรับอุปกรณ์เคลื่อนที่ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1969-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="b1969-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b1969-107">Overview</span></span>

<span data-ttu-id="b1969-108">พื้นที่ทำงาน **การอนุมัติใบแจ้งหนี้** แบบเคลื่อนที่ช่วยให้เสมียนและผู้จัดการของบัญชีเจ้าหนี้ สามารถดูใบแจ้งหนี้ที่มีการกำหนดให้เป็นส่วนหนึ่งของกระบวนการลำดับงานส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b1969-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="b1969-109">คุณสามารถดูใบแจ้งหนี้ ข้อมูล และรายละเอียดรายการและการกระจาย เพื่อช่วยให้คุณทำการตัดสินใจแจ้งการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="b1969-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="b1969-110">จากพื้นที่ทำงาน คุณสามารถดำเนินการย้ายใบแจ้งหนี้โดยใช้กระบวนการลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="b1969-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b1969-111">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b1969-111">Prerequisites</span></span>

<span data-ttu-id="b1969-112">ก่อนที่คุณจะสามารถใช้พื้นที่ทำงานนี้ ต้องเป็นไปตามข้อกำหนดเบื้องต้นต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b1969-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b1969-113">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b1969-113">Prerequisite</span></span></th>
<th><span data-ttu-id="b1969-114">บทบาท</span><span class="sxs-lookup"><span data-stu-id="b1969-114">Role</span></span></th>
<th><span data-ttu-id="b1969-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b1969-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b1969-116">Microsoft Dynamics 365 Finance ต้องถูกปรับใช้ในองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="b1969-117">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="b1969-117">System administrator</span></span></td>
<td><span data-ttu-id="b1969-118">ให้ดูที่ <a href="../deployment/deploy-demo-environment.md">ปรับใช้สภาพแวดล้อมสาธิต</a></span><span class="sxs-lookup"><span data-stu-id="b1969-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1969-119">ต้องมีการเผยแพร่พื้นที่ทำงานแบบเคลื่อนที่ของ <strong>ไดเรกทอรีของใบแจ้งหนี้</strong></span><span class="sxs-lookup"><span data-stu-id="b1969-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="b1969-120">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="b1969-120">System administrator</span></span></td>
<td><span data-ttu-id="b1969-121">ดู <a href="publish-mobile-workspace.md">เผยแพร่พื้นที่ทำงานแบบเคลื่อนที่</a></span><span class="sxs-lookup"><span data-stu-id="b1969-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="b1969-122">ดาวน์โหลดและติดตั้งแอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="b1969-122">Download and install the mobile app</span></span>

<span data-ttu-id="b1969-123">ดาวน์โหลดและติดตั้งแอปบนมือถือ Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b1969-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="b1969-124">สำหรับโทรศัพท์ Android</span><span class="sxs-lookup"><span data-stu-id="b1969-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="b1969-125">สำหรับ iPhone</span><span class="sxs-lookup"><span data-stu-id="b1969-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="b1969-126">ล็อกอินเข้าสู่แอพบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="b1969-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="b1969-127">เริ่มการทำงานแอพบนอุปกรณ์เคลื่อนที่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="b1969-128">ใส่ URL Microsoft Dynamics 365 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="b1969-129">ในครั้งแรกที่คุณเข้าสู่ระบบ ระบบจะขอให้คุณป้อนชื่อผู้ใช้และรหัสผ่านของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="b1969-130">ป้อนข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="b1969-131">หลังจากที่คุณลงชื่อเข้าใช้แล้ว พื้นที่ทำงานที่พร้อมใช้งานสำหรับบริษัทของคุณจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="b1969-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="b1969-132">หมายเหตุว่าถ้าผู้ดูแลระบบของคุณเผยแพร่พื้นที่ทำงานใหม่ในภายหลัง คุณจะต้องรีเฟรชรายการของพื้นที่ทำงานแบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b1969-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="b1969-133">[![ดึงเพื่อรีเฟรช](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="b1969-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="b1969-134">อนุมัติใบแจ้งหนี้โดยการใช้พื้นที่ทำงานการอนุมัติใบแจ้งหนี้แบบเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="b1969-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="b1969-135">บนอุปกรณ์เคลื่อนที่ ให้เลือกพื้นที่ทำงาน **การอนุมัติใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="b1969-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="b1969-136">เลือกใบแจ้งหนี้ที่มีการกำหนดกระบวนลำดับงานส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่ายให้แก่คุณ</span><span class="sxs-lookup"><span data-stu-id="b1969-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="b1969-137">ในหน้า **รายละเอียกของใบแจ้งหนี้** ให้ตรวจทานข้อมูลส่วนหัวของใบแจ้งหนี้ เช่น ข้อมูลของผู้จัดจำหน่ายและวันที่</span><span class="sxs-lookup"><span data-stu-id="b1969-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="b1969-138">เลือกรายการในใบแจ้งหนี้เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับใบแจ้งหนี้ในมุมมอง **รายละเอียดของรายการในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="b1969-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="b1969-139">ในมุมมอง **รายละเอียดของรายการในใบแจ้งหนี้** เลือก **การกระจาย** เพื่อแสดงการกระจายรายการ</span><span class="sxs-lookup"><span data-stu-id="b1969-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="b1969-140">คุณสามารถดูการลงบัญชีสำหรับรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b1969-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="b1969-141">ข้อมูลที่จะแสดงประกอบด้วยมิติทางการเงินและบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="b1969-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="b1969-142">ในหน้า **รายละเอียดในใบแจ้งหนี้** เลือก **การกระจาย** เพื่อแสดงการกระจายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b1969-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="b1969-143">คุณสามารถดูการลงบัญชีสำหรับรายการใบแจ้งหนี้สำหรับใบแจ้งหนี้ทั้งฉบับ</span><span class="sxs-lookup"><span data-stu-id="b1969-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="b1969-144">ข้อมูลที่จะแสดงประกอบด้วยมิติทางการเงินและบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="b1969-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="b1969-145">เลือก **สิ่งที่แนบ** เพื่อดูบันทึกหรือไฟล์ใดๆ ที่แนบไปกับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b1969-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="b1969-146">ในหน้า **รายละเอียกใบแจ้งหนี้** เลือกการดำเนินการลำดับงานที่เหมาะสม เพื่อดำเนินการกระบวนการตรวจทานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1969-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="b1969-147">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="b1969-147">Select **Done**.</span></span>
