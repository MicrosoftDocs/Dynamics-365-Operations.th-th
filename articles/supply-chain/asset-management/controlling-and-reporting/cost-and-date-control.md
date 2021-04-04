---
title: การควบคุมต้นทุนและวันที่
description: หัวข้อนี้จะอธิบายถึงการควบคุมต้นทุน และวันที่ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7072cb8c3f76be5869239aa0acab6cf3ff268e32
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253793"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="3bc51-103">การควบคุมต้นทุนและวันที่</span><span class="sxs-lookup"><span data-stu-id="3bc51-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3bc51-104">ในการจัดการสินทรัพย์ คุณสามารถคำนวณต้นทุนเพื่อดูภาพรวมของต้นทุนจริงเปรียบเทียบกับต้นทุนตามงบประมาณกับสินทรัพย์ ตำเเหน่งที่ทำงาน และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="3bc51-105">ต้นทุนจริงจะขึ้นอยู่กับธุรกรรมที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="3bc51-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="3bc51-106">นอกจากนี้คุณยังสามารถทำการคำนวณวันที่ได้ ถ้าคุณต้องการเปรียบเทียบวันที่เริ่มต้น และวันที่สิ้นสุดที่จัดกำหนดการไว้จนถึงวันที่เริ่มต้น และวันที่สิ้นสุดจริงของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="3bc51-107">การควบคุมต้นทุนสำหรับสินทรัพย์ ตำเเหน่งที่ทำงาน และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="3bc51-108">การคำนวณสำหรับสินทรัพย์ ตำเเหน่งที่ทำงาน และใบสั่งงานที่เกือบจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="3bc51-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="3bc51-109">ความแตกต่างเพียงอย่างเดียวคือสำหรับสินทรัพย์ และตำเเหน่งที่ทำงาน คุณยังสามารถรวมสินทรัพย์ย่อย และที่ตั้งย่อยไว้ในการคำนวณของคุณได้</span><span class="sxs-lookup"><span data-stu-id="3bc51-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="3bc51-110">วันที่ทำธุรกรรมคือวันที่การลงทะเบียนถูกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="3bc51-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="3bc51-111">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **การควบคุมต้นทุนของสินทรัพย์** หรือ **การควบคุมต้นทุนของตำแหน่งที่ทำงาน** หรือ **การจัดการสินทรัพย์** > **การสอบถาม** > **ใบสั่งงาน** > **การควบคุมต้นทุนใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="3bc51-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="3bc51-112">ในกล่องโต้ตอบ **การควบคุมต้นทุนของสินทรัพย์** / **การควบคุมต้นทุนของตำเเหน่งที่ทำงาน** / **ควบคุมต้นทุนของใบสั่งงาน** เลือกช่วงเวลาที่จะใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="3bc51-113">หากจำเป็น ให้เลือกเซ็ตมิติทางการเงินให้รวมไว้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="3bc51-114">เลือก "ใช่" บนปุ่มสลับ **ข้ามเลขศูนย์** ถ้าคุณไม่ต้องการแสดงผลลัพธ์ที่มีต้นทุนเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="3bc51-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="3bc51-115">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการควบคุมต้นทุนเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="3bc51-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="3bc51-116">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีลำดับตำเเหน่งที่ทำงานหลายระดับ การควบคุมต้นทุนของรายการทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุด ดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานอยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="3bc51-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="3bc51-117">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการควบคุมต้นทุนทั้งหมด บนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3bc51-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="3bc51-118">เลือก "ใช่" บนปุ่มสลับ **แสดงต้นทุนผูกมัด** ที่กำหนดให้เปิดค้างไว้ถ้าคุณต้องการรวมคอลัมน์นั้นไว้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="3bc51-119">เลือก "ใช่" บนปุ่มสลับ **รวมของสินทรัพย์ย่อย** เพื่อแสดงต้นทุนที่เกี่ยวข้องกับสินทรัพย์ย่อยเป็นรายการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="3bc51-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="3bc51-120">ถ้าคุณต้องการจำกัดการค้นหา คุณสามารถเลือกสินทรัพย์เฉพาะ ตำเเหน่งที่ทำงาน ใบสั่งงาน บนเเท็บด่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="3bc51-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="3bc51-121">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="3bc51-122">ตัวเลขด้านล่างแสดงตัวอย่างของ **กล่องโต้ตอบ** การควบคุมต้นทุนสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3bc51-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![กล่องโต้ตอบการควบคุมต้นทุนสินทรัพย์](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="3bc51-124">บนเพจ **การควบคุมต้นทุนของสินทรัพย์** คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3bc51-125">ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="3bc51-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="3bc51-126">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="3bc51-127">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3bc51-127">Example</span></span>

<span data-ttu-id="3bc51-128">ภาพหน้าจอด้านล่างแสดงตัวอย่างของผลการคำนวณ **การควบคุมต้นทุนสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="3bc51-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="3bc51-129">ฟิลด์ **งบประมาณเดิม** แสดงต้นทุนตามงบประมาณจากการคาดการณ์ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="3bc51-130">ฟิลด์ **ต้นทุนผูกมัด** เเสดงจำนวนทั้งหมดของค่าใช้จ่ายที่นิติบุคคลได้กำหนดการชำระเอง</span><span class="sxs-lookup"><span data-stu-id="3bc51-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="3bc51-131">ฟิลด์ **ต้นทุนผูกมัดที่เปิดอยู่** จะแสดงข้อผูกมัดเพื่อชำระสำหรับสินค้า ชั่วโมง และบริการที่คุณได้สั่งหรือได้รับแล้วแต่ยังไม่ได้ชำระ</span><span class="sxs-lookup"><span data-stu-id="3bc51-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="3bc51-132">ฟิลด์ **ต้นทุนจริง** จะแสดงต้นทุนที่เกี่ยวข้องหลังจากการลงทะเบียนปริมาณการใช้มีการลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="3bc51-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![ตัวอย่างผลลัพธ์ของการคำนวณในการควบคุมต้นทุนของสินทรัพย์](media/02-controlling-and-reporting.png)

<span data-ttu-id="3bc51-134">อีกวิธีหนึ่งในการทำการคำนวณต้นทุนเป็นการเลือกทรัพย์สินหลายรายการใน **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="3bc51-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="3bc51-135">จากนั้น ให้คุณคลิกปุ่ม **การควบคุมต้นทุน** บนแท็บ **ทั่วไป** ในกล่องโต้ตอบ **การควบคุมต้นทุนสินทรัพย์** สินทรัพย์ที่ถูกเลือกจะถูกแทรกโดยอัตโนมัติในฟิลด์ **สินทรัพย์** บน **เรกคอร์ดเพื่อรวม** แท็บด่วน</span><span class="sxs-lookup"><span data-stu-id="3bc51-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="3bc51-136">คลิก **ตกลง** และการคำนวณต้นทุนสำหรับสินทรัพย์ที่เลือกจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="3bc51-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="3bc51-137">กระบวนงานเดียวกันสามารถใช้สำหรับตำเเหน่งที่ทำงานใน **ตำเเหน่งที่ทำงานทั้งหมด** หรือ **ตำเเหน่งที่ทำงานที่ใช้งานอยู่** เเละสำหรับใบสั่งงานใน **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="3bc51-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="3bc51-138">การควบคุมวันที่ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-138">Work order date control</span></span>

<span data-ttu-id="3bc51-139">ใช้หน้านี้เพื่อเรียกดูภาพรวมของวันที่เริ่มต้น และวันที่สิ้นสุดที่คาดไว้ เปรียบเทียบกับวันที่เริ่มต้น และวันที่สิ้นสุดจริงของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="3bc51-140">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ใบสั่งงาน** > **ใบสั่งงานการควบคุมวันที่**</span><span class="sxs-lookup"><span data-stu-id="3bc51-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="3bc51-141">คลิก **คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="3bc51-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="3bc51-142">เลือกตำเเหน่งที่ทำงานในฟิลด์ **ตำแหน่งที่ทำงาน** </span><span class="sxs-lookup"><span data-stu-id="3bc51-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="3bc51-143">แทรกช่วงเวลาที่คุณต้องการทำการคำนวณในฟิลด์ **วันที่เริ่มต้น** เเละ **วันที่สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="3bc51-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="3bc51-144">ใบสั่งงานทั้งหมดที่คาดว่ามีวันที่เริ่มต้นอยู่ภายในช่วงเวลาที่กำหนดจะถูกร่วม</span><span class="sxs-lookup"><span data-stu-id="3bc51-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="3bc51-145">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3bc51-145">Click **OK**.</span></span>

6. <span data-ttu-id="3bc51-146">คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="3bc51-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3bc51-147">ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="3bc51-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="3bc51-148">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="3bc51-149">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="3bc51-149">Example</span></span>

<span data-ttu-id="3bc51-150">ภาพหน้าจอด้านล่างแสดงตัวอย่างของผลการคำนวณใน **ใบสั่งงานการควบคุมวันที่**</span><span class="sxs-lookup"><span data-stu-id="3bc51-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="3bc51-151">ฟิลด์ **การเริ่มต้นล่าช้าโดยเฉลี่ย** แสดงผลต่างระหว่างวันที่เริ่มต้นตามกำหนดการสำหรับใบสั่งงานที่เปรียบเทียบกับวันที่เริ่มต้นจริง</span><span class="sxs-lookup"><span data-stu-id="3bc51-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="3bc51-152">ตัวอย่างเช่น ถ้าวันที่เริ่มต้นจริงคือสองวันก่อนวันที่เริ่มต้นตามกำหนด "-2" จะเเสดงขึ้นในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="3bc51-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="3bc51-153">ฟิลด์ **การสิ้นสุดล่าช้าโดยเฉลี่ย** แสดงผลต่างระหว่างวันที่สิ้นสุดตามกำหนดการสำหรับใบสั่งงานที่เปรียบเทียบกับวันที่สิ้นสุดจริง</span><span class="sxs-lookup"><span data-stu-id="3bc51-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="3bc51-154">ตัวอย่างเช่น ถ้าวันที่สิ้นสุดจริงคือสามวันหลังวันที่สิ้นสุดตามกำหนด "3" จะเเสดงขึ้นในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="3bc51-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="3bc51-155">ฟิลด์ **การเกิดเหตุการณ์** แสดงจำนวนครั้งความเบี่ยงเบนของเวลาที่เกิดขึ้นในความสัมพันธ์ซึ่งกำหนด และวันที่เริ่มต้นจริง และจัดกำหนดการ และวันที่สิ้นสุดจริงของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3bc51-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![ตัวอย่างผลลัพธ์ของการคำนวณในการควบคุมวันที่ของใบสั่งงาน](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]