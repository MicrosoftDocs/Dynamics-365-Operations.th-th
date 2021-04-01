---
title: ตั้งค่าลำดับงานการอนุมัติสัญญาเช่า
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าลำดับงานการอนุมัติที่จะรันเมื่อมีการสร้างสัญญาเช่าใหม่
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249592"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="16224-103">ตั้งค่าลำดับงานการอนุมัติสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="16224-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16224-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าลำดับงานการอนุมัติที่จะรันเมื่อมีการสร้างสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="16224-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="16224-105">สำหรับข้อมูลเกี่ยวกับวิธีการใช้ลำดับงาน ให้ดูที่ [ใช้ลำดับงานการอนุมัติสัญญาเช่า](use-create-lease-wrkflw.md)</span><span class="sxs-lookup"><span data-stu-id="16224-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="16224-106">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> ลำดับงานสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="16224-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="16224-107">ในหน้า **ลำดับงานสัญญาเช่า** เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="16224-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="16224-108">ในกล่องโต้ตอบที่ปรากฏขึ้น ภายใต้ **ชนิดลำดับงาน** ให้เลือกลิงค์ **ลำดับงานสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="16224-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="16224-109">เปิดแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="16224-109">The application is opened.</span></span> <span data-ttu-id="16224-110">หลังจากที่รันแล้ว ให้ลงชื่อเข้าใช้ Azure Active Directory (Azure AD) เพื่อถูกเปลี่ยนเส้นทางไปยังแอปพลิเคชันลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="16224-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="16224-111">ลากองค์ประกอบ **การอนุมัติลำดับงานสัญญาเช่า** ไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="16224-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="16224-112">เชื่อมต่อโหนดหนึ่งรายการตั้งแต่ **เริ่มต้น** จนถึง **การอนุมัติลำดับงานสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="16224-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="16224-113">เชื่อมต่อ **การอนุมัติลำดับงานสัญญาเช่า** จน **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="16224-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="16224-114">คลิกสองครั้งที่ **การอนุมัติลำดับงานสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="16224-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="16224-115">เลือก **คุณสมบัติ** จากนั้นภายใต้ **การตั้งค่าพื้นฐาน** ให้ป้อนชื่อสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="16224-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="16224-116">ในหน้านี้ คุณยังสามารถตั้งค่าพารามิเตอร์เพิ่มเติมสำหรับลำดับงานได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="16224-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="16224-117">ถ้าคุณเปิดใช้งาน **การดำเนินการอัตโนมัติ** ระบบจะดำเนินการที่ระบุโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="16224-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="16224-118">คุณสามารถส่งการแจ้งเตือนได้ถ้ามีการระบุไว้ในแท็บ **การแจ้งเตือน** บนแท็บ **การตั้งค่าขั้นสูง** คุณสามารถระบุผู้อนุมัติขั้นสุดท้าย ตั้งค่าขีดจำกัดเวลา และกำหนดการดำเนินการเฉพาะที่ต้องทำให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="16224-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="16224-119">เมื่อคุณตั้งค่าพารามิเตอร์ลำดับงานเสร็จเรียบร้อยแล้ว ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="16224-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="16224-120">เลือก **ขั้นตอนที่ 1** แล้วเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="16224-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="16224-121">ภายใต้ **การตั้งค่าพื้นฐาน** ให้ป้อนชื่อสำหรับขั้นตอน สร้างบรรทัดชื่อเรื่องสำหรับการอนุมัติ และระบุคำสั่งสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="16224-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="16224-122">บนหน้า **การกำหนด** ให้เลือกชนิดการกำหนด</span><span class="sxs-lookup"><span data-stu-id="16224-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="16224-123">เมื่อต้องการกำหนดผู้ใช้ที่เฉพาะเจาะจงให้กับการอนุมัติ ให้เลือก **ผู้ใช้** เลือกผู้ใช้ที่อนุมัติสัญญาเช่า แล้วเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="16224-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="16224-124">เลือก **บันทึกและปิด** เพื่อสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="16224-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="16224-125">เมื่อคุณได้รับพร้อมท์ ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="16224-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="16224-126">ในหน้า **สร้างลำดับงาน** เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="16224-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="16224-127">เลือกลำดับงานใหม่ แล้วจากนั้น เลือก **รุ่น**</span><span class="sxs-lookup"><span data-stu-id="16224-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="16224-128">เลือก **ทำให้ใช้งาน** เพื่อให้แน่ใจว่าลำดับงานเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="16224-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="16224-129">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="16224-129">Select **Close**.</span></span> <span data-ttu-id="16224-130">รุ่นที่ใช้งานอยู่ใหม่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="16224-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]