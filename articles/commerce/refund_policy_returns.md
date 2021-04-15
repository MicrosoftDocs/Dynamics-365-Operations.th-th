---
title: สร้างและอัพเดตรายละเอียดการส่งคืนและการขอคืนเงิน สำหรับช่องทาง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่านโยบายการส่งคืนและการขอคืนเงินสำหรับช่องทาง
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792086"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="c9b42-103">สร้างและอัปเดตนโยบายการส่งคืนและการขอคืนเงินสำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c9b42-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9b42-104">นโยบายการส่งคืนช่องทางใน Dynamics 365 Commerce ทำให้ผู้ค้าปลีกสามารถตั้งค่าบังคับ ที่สามารถใช้ในการประมวลผลการส่งคืนบนอุปกรณ์การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="c9b42-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="c9b42-105">หัวข้อนี้อธิบายขั้นตอนการตั้งค่านโยบายการส่งคืนและการขอคืนเงินสำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c9b42-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="c9b42-106">ตอนนี้ขอบเขตของนโยบายจำกัดอยู่แค่การตั้งค่าการชำระเงินที่สามารถใช้ได้สำหรับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c9b42-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="c9b42-107">รายการ "อนุญาต" ขึ้นอยู่กับวิธีการชำระเงินที่ใช้เพื่อทำการซื้อ</span><span class="sxs-lookup"><span data-stu-id="c9b42-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="c9b42-108">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="c9b42-108">For example:</span></span>

- <span data-ttu-id="c9b42-109">ถ้ามีการซื้อโดยใช้บัตรของขวัญ นโยบายร้านค้าคือการประมวลผลการขอคืนเงินโดยให้บัตรของขวัญใหม่หรือให้เครดิตของร้านค้าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c9b42-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="c9b42-110">ถ้าเป็นขายโดยใช้เงินสด ตัวเลือกที่ได้รับอนุญาตสำหรับการขอคืนเงินเป็นเงินสด บัตรของขวัญ และบัญชีลูกค้าแต่ไม่ใช่บัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="c9b42-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="c9b42-111">เปิดใช้งานนโยบายการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c9b42-111">Enable return policy</span></span>

<span data-ttu-id="c9b42-112">เมื่อต้องการเปิดใช้งานฟังก์ชันนโยบายการส่งคืนช่องทาง ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9b42-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="c9b42-113">ไปยังพื้นที่ทำงาน **การจัดการคุณลักษณะ** ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c9b42-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="c9b42-114">ค้นหาคุณลักษณะ **เปิดใช้งานนโยบายการส่งคืนช่องทาง** ในรายการของลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c9b42-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="c9b42-115">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="c9b42-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="c9b42-116">ตั้งค่าคอนฟิกนโยบายการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c9b42-116">Configure return policy</span></span>

<span data-ttu-id="c9b42-117">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกนโยบายการส่งคืนสินค้า สำหรับร้านค้าปลีกหรือช่องทางการขายปลีกออนไลน์</span><span class="sxs-lookup"><span data-stu-id="c9b42-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="c9b42-118">ไปที่ **Retail และ Commerce** \> **ตั้งค่าช่องทาง** \> **ส่งคืนสินค้า** \> **นโยบายการส่งคืนช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="c9b42-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="c9b42-119">เลือก **สร้าง** เพื่อสร้างแม่แบบใหม่ของนโยบายการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="c9b42-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="c9b42-120">เมื่อต้องการใช้เท็มเพลตที่มีอยู่ ให้เลือกเท็มเพลตในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="c9b42-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="c9b42-121">สำหรับแม่แบบใหม่ให้เพิ่มชื่อและคำอธิบายที่จะช่วยคุณในการระบุนโยบายเมื่อมีการนำไปใช้กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c9b42-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="c9b42-122">![เพิ่มนโยบายการส่งคืนใหม่](media/Return-policy-page1.png "เพิ่มนโยบายการส่งคืนใหม่")</span><span class="sxs-lookup"><span data-stu-id="c9b42-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="c9b42-123">ในส่วน **วิธีการชำระเงินที่ได้รับอนุญาต** ให้กำหนดการชำระเงินคืนที่ **ได้รับอนุญาต** ซึ่งเกี่ยวข้องกับวิธีการชำระเงินแต่ละวิธี</span><span class="sxs-lookup"><span data-stu-id="c9b42-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="c9b42-124">![เพิ่มวิธีการชำระเงิน](media/Return-policy-page2.PNG "การตั้งค่าวิธีการชำระเงินสำหรับชนิดการชำระเงิน")</span><span class="sxs-lookup"><span data-stu-id="c9b42-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="c9b42-125">วิธีการชำระเงินจะมาจากวิธีการชำระเงินที่ตั้งค่าไว้สำหรับองค์กร</span><span class="sxs-lookup"><span data-stu-id="c9b42-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="c9b42-126">การเพิ่มชนิดการชำระเงินคืนสำหรับการชำระเงินที่ได้รับอนุญาตสำหรับวิธีการชำระเงินที่ใช้ในแต่ละรายการ จะช่วยให้คุณสามารถทำการส่งคืนไปยังชนิดการชำระเงินที่ได้รับอนุญาตได้</span><span class="sxs-lookup"><span data-stu-id="c9b42-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="c9b42-127">เชื่อมโยงแม่แบบนโยบายการส่งคืนกับร้านค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="c9b42-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="c9b42-128">เลือก **เพิ่ม** ในแท็บ **ช่องทางการขายปลีก** และเชื่อมโยงช่องทางที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c9b42-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="c9b42-129">ในกล่องโต้ตอบ **เลือกโหนดองค์กร** เลือกร้านค้า ภูมิภาค และองค์กรที่ควรเชื่อมโยงกับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="c9b42-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="c9b42-130">แม่แบบนโยบายการส่งคืนเพียงหนึ่งแม่แบบเท่านั้นที่สามารถถูกเชื่อมโยงกับแต่ละร้านค้าได้</span><span class="sxs-lookup"><span data-stu-id="c9b42-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="c9b42-131">ใช้ปุ่มลูกศรเพื่อเลือกร้านค้า ภูมิภาค หรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="c9b42-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="c9b42-132">วันที่มีผลบังคับใช้ของนโยบายจะเป็นวันที่ที่นโยบายจะใช้กับช่องทาง และมีช่องทางงานทำงานแล้ว</span><span class="sxs-lookup"><span data-stu-id="c9b42-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="c9b42-133">![กล่องโต้ตอบเลือกโหนดองค์กร](media/Return-policy-page3.PNG "กล่องโต้ตอบเลือกโหนดองค์กร")</span><span class="sxs-lookup"><span data-stu-id="c9b42-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="c9b42-134">บนหน้า **กำหนดการกระจาย** ให้รันงาน **1070** เพื่อทำให้นโยบายการส่งคืนช่องทางพร้อมใช้งานสำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="c9b42-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="c9b42-135">แสดงตัวอย่างนโยบายการส่งคืนช่องทางใน POS</span><span class="sxs-lookup"><span data-stu-id="c9b42-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="c9b42-136">ทำตามขั้นตอนในหนึ่งในตัวอย่างต่อไปนี้ เพื่อดูชนิดการชำระเงินคืนที่ได้รับอนุญาตใน POS</span><span class="sxs-lookup"><span data-stu-id="c9b42-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="c9b42-137">ลงชื่อเข้าใช้สู่ POS ในฐานะแคชเชียร์หรือผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="c9b42-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="c9b42-138">ภายใต้ **ลิ้นชักและกะ** ให้เลือก **แสดงสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="c9b42-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="c9b42-139">เลือกธุรกรรมที่เป็นส่วนหนึ่งของการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c9b42-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="c9b42-140">เลือกสินค้าที่จะขอคืนเงินแล้วเลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c9b42-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="c9b42-141">ถ้าการชำระเงินของการชำระเงินที่เลือกอยู่ในรายการที่อนุญาตของชนิดการชำระเงินคืน แคชเชียร์จะสามารถทำธุรกรรมให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="c9b42-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="c9b42-142">ถ้าวิธีการชำระเงินของการชำระเงินที่เลือกไม่ได้รับอนุญาต ข้อความแสดงข้อผิดพลาดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c9b42-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="c9b42-143">เลือก **ยอดเงินที่ต้องชำระ** เพื่อแสดงรายการของชนิดการชำระเงินคืนที่ได้รับอนุญาตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c9b42-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="c9b42-144">หรือ</span><span class="sxs-lookup"><span data-stu-id="c9b42-144">-or-</span></span>

1. <span data-ttu-id="c9b42-145">ลงชื่อเข้าใช้สู่ POS ในฐานะแคชเชียร์หรือผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="c9b42-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="c9b42-146">เลือก **ธุรกรรมการส่งคืน** และป้อนรหัสการรับสินค้าโดยใช้การสแกนบาร์โค้ดหรือด้วยการป้อนข้อมูลด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c9b42-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="c9b42-147">เลือกธุรกรรมที่เป็นส่วนหนึ่งของการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c9b42-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="c9b42-148">เลือกสินค้าที่จะขอคืนเงินแล้วเลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c9b42-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="c9b42-149">ถ้าการชำระเงินของการชำระเงินที่เลือกอยู่ในรายการที่อนุญาตของชนิดการชำระเงินคืน แคชเชียร์จะสามารถทำธุรกรรมให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="c9b42-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="c9b42-150">ถ้าวิธีการชำระเงินของการชำระเงินที่เลือกไม่ได้รับอนุญาต ข้อความแสดงข้อผิดพลาดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c9b42-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="c9b42-151">เลือก **ยอดเงินที่ต้องชำระ** เพื่อแสดงรายการของชนิดการชำระเงินคืนที่ได้รับอนุญาตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c9b42-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="c9b42-152">![ไม่อนุญาตให้คืนเงิน](media/Return-policy-page6.png "ประเภทการคืนเงินไม่ได้รับอนุญาต")</span><span class="sxs-lookup"><span data-stu-id="c9b42-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="c9b42-153">![รายการวิธีการชำระเงิน](media/Return-policy-page5.PNG "ประเภทการคืนเงินได้รับอนุญาต")</span><span class="sxs-lookup"><span data-stu-id="c9b42-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
