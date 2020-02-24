---
title: สร้างและอัพเดตรายละเอียดการส่งคืนและการขอคืนเงิน สำหรับช่องทาง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่านโยบายการส่งคืนและการขอคืนเงินสำหรับช่องทาง
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 66bb9bbd338561315f2f69ae4aff86a67513b190
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024269"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="163e5-103">สร้างและอัพเดตรายละเอียดการส่งคืนและการขอคืนเงิน สำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="163e5-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]


## <a name="overview"></a><span data-ttu-id="163e5-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="163e5-104">Overview</span></span>

<span data-ttu-id="163e5-105">นโยบายการส่งคืนช่องทางใน Dynamics 365 Commerce ทำให้ผู้ค้าปลีกสามารถตั้งค่าบังคับ ที่สามารถใช้ในการประมวลผลการส่งคืนบนอุปกรณ์การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="163e5-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="163e5-106">หัวข้อนี้อธิบายขั้นตอนการตั้งค่านโยบายการส่งคืนและการขอคืนเงินสำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="163e5-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="163e5-107">ตอนนี้ขอบเขตของนโยบายจำกัดอยู่แค่การตั้งค่าการชำระเงินที่สามารถใช้ได้สำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="163e5-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="163e5-108">รายการ "อนุญาต" ขึ้นอยู่กับวิธีการชำระเงินที่ใช้เพื่อทำการซื้อ</span><span class="sxs-lookup"><span data-stu-id="163e5-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="163e5-109">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="163e5-109">For example:</span></span>

- <span data-ttu-id="163e5-110">ถ้ามีการซื้อโดยใช้บัตรของขวัญ นโยบายร้านค้าคือการประมวลผลการขอคืนเงินโดยให้บัตรของขวัญใหม่หรือให้เครดิตของร้านค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="163e5-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="163e5-111">ถ้าเป็นขายโดยใช้เงินสด ตัวเลือกที่ได้รับอนุญาตสำหรับการขอคืนเงินเป็นเงินสด บัตรของขวัญ และบัญชีลูกค้าแต่ไม่ใช่บัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="163e5-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="163e5-112">เปิดใช้งานนโยบายการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="163e5-112">Enable return policy</span></span>

<span data-ttu-id="163e5-113">เมื่อต้องการเปิดใช้งานฟังก์ชันนโยบายการส่งคืนช่องทาง ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="163e5-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="163e5-114">ไปยังพื้นที่ทำงาน **การจัดการคุณลักษณะ** ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="163e5-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="163e5-115">ค้นหาคุณลักษณะ **เปิดใช้งานนโยบายการส่งคืนช่องทาง** ในรายการของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="163e5-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="163e5-116">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="163e5-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="163e5-117">ตั้งค่าคอนฟิกนโยบายการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="163e5-117">Configure return policy</span></span>

<span data-ttu-id="163e5-118">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกนโยบายการส่งคืนสินค้า สำหรับร้านค้าปลีกหรือช่องทางการขายปลีกออนไลน์</span><span class="sxs-lookup"><span data-stu-id="163e5-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="163e5-119">ไปที่ **Retail และ Commerce** \> **ตั้งค่าช่องทาง** \> **ส่งคืนสินค้า** \> **นโยบายการส่งคืนช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="163e5-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="163e5-120">เลือก **สร้าง** เพื่อสร้างแม่แบบใหม่ของนโยบายการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="163e5-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="163e5-121">เมื่อต้องการใช้เท็มเพลตที่มีอยู่ ให้เลือกเท็มเพลตในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="163e5-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="163e5-122">สำหรับแม่แบบใหม่ให้เพิ่มชื่อและคำอธิบายที่จะช่วยคุณในการระบุนโยบายเมื่อมีการนำไปใช้กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="163e5-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="163e5-123">![เพิ่มนโยบายการส่งคืนใหม่](media/Return-policy-page1.png "เพิ่มนโยบายการส่งคืนใหม่")</span><span class="sxs-lookup"><span data-stu-id="163e5-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="163e5-124">ในส่วน **วิธีการชำระเงินที่ได้รับอนุญาต** ให้กำหนดการชำระเงินคืนที่ **ได้รับอนุญาต** ซึ่งเกี่ยวข้องกับวิธีการชำระเงินแต่ละวิธี</span><span class="sxs-lookup"><span data-stu-id="163e5-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="163e5-125">![เพิ่มวิธีการชำระเงิน](media/Return-policy-page2.PNG "การตั้งค่าวิธีการชำระเงินสำหรับชนิดการชำระเงิน")</span><span class="sxs-lookup"><span data-stu-id="163e5-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="163e5-126">วิธีการชำระเงินจะมาจากวิธีการชำระเงินที่ตั้งค่าไว้สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="163e5-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="163e5-127">การเพิ่มชนิดการชำระเงินคืนสำหรับการชำระเงินที่ได้รับอนุญาตสำหรับวิธีการชำระเงินที่ใช้ในแต่ละรายการ จะช่วยให้คุณสามารถทำการส่งคืนไปยังชนิดการชำระเงินที่ได้รับอนุญาตได้</span><span class="sxs-lookup"><span data-stu-id="163e5-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="163e5-128">เชื่อมโยงแม่แบบนโยบายการส่งคืนกับร้านค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="163e5-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="163e5-129">เลือก **เพิ่ม** ในแท็บ **ช่องทางการขายปลีก** และเชื่อมโยงช่องทางที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="163e5-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="163e5-130">ในกล่องโต้ตอบ **เลือกโหนดองค์กร** เลือกร้านค้า ภูมิภาค และองค์กรที่ควรเชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="163e5-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="163e5-131">แม่แบบนโยบายการส่งคืนเพียงหนึ่งแม่แบบเท่านั้นที่สามารถถูกเชื่อมโยงกับแต่ละร้านค้าได้</span><span class="sxs-lookup"><span data-stu-id="163e5-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="163e5-132">ใช้ปุ่มลูกศรเพื่อเลือกร้านค้า ภูมิภาค หรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="163e5-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="163e5-133">วันที่มีผลบังคับใช้ของนโยบายจะเป็นวันที่ที่นโยบายจะใช้กับช่องทาง และมีช่องทางงานทำงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="163e5-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="163e5-134">![กล่องโต้ตอบเลือกโหนดองค์กร](media/Return-policy-page3.PNG "กล่องโต้ตอบเลือกโหนดองค์กร")</span><span class="sxs-lookup"><span data-stu-id="163e5-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="163e5-135">บนหน้า **กำหนดการกระจาย** ให้รันงาน **1070** เพื่อทำให้นโยบายการส่งคืนช่องทางพร้อมใช้งานสำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="163e5-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="163e5-136">แสดงตัวอย่างนโยบายการส่งคืนช่องทางใน POS</span><span class="sxs-lookup"><span data-stu-id="163e5-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="163e5-137">ทำตามขั้นตอนในหนึ่งในตัวอย่างต่อไปนี้ เพื่อดูชนิดการชำระเงินคืนที่ได้รับอนุญาตใน POS</span><span class="sxs-lookup"><span data-stu-id="163e5-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="163e5-138">ลงชื่อเข้าใช้สู่ POS ในฐานะแคชเชียร์หรือผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="163e5-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="163e5-139">ภายใต้ **ลิ้นชักและกะ** ให้เลือก **แสดงสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="163e5-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="163e5-140">เลือกธุรกรรมที่เป็นส่วนหนึ่งของการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="163e5-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="163e5-141">เลือกสินค้าที่จะขอคืนเงินแล้วเลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="163e5-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="163e5-142">ถ้าการชำระเงินของการชำระเงินที่เลือกอยู่ในรายการที่อนุญาตของชนิดการชำระเงินคืน แคชเชียร์จะสามารถทำธุรกรรมให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="163e5-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="163e5-143">ถ้าวิธีการชำระเงินของการชำระเงินที่เลือกไม่ได้รับอนุญาต ข้อความแสดงข้อผิดพลาดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="163e5-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="163e5-144">เลือก **ยอดเงินที่ต้องชำระ** เพื่อแสดงรายการของชนิดการชำระเงินคืนที่ได้รับอนุญาตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="163e5-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="163e5-145">หรือ</span><span class="sxs-lookup"><span data-stu-id="163e5-145">-or-</span></span>

1. <span data-ttu-id="163e5-146">ลงชื่อเข้าใช้สู่ POS ในฐานะแคชเชียร์หรือผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="163e5-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="163e5-147">เลือก **ธุรกรรมการส่งคืน** และป้อนรหัสการรับสินค้าโดยใช้การสแกนบาร์โค้ดหรือด้วยการป้อนข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="163e5-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="163e5-148">เลือกธุรกรรมที่เป็นส่วนหนึ่งของการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="163e5-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="163e5-149">เลือกสินค้าที่จะขอคืนเงินแล้วเลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="163e5-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="163e5-150">ถ้าการชำระเงินของการชำระเงินที่เลือกอยู่ในรายการที่อนุญาตของชนิดการชำระเงินคืน แคชเชียร์จะสามารถทำธุรกรรมให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="163e5-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="163e5-151">ถ้าวิธีการชำระเงินของการชำระเงินที่เลือกไม่ได้รับอนุญาต ข้อความแสดงข้อผิดพลาดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="163e5-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="163e5-152">เลือก **ยอดเงินที่ต้องชำระ** เพื่อแสดงรายการของชนิดการชำระเงินคืนที่ได้รับอนุญาตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="163e5-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="163e5-153">![ไม่อนุญาตให้คืนเงิน](media/Return-policy-page6.png "ประเภทการคืนเงินไม่ได้รับอนุญาต")</span><span class="sxs-lookup"><span data-stu-id="163e5-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="163e5-154">![รายการวิธีการชำระเงิน](media/Return-policy-page5.PNG "ประเภทการคืนเงินได้รับอนุญาต")</span><span class="sxs-lookup"><span data-stu-id="163e5-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
