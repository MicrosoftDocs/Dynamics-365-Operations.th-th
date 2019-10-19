---
title: ลำดับงานของผู้จัดจำหน่าย
description: ปรับเปลี่ยนข้อมูลผู้จัดจำหน่าย และใช้ลำดับงานเพื่ออนุมัติ
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: afda0ead11ec1adac2d436511eef8165a7f0aed2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189280"
---
# <a name="vendor-workflow"></a><span data-ttu-id="bcb45-103">ลำดับงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bcb45-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcb45-104">เมื่อมีการใช้ลำดับงานของผู้จัดจำหน่าย การเปลี่ยนแปลงที่ทำกับฟิลด์ที่ระบุจะถูกส่งไปยังลำดับงานสำหรับการอนุมัติ ก่อนที่จะเพิ่มไปยังผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bcb45-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="bcb45-105">ตั้งค่าลำดับงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bcb45-105">Set up the vendor workflow</span></span>

<span data-ttu-id="bcb45-106">ก่อนที่คุณจะสามารถใช้คุณลักษณะของลำดับงาน คุณต้องเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="bcb45-107">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="bcb45-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="bcb45-108">บนแท็บ **ทั่วไป** บน FastTab **การอนุมัติผู้จัดจำหน่าย** ตั้งค่าตัวเลือก **เปิดใช้งานการอนุมัติผู้จัดจำหน่าย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="bcb45-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="bcb45-109">ในฟิลด์ **พฤติกรรมเอนทิตีข้อมูล** เลือกพฤติกรรมที่ควรใช้เมื่อมีการนำเข้าข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="bcb45-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="bcb45-110">**อนุญาตให้เปลี่ยนแปลง โดยไม่มีการอนุมัติ** – เอนทิตีข้อมูลสามารถปรับปรุงเรกคอร์ดผู้จัดจำหน่ายโดยไม่มีการประมวลผลโดยใช้ลำดับงานได้</span><span class="sxs-lookup"><span data-stu-id="bcb45-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="bcb45-111">**ปฏิเสธการเปลี่ยนแปลง** – ไม่สามารถทำการเปลี่ยนแปลงกับเรกคอร์ดผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="bcb45-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="bcb45-112">การนำเข้าจะล้มเหลวสำหรับฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="bcb45-113">**สร้างข้อเสนอการเปลี่ยน** – จะมีการเปลี่ยนแปลงฟิลด์ทั้งหมด ยกเว้นฟิลด์ที่ถูกเปิดใช้งานสำหรับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="bcb45-114">ค่าใหม่สำหรับฟิลด์เหล่านั้นที่จะถูกเพิ่มไปยังผู้จัดจำหน่ายเป็นการเปลี่ยนแปลงที่เสนอ และลำดับงานจะถูกเริ่มต้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bcb45-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="bcb45-115">ในรายการของฟิลด์ผู้จัดจำหน่าย เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** สำหรับฟิลด์ทุกฟิลด์ที่ต้องได้รับอนุมัติ ก่อนที่จะสามารถทำการเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="bcb45-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="bcb45-116">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่า \> ลำดับงานของบัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="bcb45-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="bcb45-117">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="bcb45-117">Select **New**.</span></span>
7. <span data-ttu-id="bcb45-118">เลือก **ลำดับงานของการเปลี่ยนแปลงที่นำเสนอของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="bcb45-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="bcb45-119">ตั้งค่าลำดับงานเพื่อให้ตรงกับกระบวนการอนุมัติของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcb45-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="bcb45-120">องค์ประกอบการอนุมัติลำดับงาน **การอนุมัติลำดับงานสำหรับการเปลี่ยนแปลงของผู้จัดจำหน่ายที่เสนอ** จะใช้การเปลี่ยนแปลงกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="bcb45-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="bcb45-121">เปลี่ยนข้อมูลผู้จัดจำหน่าย และส่งการเปลี่ยนแปลงไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="bcb45-122">เมื่อคุณเปลี่ยนฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน หน้า **การเปลี่ยนแปลงที่เสนอ** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="bcb45-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="bcb45-123">หน้านี้จะแสดงค่าเดิมของฟิลด์และค่าใหม่ที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="bcb45-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="bcb45-124">ฟิลด์ที่คุณทำการเปลี่ยนแปลงถูกแปลงกลับเป็นค่าเดิม</span><span class="sxs-lookup"><span data-stu-id="bcb45-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="bcb45-125">ข้อความสถานะยังจะแจ้งให้คุณทราบว่า ยังไม่มีการส่งการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcb45-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="bcb45-126">ทุกครั้งที่คุณเปลี่ยนฟิลด์ที่เปิดใช้งานสำหรับลำดับงาน ฟิลด์นั้นจะถูกเพิ่มลงในรายการบนหน้า **การเปลี่ยนแปลงที่เสนอ**</span><span class="sxs-lookup"><span data-stu-id="bcb45-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="bcb45-127">เมื่อต้องการละทิ้งค่าที่เสนอสำหรับฟิลด์ ใช้ปุ่ม **ละทิ้ง** ที่ถัดจากฟิลด์ในรายการ</span><span class="sxs-lookup"><span data-stu-id="bcb45-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="bcb45-128">เมื่อต้องการละทิ้งการเปลี่ยนแปลงทั้งหมด ใช้ปุ่ม **ละทิ้งการเปลี่ยนแปลงทั้งหมด** ที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="bcb45-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="bcb45-129">เลือก **ตกลง** เพื่อปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bcb45-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="bcb45-130">หลังจากที่คุณมีการเปลี่ยนแปลงที่เสนออย่างน้อยหนึ่งรายการ แท็บเพิ่มเติมสองแท็บจะปรากฏในบานหน้าต่างการดำเนินการ: **การเปลี่ยนแปลงที่เสนอ** และ **ลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="bcb45-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="bcb45-131">เลือก **การเปลี่ยนแปลงที่เสนอ** เพื่อเปิดหน้า **การเปลี่ยนแปลงที่เสนอ** และตรวจทานการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="bcb45-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="bcb45-132">เลือก **ลำดับงาน \> เพื่อส่งการเปลี่ยนแปลงไปยังลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="bcb45-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="bcb45-133">สถานะในหน้าเปลี่ยนเป็น **การอนุมัติการเปลี่ยนแปลงที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="bcb45-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="bcb45-134">เวิร์กโฟลว์ติดตามกระบวนการเวิร์กโฟลว์มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="bcb45-135">ผู้อนุมัติถูกส่งตรงไปยังหน้า **ผู้จัดจำหน่าย** ที่เขาหรือเธอสามารถตรวจสอบการเปลี่ยนแปลงในหน้า **การเปลี่ยนแปลงที่เสนอ** ได้ และจากนั้น เลือก **ลำดับงาน \> อนุมัติ** เพื่ออนุมัติลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bcb45-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="bcb45-136">หลังจากการอนุมัติทั้งหมดเสร็จสมบูรณ์ ฟิลด์จะได้รับการอัปเดตเป็นค่าที่คุณนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="bcb45-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
