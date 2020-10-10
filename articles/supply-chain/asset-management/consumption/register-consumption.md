---
title: ลงทะเบียนปริมาณการใช้
description: หัวข้อนี้อธิบายวิธีการลงทะเบียนปริมาณการใช้ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c9bbd51da23ea412bc124f932f73876a9506d47
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889252"
---
# <a name="register-consumption"></a><span data-ttu-id="acdbb-103">ลงทะเบียนปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="acdbb-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="acdbb-104">เมื่องานบำรุงรักษาเสร็จสมบูรณ์แล้วในใบสั่งงาน ขั้นตอนต่อไปคือการทำการลงทะเบียนปริมาณการใช้และลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="acdbb-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="acdbb-105">คุณสามารถทำการลงทะเบียนในชนิดปริมาณการใช้วัสดุต่อไปนี้: ชั่วโมง สินค้า และค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="acdbb-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="acdbb-106">ชนิดของปริมาณการใช้วัสดุที่แตกต่างกันจะมีการลงทะเบียนและลงรายการบัญชีบนหน้า **สมุดรายวันใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="acdbb-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="acdbb-107">มีการใช้การตั้งค่าสมุดรายวันใน **การจัดการสินทรัพย์** สำหรับการสร้างและการลงรายการบัญชีสมุดรายวันที่แยกต่างหากสำหรับชั่วโมง สินค้า และค่าใช้จ่ายในโมดูล **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="acdbb-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="acdbb-108">ในบางกรณี คุณอาจสามารถเพิ่มหรือลบรายการการคาดการณ์บนใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="acdbb-109">การตั้งค่าสถานะวงจรการใช้ใบสั่งงาน ชนิดโครงการที่เกี่ยวข้อง และกฎขั้นที่เกี่ยวข้องกับชนิดโครงการจะเป็นตัวกำหนดว่าคุณสามารถเพิ่มหรือแก้ไขรายการสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="acdbb-110">อ่านเพิ่มเติมเกี่ยวกับสถานะของวงจรการใช้ของใบสั่งงานและขั้นโครงการที่เกี่ยวข้องใน [การคาดการณ์ ใบสั่งงาน และโครงการ](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)</span><span class="sxs-lookup"><span data-stu-id="acdbb-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="acdbb-111">คุณสามารถตั้งค่าการลงรายการบัญชีสมุดรายวันโดยอัตโนมัติในสถานะวงจรการใช้ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="acdbb-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="acdbb-112">อ้างอิง [สถานะวงจรใบสั่งงาน](../setup-for-work-orders/work-order-lifecycle-states.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="acdbb-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="acdbb-113">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="acdbb-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="acdbb-114">เลือกใบสั่งงาน และคลิก **สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="acdbb-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="acdbb-115">คลิก **คัดลอกจากการคาดการณ์** เพื่อโอนย้ายรายการคาดการณ์ใดๆ ที่อาจจะเชื่อมต่อกับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="acdbb-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="acdbb-116">คุณสามารถเลือกชนิดของปริมาณการใช้วัสดุที่คุณต้องการโอนย้ายได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="acdbb-117">ถ้าจำเป็น คุณสามารถเพิ่มรายการปริมาณการใช้วัสดุเพิ่มเติมบนแท็บด่วนโดยคลิกที่ **เพิ่มรายการ** และการกรอกข้อมูลในรายการ</span><span class="sxs-lookup"><span data-stu-id="acdbb-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="acdbb-118">คลิก **ตรวจสอบความถูกต้องของสมุดรายวัน** เพื่อตรวจสอบความถูกต้องของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="acdbb-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="acdbb-119">คลิก **ลงรายการบัญชีสมุดรายวัน** เพื่อลงรายการบัญชีรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="acdbb-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="acdbb-120">หลังจากที่คุณลงรายการบัญชีสมุดรายวันปริมาณการใช้แล้ว คุณสามารถอัพเดตข้อมูลสถานะของวงจรการใช้ของใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="acdbb-121">ตัวอย่างเช่น ถ้าต้องการระบุว่าใบสั่งงานเสร็จสมบูรณ์แล้ว คุณสามารถอัพเดตสถานะของวงจรการใช้เป็น "สิ้นสุดแล้ว"</span><span class="sxs-lookup"><span data-stu-id="acdbb-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="acdbb-122">ในฟิลด์ **แสดง** ที่ด้านบนของหน้า **สมุดรายวันใบสั่งงาน** ให้เลือกรายการสมุดรายวันที่คุณต้องการดู: **ทั้งหมด** **ไม่ได้ลงรายการบัญชี** หรือ **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="acdbb-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="acdbb-123">สมุดรายวันที่ลงรายการบัญชีมีเครื่องหมายถูกในกล่องกาเครื่องหมาย **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="acdbb-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="acdbb-124">เมื่อมีการสร้างรายการสินค้าในสมุดรายวันใบสั่งงาน มิติของผลิตภัณฑ์ และมิติการติดตามที่เกี่ยวข้องกับสินค้าจะถูกโอนย้ายไปยังรายการสมุดรายวันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="acdbb-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="acdbb-125">ภาพหน้าจอด้านล่างแสดงตัวอย่างของการลงทะเบียนชั่วโมงและสินค้าในใบสั่งงานใน **สมุดรายวันใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="acdbb-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![รูปที่ 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="acdbb-127">แบ่งชั่วโมงของใบสั่งงานที่มีงานใบสั่งงานหลายงาน</span><span class="sxs-lookup"><span data-stu-id="acdbb-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="acdbb-128">ถ้าใบสั่งงานมีงานใบสั่งงานหลายงาน คุณสามารถลงทะเบียนชั่วโมงทำงานโดยใช้ฟังก์ชัน **แบ่งชั่วโมง** ซึ่งหมายความว่ารายการลงทะเบียนชั่วโมงหนึ่งสามารถกระจายอย่างสม่ำเสมอในแต่ละงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="acdbb-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="acdbb-129">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="acdbb-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="acdbb-130">เลือกใบสั่งงาน และคลิก **สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="acdbb-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="acdbb-131">เลือกบรรทัดการลงทะเบียนชั่วโมงที่คุณต้องการแบ่ง แล้วคลิก **แบ่งชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="acdbb-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="acdbb-132">ในกล่องโต้ตอบ **แบ่งชั่วโมงงานการบำรุงรักษาใบสั่งงาน** ชื่อของผู้ปฏิบัติงานที่ล็อกอินจะแสดงขึ้นโดยอัตโนมัติในฟิลด์ **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="acdbb-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="acdbb-133">ถ้าจำเป็น คุณสามารถเลือกผู้ปฏิบัติงานอื่นได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="acdbb-134">เลือกประเภทสำหรับการลงทะเบียนชั่วโมงในฟิลด์ **ประเภท**</span><span class="sxs-lookup"><span data-stu-id="acdbb-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="acdbb-135">แทรกจำนวนชั่วโมงทำงานที่จะแบ่งในฟิลด์ **ชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="acdbb-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![รูปที่ 2](media/02-consumption.png)

7. <span data-ttu-id="acdbb-137">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="acdbb-137">Click **OK**.</span></span>

<span data-ttu-id="acdbb-138">*ตัวอย่าง:* ในภาพหน้าจอด้านล่าง รายการสมุดรายวันสำหรับใบสั่งงานที่มีงานใบสั่งงานสามงานจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="acdbb-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="acdbb-139">รายการแรกที่มีชั่วโมงการทำงานสามชั่วโมง จะถูกแบ่งและมีการลงทะเบียนชั่วโมงงานหนึ่งชั่วโมงสำหรับแต่ละงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="acdbb-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="acdbb-140">หลังจากที่สร้างรายการลงทะเบียนสามชั่วโมงแล้ว ให้คุณตัดสินใจว่าจะทำอะไรกับรายการลงทะเบียนชั่วโมงดั้งเดิม (รายการแรกในตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="acdbb-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="acdbb-141">คุณสามารถเก็บไว้หรือลบออกก็ได้</span><span class="sxs-lookup"><span data-stu-id="acdbb-141">You can keep it as is or delete it.</span></span> 

![รูปที่ 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="acdbb-143">มิติทางการเงินสำหรับการลงทะเบียนปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="acdbb-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="acdbb-144">เมื่อคุณทำการลงทะเบียนปริมาณการใช้ มิติทางการเงินที่เกี่ยวข้องกับชนิดของการลงทะเบียนต่างๆ จะถูกเพิ่มเข้าไปในการลงทะเบียนในลำดับที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="acdbb-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="acdbb-145">*การลงทะเบียนชั่วโมงและค่าใช้จ่าย:* อันดับแรก มิติทางการเงินจากหัวข้อสมุดรายวันจะถูกเพิ่ม ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="acdbb-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="acdbb-146">ถัดไป มิติทางการเงินจากโครงการของใบสั่งงานที่เกี่ยวข้องจะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="acdbb-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="acdbb-147">สุดท้าย มิติทางการเงินจากทรัพยากร (ผู้ปฏิบัติงาน) จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="acdbb-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="acdbb-148">*การลงทะเบียนสินค้า* อันดับแรก มิติทางการเงินจากหัวข้อสมุดรายวันจะถูกเพิ่ม ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="acdbb-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="acdbb-149">จากนั้น มิติทางการเงินจากโครงการของใบสั่งงานที่เกี่ยวข้องจะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="acdbb-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="acdbb-150">ถัดไป มิติทางการเงินจากไซต์จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="acdbb-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="acdbb-151">สุดท้าย มิติทางการเงินจากสินค้าจะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="acdbb-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="acdbb-152">สำหรับการลงทะเบียนทั้งสามชนิด จะมีการตรวจสอบความถูกต้องของชุดมิติทางการเงิน และชุดข้อมูลที่ไม่ถูกต้องจะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="acdbb-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="acdbb-153">นี่คือการตั้งค่ามาตรฐานด้วยแอป Finance and Operations อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="acdbb-153">This is standard setup with other Finance and Operations apps.</span></span>

