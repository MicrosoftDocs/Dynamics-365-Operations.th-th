---
title: "ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกองค์ประกอบลำดับงานของสินค้าในรายการ"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0a57baa3ecae727721f62477cfc5fa41f60ad06d
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="configure-line-item-workflows"></a><span data-ttu-id="65425-103">ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65425-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกองค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="65425-105">หากต้องการตั้งค่าคอนฟิกองค์ประกอบลำดับงานของสินค้าในรายการในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่องค์ประกอบนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดหน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="65425-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="65425-106">จากนั้น ให้ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติต่างๆ ขององค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="65425-107">ตั้งชื่อองค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-107">Name the line-item workflow element</span></span>
<span data-ttu-id="65425-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับองค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="65425-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="65425-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="65425-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อเฉพาะสำหรับองค์ประกอบลำดับงานของสินค้าในรายการ</span><span class="sxs-lookup"><span data-stu-id="65425-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="65425-111">ระบุว่าจะใช้ลำดับงานเดียวกันในการประมวลผลสินค้าในรายการทั้งหมดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65425-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="65425-112">ทำตามขั้นตอนเหล่านี้เพื่อระบุว่าจะใช้ลำดับงานเดียวกันในการประมวลผลสินค้าในรายการทั้งหมดบนเอกสารเดียวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65425-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="65425-113">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="65425-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="65425-114">ถ้าควรใช้ลำดับงานเดียวกันในการประมวลผลสินค้าในรายการทั้งหมดบนเอกสารเดียว ให้คลิก **เรียกลำดับงานเดียวสำหรับสินค้าในรายการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="65425-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="65425-115">จากนั้นเลือกลำดับงานที่จะใช้ในการประมวลผลสินค้าในรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="65425-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="65425-116">ถ้าควรใช้ลำดับงานเฉพาะในการประมวลผลสินค้าในรายการที่ตรงกับชุดเงื่อนไขที่เฉพาะเจาะจง ให้คลิก **เรียกลำดับงานสำหรับสินค้าในรายการแต่ละรายการ**</span><span class="sxs-lookup"><span data-stu-id="65425-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="65425-117">จากนั้น ทำตามขั้นตอนเหล่านี้เพื่อกำหนดชุดของเงื่อนไข:</span><span class="sxs-lookup"><span data-stu-id="65425-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="65425-118">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="65425-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="65425-119">เลือกเงื่อนไขในตาราง</span><span class="sxs-lookup"><span data-stu-id="65425-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="65425-120">บนแท็บ **ชื่อเงื่อนไข** ป้อนชื่อสำหรับชุดของเงื่อนไขที่คุณกำลังกำหนด</span><span class="sxs-lookup"><span data-stu-id="65425-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="65425-121">คลิก **เพิ่มเงื่อนไข** เพื่อป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="65425-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="65425-122">ป้อนเงื่อนไขเพิ่มเติมใด ๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="65425-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="65425-123">หากต้องการตรวจสอบว่าชุดของเงื่อนไขที่คุณป้อนเข้าไปถูกตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="65425-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="65425-124">ในหน้า **ทดสอบเงื่อนไขลำดับงาน** ในพื้นที่ **ตรวจสอบความถูกต้องของเงื่อนไข** เลือกเรกคอร์ด แล้วคลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="65425-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="65425-125">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="65425-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="65425-126">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่หน้า **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="65425-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="65425-127">บนแท็บ **ลำดับงาน** เลือกลำดับงานที่จะใช้ในการประมวลผลสินค้าในรายการที่ตรงกับชุดของเงื่อนไขที่คุณกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="65425-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





