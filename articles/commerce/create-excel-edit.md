---
title: สร้างเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการสร้างเวิร์กบุ๊ก Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/04/2020
ms.locfileid: "4460071"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="98dd0-103">สร้างเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="98dd0-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98dd0-104">หัวข้อนี้จะอธิบายวิธีการสร้างเวิร์กบุ๊ก Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="98dd0-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98dd0-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="98dd0-105">Overview</span></span>

<span data-ttu-id="98dd0-106">มีเท็มเพลต Excel ที่กำหนดไว้ล่วงหน้าซึ่งลูกค้าสามารถเข้าถึงได้จากส่วนต่างๆ ของระบบและใช้เพื่อแก้ไขและตรวจสอบธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="98dd0-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="98dd0-107">อย่างไรก็ตาม ลูกค้ายังสามารถสร้างเวิร์กบุ๊ก Excel แบบกำหนดเองสำหรับวัตถุประสงค์นี้ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="98dd0-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="98dd0-108">สร้างและตั้งค่าคอนฟิกเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="98dd0-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="98dd0-109">หากต้องการสร้างและตั้งค่าคอนฟิกเวิร์กบุ๊ก Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกได้ ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="98dd0-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="98dd0-110">เปิด Excel และสร้างเวิร์กบุ๊กเปล่า</span><span class="sxs-lookup"><span data-stu-id="98dd0-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="98dd0-111">บนแท็บ **แทรก** ให้เลือก **Add-in ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="98dd0-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="98dd0-112">ในบานหน้าต่างด้านขวา ให้เลือกลิงก์ **เพิ่มข้อมูลเซิร์ฟเวอร์**</span><span class="sxs-lookup"><span data-stu-id="98dd0-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="98dd0-113">ป้อน URL ของเซิร์ฟเวอร์ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="98dd0-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="98dd0-114">ถ้าคุณได้รับข้อความแสดงข้อผิดพลาด "ไม่พบการลงทะเบียนแอปเพล็ต" ให้ทำตามขั้นตอนต่อไปนี้เพื่อแก้ปัญหา:</span><span class="sxs-lookup"><span data-stu-id="98dd0-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="98dd0-115">ใน Commerce ให้ไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ของแอป Office**</span><span class="sxs-lookup"><span data-stu-id="98dd0-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="98dd0-116">บนแท็บด่วน **พารามิเตอร์ของแอป** ให้เลือก **เริ่มต้นพารามิเตอร์ของแอป**</span><span class="sxs-lookup"><span data-stu-id="98dd0-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="98dd0-117">ในกล่องข้อความการยืนยัน ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="98dd0-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="98dd0-118">บนแท็บด่วน **แอปเพล็ตที่ลงทะเบียน** ให้เลือก **เริ่มต้นการลงทะเบียนแอปเพล็ต**</span><span class="sxs-lookup"><span data-stu-id="98dd0-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="98dd0-119">ทำซ้ำสามขั้นตอนก่อนหน้านี้ตามที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="98dd0-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="98dd0-120">เลือก **ออกแบบ** แล้วเลือก **เพิ่มตาราง**</span><span class="sxs-lookup"><span data-stu-id="98dd0-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="98dd0-121">เลือกเอนทิตี้ที่ต้องเพิ่มลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขตามข้อมูลที่ต้องมีการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="98dd0-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="98dd0-122">ใช้ตารางต่อไปนี้เป็นข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="98dd0-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="98dd0-123">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="98dd0-123">Transaction type</span></span> | <span data-ttu-id="98dd0-124">เอนทิตี้ข้อมูลที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="98dd0-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="98dd0-125">ธุรกรรมเงินสดและการขนส่ง ใบสั่งออนไลน์ ใบสั่งของลูกค้าเอซิงค์ ใบเสนอราคาลูกค้าเอซิงค์</span><span class="sxs-lookup"><span data-stu-id="98dd0-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="98dd0-126">ธุรกรรม (ตรวจสอบได้) ธุรกรรมการขาย (ตรวจสอบได้) ธุรกรรมการชำระเงิน (ตรวจสอบได้) ธุรกรรมภาษี (ตรวจสอบได้) ธุรกรรมส่วนลด (ตรวจสอบได้) ธุรกรรมค่าธรรมเนียม (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="98dd0-127">การนำเงินฝากเข้าธนาคาร</span><span class="sxs-lookup"><span data-stu-id="98dd0-127">Bank drop</span></span> | <span data-ttu-id="98dd0-128">ธุรกรรม (ตรวจสอบได้) ธุรกรรมการชำระเงินที่ผ่านระบบธนาคาร (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="98dd0-129">การนำเงินฝากเข้าเซฟ</span><span class="sxs-lookup"><span data-stu-id="98dd0-129">Safe drop</span></span> | <span data-ttu-id="98dd0-130">ธุรกรรม (ตรวจสอบได้) ธุรกรรมการชำระเงินที่เข้าเซฟ (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="98dd0-131">การตรวจนับเงิน</span><span class="sxs-lookup"><span data-stu-id="98dd0-131">Tender declaration</span></span> | <span data-ttu-id="98dd0-132">ธุรกรรม (ตรวจสอบได้) ธุรกรรมการตรวจนับเงิน (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="98dd0-133">รายได้, ค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="98dd0-133">Income, Expense</span></span> | <span data-ttu-id="98dd0-134">ธุรกรรม (ตรวจสอบได้) ธุรกรรมรายได้/ค่าใช้จ่าย (ตรวจสอบได้) ธุรกรรมการชำระเงิน (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="98dd0-135">ตรวจนับจำนวนเงินเริ่มต้น การลบการชำระเงิน การป้อนข้อมูลเศษเงินทอน เงินทอน ใบแจ้งหนี้การชำระเงิน การฝากเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="98dd0-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="98dd0-136">ธุรกรรม (ตรวจสอบได้) ธุรกรรมการชำระเงิน (ตรวจสอบได้)</span><span class="sxs-lookup"><span data-stu-id="98dd0-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="98dd0-137">คุณต้องเพิ่มเพียงหนึ่งเอนทิตี้ข้อมูลลงในเวิร์กบุ๊ก Excel แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="98dd0-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="98dd0-138">นอกจากนี้ ต้องเพิ่มฟิลด์ทั้งหมดที่มีการทำเครื่องหมายด้วยสัญลักษณ์กุญแจลงในเวิร์กบุ๊กที่เกี่ยวข้องด้วย</span><span class="sxs-lookup"><span data-stu-id="98dd0-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="98dd0-139">หลังจากที่มีการตั้งค่าคอนฟิกเวิร์กบุ๊กแล้ว ให้ใช้ตัวกรองที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="98dd0-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="98dd0-140">ตรวจสอบให้แน่ใจว่าได้ใช้ตัวกรองเดียวกันกับเวิร์กบุ๊กทั้งหมดในไฟล์</span><span class="sxs-lookup"><span data-stu-id="98dd0-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="98dd0-141">หลีกเลี่ยงการโหลดข้อมูลจำนวนมากลงในไฟล์ Excel</span><span class="sxs-lookup"><span data-stu-id="98dd0-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="98dd0-142">เพราะอาจมีผลกระทบกับประสิทธิภาพ และ Excel และระบบของคุณอาจทำงานช้าลง</span><span class="sxs-lookup"><span data-stu-id="98dd0-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="98dd0-143">เราขอแนะนำให้คุณใช้ "บริษัท" และ "หมายเลขใบแจ้งยอด" หรือ "หมายเลขธุรกรรม" เป็นตัวกรองสำหรับไฟล์ของคุณเสมอ</span><span class="sxs-lookup"><span data-stu-id="98dd0-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="98dd0-144">หลังจากที่มีการตั้งค่าคอนฟิกตัวกรองแล้ว ให้เลือก **รีเฟรช** เพื่อโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="98dd0-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="98dd0-145">แก้ไขข้อมูลที่จำเป็นแล้วเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="98dd0-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="98dd0-146">ถ้าปุ่ม **เผยแพร่** ไม่พร้อมใช้งาน แสดงว่าฟิลด์ที่สำคัญบางฟิลด์อาจไม่ได้ถูกเพิ่มลงในเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="98dd0-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98dd0-147">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="98dd0-147">Additional resources</span></span>

[<span data-ttu-id="98dd0-148">แก้ไขและตรวจสอบธุรกรรมเงินสดและการขนส่งและการจัดการเงินสด</span><span class="sxs-lookup"><span data-stu-id="98dd0-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="98dd0-149">แก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="98dd0-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="98dd0-150">แก้ไขมิติทางการเงินสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="98dd0-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="98dd0-151">เพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="98dd0-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
