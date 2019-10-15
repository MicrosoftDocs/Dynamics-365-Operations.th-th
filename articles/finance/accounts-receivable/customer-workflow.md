---
title: ลำดับงานของลูกค้า
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับลำดับงานของลูกค้า คุณจะเปลี่ยนฟิลด์เฉพาะสำหรับลูกค้าแล้วส่งการเปลี่ยนแปลงเหล่านั้นเพื่อขอการอนุมัติโดยใช้ลำดับงานก่อนที่จะมีการเพิ่มไปยังลูกค้า
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8ff91a1df82d6195da266b97c347ef27afec662d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176113"
---
# <a name="customer-workflow"></a><span data-ttu-id="e2382-104">ลำดับงานของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e2382-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2382-105">ลำดับงานของลูกค้าได้รับการเพิ่มลงในรุ่น 8.0.4 แล้ว</span><span class="sxs-lookup"><span data-stu-id="e2382-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="e2382-106">คุณสามารถเปลี่ยนฟิลด์เฉพาะสำหรับลูกค้าแล้วส่งการเปลี่ยนแปลงเหล่านั้นเพื่อขอการอนุมัติโดยใช้ลำดับงานก่อนที่จะมีการเพิ่มไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e2382-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="e2382-107">ตั้งค่าลำดับงานของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e2382-107">Set up the customer workflow</span></span>

<span data-ttu-id="e2382-108">คุณต้องเปิดใช้งานลำดับงานของลูกค้าก่อนจึงจะสามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="e2382-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="e2382-109">ไปที่ **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="e2382-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="e2382-110">บนแท็บ **ทั่วไป** บนแท็บด่วน **การอนุมัติของลูกค้า** ตั้งค่าตัวเลือก **เปิดใช้งานการอนุมัติของลูกค้า** เป็น **ใช่** เพื่อเปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="e2382-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="e2382-111">ในฟิลด์ **ลักษณะการทำงานของเอนทิตี้ข้อมูล** ให้เลือกลักษณะการทำงานที่เอนทิตี้ข้อมูลควรใช้เมื่อมีการนำเข้าข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="e2382-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="e2382-112">**อนุญาตการเปลี่ยนแปลงโดยไม่ต้องมีการอนุมัติ** – เอนทิตี้สามารถอัปเดตเรกคอร์ดลูกค้าได้โดยไม่ต้องดำเนินการผ่านลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="e2382-113">**ปฏิเสธการเปลี่ยนแปลง** – ไม่สามารถทำการเปลี่ยนแปลงกับเรกคอร์ดลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e2382-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="e2382-114">การนำเข้าจะล้มเหลวในฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="e2382-115">**สร้างข้อเสนอการเปลี่ยนแปลง** – ฟิลด์ทั้งหมดจะมีการเปลี่ยนแปลงยกเว้นฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="e2382-116">ค่าใหม่สำหรับฟิลด์เหล่านั้นจะมีการเพิ่มไปยังลูกค้าเป็นการเปลี่ยนแปลงที่นำเสนอ และลำดับงานจะเริ่มต้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e2382-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="e2382-117">ในรายการของฟิลด์ลูกค้า ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** สำหรับทุกฟิลด์ที่ต้องได้รับการอนุมัติก่อนที่จะทำการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="e2382-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="e2382-118">ไปที่ **บัญชีลูกหนี้ \> การตั้งค่า \> ลำดับงานบัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="e2382-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="e2382-119">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e2382-119">Select **New**.</span></span>
7. <span data-ttu-id="e2382-120">เลือก **ลำดับงานการเปลี่ยนแปลงที่นำเสนอของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="e2382-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="e2382-121">ตั้งค่าลำดับงานเพื่อให้ตรงกันกับกระบวนการอนุมัติของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2382-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="e2382-122">องค์ประกอบการอนุมัติลำดับงาน **การอนุมัติลำดับงานสำหรับการเปลี่ยนแปลงที่นำเสนอของลูกค้า** จะใช้การเปลี่ยนแปลงกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e2382-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="e2382-123">เปลี่ยนแปลงข้อมูลลูกค้าและส่งการเปลี่ยนแปลงไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="e2382-124">เมื่อคุณเปลี่ยนแปลงฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน หน้า **การเปลี่ยนแปลงที่นำเสนอ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e2382-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="e2382-125">หน้านี้จะแสดงค่าเดิมของฟิลด์และค่าใหม่ที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="e2382-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="e2382-126">ฟิลด์ที่คุณเปลี่ยนแปลงจะคืนกลับเป็นค่าเดิม</span><span class="sxs-lookup"><span data-stu-id="e2382-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="e2382-127">ข้อความแสดงสถานะในหน้าจะแจ้งให้คุณทราบว่ายังไม่มีการส่งการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2382-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="e2382-128">ทุกครั้งที่คุณเปลี่ยนแปลงฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน ระบบจะเพิ่มฟิลด์นั้นลงในรายการของการเปลี่ยนแปลงที่นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="e2382-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="e2382-129">หากต้องการยกเลิกค่าที่นำเสนอสำหรับฟิลด์ ให้ใช้ปุ่ม **ละทิ้ง** ที่อยู่ถัดจากฟิลด์ในรายการ</span><span class="sxs-lookup"><span data-stu-id="e2382-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="e2382-130">หากต้องการยกเลิกการเปลี่ยนแปลงทั้งหมด ให้ใช้ปุ่ม **ละทิ้งการเปลี่ยนแปลงทั้งหมด** ที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="e2382-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="e2382-131">เลือก **ตกลง** เพื่อปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="e2382-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="e2382-132">หลังจากที่คุณมีการเปลี่ยนแปลงที่นำเสนออย่างน้อยหนึ่งรายการ จะปรากฏเมนูเพิ่มเติมสองเมนูบนบานหน้าต่างการดำเนินการ: **การเปลี่ยนแปลงที่นำเสนอ** และ **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="e2382-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="e2382-133">เลือก **การเปลี่ยนแปลงที่นำเสนอ** เพื่อเปิดหน้า **การเปลี่ยนแปลงที่นำเสนอ** และตรวจสอบการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="e2382-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="e2382-134">เลือก **ลำดับงาน \> ส่ง** เพื่อส่งการเปลี่ยนแปลงไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="e2382-135">สถานะในหน้าเปลี่ยนเป็น **การอนุมัติการเปลี่ยนแปลงที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="e2382-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="e2382-136">ลำดับงานจะดำเนินการตามกระบวนการของลำดับงานมาตรฐานในแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="e2382-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="e2382-137">ระบบจะนำผู้อนุมัติไปยังหน้า **ลูกค้า** ซึ่งเขาหรือเธอสามารถตรวจสอบการเปลี่ยนแปลงในหน้า **การเปลี่ยนแปลงที่นำเสนอ** แล้วเลือก **ลำดับงาน \> อนุมัติ** เพื่ออนุมัติลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="e2382-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="e2382-138">หลังจากการอนุมัติทั้งหมดเสร็จสมบูรณ์ ฟิลด์จะได้รับการอัปเดตเป็นค่าที่คุณนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="e2382-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
