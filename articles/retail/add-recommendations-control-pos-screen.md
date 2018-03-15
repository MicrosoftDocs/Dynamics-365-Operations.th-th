---
title: "เพิ่มตัวควบคุมคำแนะนำในหน้าธุรกรรมบนอุปกรณ์ POS"
description: "หัวข้อนี้อธิบายวิธีการเพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ขายหน้าร้าน (POS) ที่ใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 for Retail"
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: b99d1d30fc320bca5c49921b7c4ccdd7e977f67c
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="ad069-103">เพิ่มตัวควบคุมคำแนะนำในหน้าธุรกรรมบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="ad069-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ad069-104">เราจะลบเวอร์ชันปัจจุบันของบริการแนะนำผลิตภัณฑ์ เนื่องจากเราได้ออกแบบคุณลักษณะนี้ใหม่พร้อมกับอัลกอริทึมที่ดีขึ้นและความสามารถที่เกี่ยวข้องกับการขายปลีกที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="ad069-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="ad069-105">สำหรับข้อมูลเพิ่มเติม ให้ดู [ลบหรือเลิกใช้คุณลักษณะ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)</span><span class="sxs-lookup"><span data-stu-id="ad069-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="ad069-106">หัวข้อนี้อธิบายวิธีการเพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ขายหน้าร้าน (POS) ที่ใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="ad069-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="ad069-107">คุณสามารถแสดงคำแนะนำผลิตภัณฑ์บนอุปกรณ์ POS ของคุณเมื่อคุณใช้ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="ad069-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="ad069-108">*รายการแนะนำ* คือสินค้าที่ลูกค้าของคุณอาจสนใจโดยยึดตามของประวัติการซื้อของพวกเขา สินค้าในรายการสิ่งที่ต้องการของพวกเขา และสินค้าที่ลูกค้ารายอื่นซื้อแบบออนไลน์และในร้านค้าจริง</span><span class="sxs-lookup"><span data-stu-id="ad069-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="ad069-109">เมื่อต้องการแสดงคำแนะนำผลิตภัณฑ์ คุณต้องเพิ่มตัวควบคุมไปยังหน้าจอธุรกรรมโดยใช้ตัวออกแบบโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="ad069-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="ad069-110">เปิดตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="ad069-110">Open Layout designer</span></span>
1.  <span data-ttu-id="ad069-111">ไปที่ **การขายปลีก** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **POS** &gt; **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="ad069-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="ad069-112">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาหน้าจอที่คุณต้องการเพิ่มตัวควบคุม</span><span class="sxs-lookup"><span data-stu-id="ad069-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="ad069-113">ตัวอย่างเช่น ตัวกรองบนฟิลด์ **รหัสโครงร่างหน้าจอ** โดยใช้ค่า 'F2CP16:9M'</span><span class="sxs-lookup"><span data-stu-id="ad069-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="ad069-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad069-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="ad069-115">ตัวอย่างเช่น เลือก ‘ชื่อ: F2CP16:9M รหัสโครงร่างหน้าจอ: F2CP16:9M’</span><span class="sxs-lookup"><span data-stu-id="ad069-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="ad069-116">คลิก **ตัวออกแบบโครงร่าง**</span><span class="sxs-lookup"><span data-stu-id="ad069-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="ad069-117">ทำตามพร้อมต์เพื่อเปิดใช้งานตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="ad069-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="ad069-118">เมื่อได้รับพร้อมต์สำหรับข้อมูลประจำตัว ให้ป้อนข้อมูลประจำตัวเดียวกันที่ถูกใช้เมื่อมีการเปิดใช้ตัวออกแบบโครงร่างจากหน้า **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="ad069-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="ad069-119">เมื่อคุณเข้าสู่ระบบ หน้าที่คล้ายกับหน้าด้านล่างนี้จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="ad069-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="ad069-120">โครงร่างจะแตกต่างกันโดยขึ้นอยู่กับการเลือกกำหนดที่ทำไว้สำหรับร้านค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="ad069-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="ad069-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) เลือกตัวเลือกการแสดง</span><span class="sxs-lookup"><span data-stu-id="ad069-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="ad069-122">มีตัวเลือกสองตัวสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="ad069-122">There are two configurations options available.</span></span> <span data-ttu-id="ad069-123">เลือกตัวเลือกที่ดีที่สุดสำหรับร้านค้าของคุณ และทำตามคำแนะนำที่เหลือเพื่อทำการตั้งค่าตัวควบคุมให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="ad069-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="ad069-124">ตัวเลือกสองตัว ได้แก่</span><span class="sxs-lookup"><span data-stu-id="ad069-124">The two options are:</span></span>
-   <span data-ttu-id="ad069-125">คำแนะนำจะปรากฏขึ้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="ad069-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="ad069-126">แท็บ **คำแนะนำ** จะปรากฏในกริดทางด้านขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="ad069-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="ad069-127">เมื่อต้องการทำให้คำแนะนำปรากฏขึ้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="ad069-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="ad069-128">ให้ลดความสูงของพื้นที่รายละเอียดของบรรทัดธุรกรรมเพื่อให้มีความสูงเท่ากับแผงสำหรับลูกค้าที่แสดงที่ด้านซ้าย[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="ad069-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="ad069-129">จากเมนูทางด้านซ้าย ลากและปล่อยตัวควบคุมคำแนะนำระหว่างพื้นที่รายละเอียดของบรรทัดธุรกรรมและกริดปุ่มในศูนย์กลางด้านล่างของหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ad069-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="ad069-130">ปรับขนาดตัวควบคุมเพื่อให้พอดีในช่องนั้น[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="ad069-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="ad069-131">คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="ad069-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="ad069-132">ใน Dynamics 365 for Retail ไปที่ **การขายปลีก** &gt; **ไอทีการขายปลีก** &gt; **กำหนดการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="ad069-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="ad069-133">ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="ad069-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="ad069-134">คลิก **รันทันที**</span><span class="sxs-lookup"><span data-stu-id="ad069-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="ad069-135">เมื่อต้องการเพิ่มแท็บคำแนะนำไปยังกริดปุ่มทางด้านขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="ad069-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="ad069-136">คลิกขวาในพื้นที่ว่างที่อยู่ด้านล่างของแท็บสุดท้ายในกริดปุ่มที่อยู่ทางด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="ad069-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="ad069-137">คลิก **เลือกกำหนด**[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="ad069-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="ad069-138">คลิก **แท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="ad069-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="ad069-139">ค้นหาแท็บใหม่ที่คุณเพิ่งเพิ่มเข้ามา</span><span class="sxs-lookup"><span data-stu-id="ad069-139">Find the new tab that you just added.</span></span> <span data-ttu-id="ad069-140">คุณอาจต้องเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="ad069-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="ad069-141">ในเมนูแบบหล่นลง **เนื้อหา** เลือก**ผลิตภัณฑ์ที่แนะนำ**</span><span class="sxs-lookup"><span data-stu-id="ad069-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="ad069-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="ad069-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="ad069-143">ในฟิลด์ **ป้ายชื่อ** พิมพ์ชื่อสำหรับแท็บคำแนะนำ ตัวอย่างเช่น พิมพ์ 'ผลิตภัณฑ์ที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="ad069-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="ad069-144">ในฟิลด์ **รูปภาพ** ให้เลือกรูปภาพที่จะให้ปรากฏบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="ad069-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="ad069-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ad069-145">Click **OK**.</span></span> <span data-ttu-id="ad069-146">แท็บใหม่จะปรากฏในกริดปุ่ม</span><span class="sxs-lookup"><span data-stu-id="ad069-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="ad069-147">คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="ad069-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="ad069-148">ใน Dynamics 365 for Retail ไปที่ **การขายปลีก** &gt; **ไอทีการขายปลีก** &gt; **กำหนดการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="ad069-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="ad069-149">ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="ad069-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="ad069-150">คลิก **รันทันที**</span><span class="sxs-lookup"><span data-stu-id="ad069-150">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="ad069-151">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ad069-151">See also</span></span>
--------

[<span data-ttu-id="ad069-152">ภาพรวมคำแนะนำผลิตภัณฑ์แบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="ad069-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




