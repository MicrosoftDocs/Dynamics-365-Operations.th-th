---
title: เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS
description: หัวข้อนี้อธิบายวิธีการเพิ่มการควบคุมคำแนะนำไปยังหน้าจอธุรกรรมบนอุปกรณ์ point of sale (POS) โดยใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 for Retail
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811227"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="390ee-103">เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="390ee-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="390ee-104">หัวข้อนี้อธิบายวิธีการเพิ่มการควบคุมคำแนะนำไปยังหน้าจอธุรกรรมบนอุปกรณ์ point of sale (POS) โดยใช้ตัวออกแบบโครงร่างหน้าจอใน Microsoft Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="390ee-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="390ee-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](product.md)</span><span class="sxs-lookup"><span data-stu-id="390ee-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="390ee-106">คุณสามารถแสดงคำแนะนำผลิตภัณฑ์บนอุปกรณ์ POS ของคุณได้ เมื่อคุณใช้ Microsoft Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="390ee-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="390ee-107">เมื่อต้องการแสดงคำแนะนำผลิตภัณฑ์ คุณต้องเพิ่มตัวควบคุมไปยังหน้าจอธุรกรรมโดยใช้ตัวออกแบบโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="390ee-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="390ee-108">เปิดตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="390ee-108">Open Layout designer</span></span>

1. <span data-ttu-id="390ee-109">ไปที่ **การขายปลีก** &gt; **การตั้งค่าช่องทาง** &gt; **การตั้งค่า POS** &gt; **POS** &gt; **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="390ee-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="390ee-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาหน้าจอที่คุณต้องการเพิ่มตัวควบคุม</span><span class="sxs-lookup"><span data-stu-id="390ee-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="390ee-111">ตัวอย่างเช่น ตัวกรองบนฟิลด์ **รหัสโครงร่างหน้าจอ** โดยใช้ค่า **F2CP16:9M**</span><span class="sxs-lookup"><span data-stu-id="390ee-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="390ee-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="390ee-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="390ee-113">ตัวอย่างเช่น เลือก **ชื่อ: F2CP16:9M รหัสโครงร่างหน้าจอ: F2CP16:9M**</span><span class="sxs-lookup"><span data-stu-id="390ee-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="390ee-114">คลิก **ตัวออกแบบโครงร่าง**</span><span class="sxs-lookup"><span data-stu-id="390ee-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="390ee-115">ทำตามพร้อมต์เพื่อเปิดใช้งานตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="390ee-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="390ee-116">เมื่อได้รับพร้อมต์สำหรับข้อมูลประจำตัว ให้ป้อนข้อมูลประจำตัวเดียวกันที่ถูกใช้เมื่อมีการเปิดใช้ตัวออกแบบโครงร่างจากเพจ **โครงร่างหน้าจอ**</span><span class="sxs-lookup"><span data-stu-id="390ee-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="390ee-117">เมื่อคุณเข้าสู่ระบบ หน้าที่คล้ายกับหน้าด้านล่างนี้จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="390ee-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="390ee-118">โครงร่างจะแตกต่างกันโดยขึ้นอยู่กับการเลือกกำหนดที่ทำไว้สำหรับร้านค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="390ee-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="390ee-119">[![ตัวออกแบบโครงร่าง](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="390ee-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="390ee-120">เลือกตัวเลือกการแสดง</span><span class="sxs-lookup"><span data-stu-id="390ee-120">Choose a display option</span></span>

<span data-ttu-id="390ee-121">มีตัวเลือกสองตัวสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="390ee-121">There are two configurations options available.</span></span> <span data-ttu-id="390ee-122">เลือกตัวเลือกที่ดีที่สุดสำหรับร้านค้าของคุณ และทำตามคำแนะนำที่เหลือเพื่อทำการตั้งค่าตัวควบคุมให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="390ee-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="390ee-123">ตัวเลือกสองตัว ได้แก่</span><span class="sxs-lookup"><span data-stu-id="390ee-123">The two options are:</span></span>

- <span data-ttu-id="390ee-124">คำแนะนำจะปรากฏขึ้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="390ee-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="390ee-125">แท็บ **คำแนะนำ** จะปรากฏในกริดทางด้านขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="390ee-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="390ee-126">ทำให้คำแนะนำปรากฏขึ้นเสมอ</span><span class="sxs-lookup"><span data-stu-id="390ee-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="390ee-127">ลดความสูงของพื้นที่รายละเอียดของรายการธุรกรรม เพื่อให้มีความสูงเท่ากับแผงสำหรับลูกค้าทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="390ee-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="390ee-128">[![ความสูงของพื้นที่รายละเอียดของรายการธุรกรรมถูกลดลง](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="390ee-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="390ee-129">จากเมนูทางด้านซ้าย ลากและปล่อยตัวควบคุมคำแนะนำระหว่างพื้นที่รายละเอียดของบรรทัดธุรกรรมและกริดปุ่มในศูนย์กลางด้านล่างของหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="390ee-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="390ee-130">ปรับขนาดตัวควบคุมเพื่อให้พอดีในช่องนั้น</span><span class="sxs-lookup"><span data-stu-id="390ee-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="390ee-131">[![ตัวควบคุมคำแนะนำถูกเพิ่มลงในโครงร่าง](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="390ee-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="390ee-132">คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="390ee-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="390ee-133">ใน Dynamics 365 for Retail ไปยัง **Retail** &gt; **Retail IT** &gt; **กำหนดการการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="390ee-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="390ee-134">ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="390ee-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="390ee-135">คลิก **รันทันที**</span><span class="sxs-lookup"><span data-stu-id="390ee-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="390ee-136">เพิ่มแท็บคำแนะนำไปยังกริดปุ่มทางด้านขวาของหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="390ee-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="390ee-137">คลิกขวาในพื้นที่ว่างที่อยู่ด้านล่างของแท็บสุดท้ายในกริดปุ่มที่อยู่ทางด้านขวาของหน้า</span><span class="sxs-lookup"><span data-stu-id="390ee-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="390ee-138">คลิก **กำหนด**</span><span class="sxs-lookup"><span data-stu-id="390ee-138">Click **Customize**.</span></span>

    <span data-ttu-id="390ee-139">[![กล่องโต้ตอบการเลือกกำหนด - ตัวควบคุมแท็บ](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="390ee-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="390ee-140">คลิก **แท็บใหม่**</span><span class="sxs-lookup"><span data-stu-id="390ee-140">Click **New tab**.</span></span>
4. <span data-ttu-id="390ee-141">ค้นหาแท็บใหม่ที่คุณเพิ่งเพิ่มเข้ามา</span><span class="sxs-lookup"><span data-stu-id="390ee-141">Find the new tab that you just added.</span></span> <span data-ttu-id="390ee-142">คุณอาจต้องเลื่อนลง</span><span class="sxs-lookup"><span data-stu-id="390ee-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="390ee-143">ในเมนูแบบหล่นลง **เนื้อหา** เลือก**ผลิตภัณฑ์ที่แนะนำ**</span><span class="sxs-lookup"><span data-stu-id="390ee-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="390ee-144">[![การเลือกผลิตภัณฑ์ที่แนะนำในฟิลด์เนื้อหา](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="390ee-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="390ee-145">ในฟิลด์ **ป้ายชื่อ** พิมพ์ชื่อสำหรับแท็บคำแนะนำ ตัวอย่างเช่น พิมพ์ 'ผลิตภัณฑ์ที่แนะนำ'</span><span class="sxs-lookup"><span data-stu-id="390ee-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="390ee-146">ในฟิลด์ **รูปภาพ** ให้เลือกรูปภาพที่จะให้ปรากฏบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="390ee-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="390ee-147">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="390ee-147">Click **OK**.</span></span> <span data-ttu-id="390ee-148">แท็บใหม่จะปรากฏในกริดปุ่ม</span><span class="sxs-lookup"><span data-stu-id="390ee-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="390ee-149">คลิก **X** เพื่อบันทึกและออกจากตัวออกแบบโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="390ee-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="390ee-150">ใน Dynamics 365 for Retail ไปยัง **Retail** &gt; **Retail IT** &gt; **กำหนดการการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="390ee-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="390ee-151">ในรายการ เลือก **1090 เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="390ee-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="390ee-152">คลิก **รันทันที**</span><span class="sxs-lookup"><span data-stu-id="390ee-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="390ee-153">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="390ee-153">Additional resources</span></span>

[<span data-ttu-id="390ee-154">คำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="390ee-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="390ee-155">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="390ee-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
