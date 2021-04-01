---
title: การวิเคราะห์ข้อบกพร่องของสินทรัพย์
description: หัวข้อนี้จะอธิบายถึงการวิเคราะห์ข้อบกพร่องของสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f4d7b4a92486287027cba79c43ca5933cce42a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253865"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="39902-103">การวิเคราะห์ข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="39902-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="39902-104">ในการจัดการสินทรัพย์ คุณสามารถวิเคราะห์การลงทะเบียนความผิดพลาดของสินทรัพย์เพื่อดูภาพรวมของจำนวนความบกพร่องทั้งหมดที่ลงทะเบียนไว้ในระหว่างรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="39902-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="39902-105">การลงทะเบียนความผิดพลาดสามารถวิเคราะห์จากมุมมองที่แตกต่างกันได้ ตัวอย่างเช่น เมื่อเน้นไปที่สินทรัพย์ ชนิดสินทรัพย์ ตำแหน่งที่ทำงาน อาการผิดปกติ หรือชนิดข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="39902-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="39902-106">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **การวิเคราะห์ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="39902-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="39902-107">ในกล่องโต้ตอบ **การคำนวณการวิเคราะห์ความบกพร่องของสินทรัพย์** คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการความบกพร่องของสินทรัพย์เกี่ยวข้องกับตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="39902-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="39902-108">ตัวอย่างเช่น หากคุณใส่หมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ รายการสินทรัพย์ทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุด ดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="39902-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="39902-109">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการข้อบกพร่องของสินทรัพย์ทั้งหมดบนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="39902-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="39902-110">ถ้าคุณต้องการจำกัดการค้นหา คุณสามารถเลือกสินทรัพย์เฉพาะ วันที่บกพร่อง สาเหตุของความบกพร่อง และการแก้ไขความผิดพลาดบนแท็บด่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="39902-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="39902-111">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="39902-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="39902-112">บนแท็บ **การวิเคราะห์ความผิดพลาดของสินทรัพย์** คลิกปุ่มหนึ่งปุ่มขึ้นไปใน **กลุ่มโดย...** เพื่อแสดงระดับของรายละเอียดที่คุณต้องการดู</span><span class="sxs-lookup"><span data-stu-id="39902-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="39902-113">ปุ่มที่เปิดใช้งานจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="39902-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="39902-114">เรียกใช้หรือยกเลิกการเรียกใช้ปุ่มโดยการคลิกที่ปุ่ม</span><span class="sxs-lookup"><span data-stu-id="39902-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="39902-115">คลิก **อัพเดตการคำนวณ** เพื่อแสดงสิ่งที่คุณเลือกไว้บนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="39902-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="39902-116">ทุกครั้งที่คุณเปิดใช้งานหรือปิดใช้งานปุ่ม **กลุ่มโดย** โปรดอย่าลืมคลิกปุ่ม **อัพเดตการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="39902-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="39902-117">การทำเช่นนี้จำเป็น เนื่องจากจะมีการประมวลผลข้อมูลจำนวนมากเมื่อคุณกำลังคำนวณความน่าจะเป็นของความผิดพลาดอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="39902-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="39902-118">ตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="39902-118">Examples</span></span>

<span data-ttu-id="39902-119">การวิเคราะห์การลงทะเบียนความผิดพลาดทำได้หลายวิธี</span><span class="sxs-lookup"><span data-stu-id="39902-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="39902-120">ส่วนนี้จะให้ตัวอย่าง 5 ตัวอย่างในการเลือกข้อมูลที่แตกต่างกันจะสามารถให้ข้อมูลเชิงลึกและรายละเอียดเพิ่มเติมเมื่อวิเคราะห์การลงทะเบียนความผิดพลาดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="39902-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="39902-121">จัดกลุ่มตามอาการ</span><span class="sxs-lookup"><span data-stu-id="39902-121">Group by symptoms</span></span>

<span data-ttu-id="39902-122">ในหน้าจอด้านล่าง มีการเลือกปุ่ม **อาการ** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="39902-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="39902-123">มีการลงทะเบียนข้อบกพร่องเกี่ยวกับอาการผิดปกติสามประการ: "อากาศรั่วไหล", "ฟิวส์ไหม้" และ "อุปกรณ์ติดค้าง"</span><span class="sxs-lookup"><span data-stu-id="39902-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="39902-124">ในคอลัมน์ **% ความน่าจะเป็น** เปอร์เซ็นต์ทั้งหมดจะเพิ่มถึง 100%</span><span class="sxs-lookup"><span data-stu-id="39902-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="39902-125">ความน่าจะเป็นขึ้นอยู่กับการลงทะเบียน **อาการ** ทั้งหมดในการวิเคราะห์ข้อบกพร่องนี้</span><span class="sxs-lookup"><span data-stu-id="39902-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![รูปที่ 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="39902-127">จัดกลุ่มตามอาการและรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="39902-127">Group by symptoms and time period</span></span>

<span data-ttu-id="39902-128">ในภาพหน้าจอด้านล่าง **ปี** และ **เดือน** จะถูกเพิ่มเพื่อแสดงวิธีการที่คุณสามารถดูการลงทะเบียนข้อบกพร่องระหว่างรอบระยะเวลาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="39902-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="39902-129">ขณะนี้อาการของความผิดปกติแสดงเป็นการลงทะเบียนต่อปี/เดือน</span><span class="sxs-lookup"><span data-stu-id="39902-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="39902-130">ในคอลัมน์ **% ความน่าจะเป็น** ถ้าคุณเพิ่มเปอร์เซ็นต์ทั้งหมดสำหรับแต่ละเดือน จะเพิ่มได้ถึง 100%</span><span class="sxs-lookup"><span data-stu-id="39902-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="39902-131">ความน่าจะเป็นขึ้นอยู่กับการลงทะเบียน **อาการ** ในการวิเคราะห์ข้อบกพร่องนี้</span><span class="sxs-lookup"><span data-stu-id="39902-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="39902-132">ถ้าคุณมีรายการในสินทรัพย์จำนวนมาก แต่มีเปอร์เซ็นต์ขนาดใหญ่ที่โดดเด่นในรายการ นั่นจะเป็นตัวบ่งชี้ถึงอาการของความผิดพลาด เพื่อตรวจสอบอย่างใกล้ชิดขึ้น เพื่อหาวิธีจำกัดจำนวนการลงทะเบียนสำหรับอาการที่บกพร่องดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="39902-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![รูปที่ 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="39902-134">จัดกลุ่มตามอาการและสินทรัพย์หลายรายการ</span><span class="sxs-lookup"><span data-stu-id="39902-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="39902-135">การรวมกันของสินทรัพย์และชนิดสินทรัพย์จะถูกใช้เป็นข้อมูลพื้นฐานสำหรับการคำนวณที่แสดงอยู่ในภาพหน้าจอสามภาพด้านล่างนี้ ซึ่งจะเพิ่มขึ้นในระดับรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="39902-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="39902-136">โดยทั่วไป ปุ่มในกลุ่มหน้าต่างการดำเนินการ **จัดกลุ่มตามวันที่** **จัดกลุ่มตามสินทรัพย์** **จัดกลุ่มตามตำแหน่งที่ทำงาน** รวมทั้งปุ่ม **ข้อผิดพลาด** (รหัสข้อผิดพลาด) จะมีรอบระยะเวลาหรือความสัมพันธ์ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="39902-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="39902-137">ปุ่ม **อาการ** **พื้นที่** **ชนิด** **สาเหตุ** และ **การแก้ไข** ถูกจัดการเพื่อใช้ในการจัดการข้อบกพร่อง เพื่อวิเคราะห์การลงทะเบียนความผิดพลาดของสินทรัพย์ และพื้นที่ปัญหาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="39902-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="39902-138">**จัดกลุ่มตามอาการ สินทรัพย์และชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="39902-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="39902-139">ในภาพหน้าจอด้านล่าง **สินทรัพย์** และ **ชนิดสินทรัพย์** ถูกเพิ่มเข้ามาเพื่อให้รายละเอียดเพิ่มเติมเกี่ยวกับการลงทะเบียนความบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="39902-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="39902-140">ขณะนี้อาการผิดปกติถูกแบ่งตามการรวมของ **สินทรัพย์** / **ชนิดสินทรัพย์** / **อาการ**</span><span class="sxs-lookup"><span data-stu-id="39902-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="39902-141">ในคอลัมน์ **% ความน่าจะเป็น** ถ้าคุณเพิ่มเปอร์เซ็นต์ทั้งหมดสำหรับการรวมกันของ **สินทรัพย์t** / **ชนิดสินทรัพย์** / **อาการ** แต่ละส่วนจะเพิ่มได้ถึง 100%</span><span class="sxs-lookup"><span data-stu-id="39902-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="39902-142">ความน่าจะเป็นขึ้นอยู่กับการลงทะเบียน **อาการ** ทั้งหมดในการวิเคราะห์ข้อบกพร่องนี้</span><span class="sxs-lookup"><span data-stu-id="39902-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="39902-143">ถ้าคุณมีรายการในสินทรัพย์จำนวนมาก แต่มีเปอร์เซ็นต์ขนาดใหญ่ที่โดดเด่นในรายการ นั่นจะเป็นตัวบ่งชี้ถึงอาการของความผิดพลาด เพื่อตรวจสอบอย่างใกล้ชิดขึ้น เพื่อหาวิธีจำกัดจำนวนการลงทะเบียนสำหรับอาการที่บกพร่องดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="39902-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![รูปที่ 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="39902-145">**จัดกลุ่มตาม 2 อาการ สินทรัพย์และชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="39902-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="39902-146">ในภาพหน้าจอด้านล่าง **พื้นที่** ถูกเพิ่มไปยัง **อาการ** **สินทรัพย์** และ **ชนิดสินทรัพย์** ถูกเพิ่มเข้ามาเพื่อให้รายละเอียดเพิ่มเติมเกี่ยวกับการลงทะเบียนความบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="39902-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="39902-147">ในคอลัมน์ **% ความน่าจะเป็น** ถ้าคุณเพิ่มเปอร์เซ็นต์ทั้งหมดสำหรับการรวมกันของ **สินทรัพย์** / **ชนิดสินทรัพย์** / **อาการ** ในสินทรัพย์ แต่ละส่วนจะเพิ่มได้ถึง 100%</span><span class="sxs-lookup"><span data-stu-id="39902-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="39902-148">ความน่าจะเป็นขึ้นอยู่กับการรวมกันของ **อาการ** และ **พื้นที่** ในการวิเคราะห์ข้อบกพร่องนี้</span><span class="sxs-lookup"><span data-stu-id="39902-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="39902-149">ถ้าคุณมีรายการในสินทรัพย์จำนวนมาก แต่มีเปอร์เซ็นต์ขนาดใหญ่ที่โดดเด่นในรายการ นั่นจะเป็นตัวบ่งชี้ถึงพื้นที่ของความผิดพลาด เพื่อตรวจสอบอย่างใกล้ชิดขึ้นและหาวิธีจำกัดจำนวนการลงทะเบียนสำหรับพื้นที่ที่บกพร่องดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="39902-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![รูปที่ 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="39902-151">**จัดกลุ่มตาม 3 อาการ สินทรัพย์และชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="39902-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="39902-152">ในภาพหน้าจอด้านล่าง **ชนิด** ถูกเพิ่มเข้ามา และการคำนวณรายละเอียดที่มากที่สุดในตัวอย่างนี้จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="39902-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="39902-153">ในคอลัมน์ **% ความน่าจะเป็น** ถ้าคุณเพิ่มเปอร์เซ็นต์ทั้งหมดสำหรับการรวมกันของ **สินทรัพย์** / **ชนิดสินทรัพย์** / **อาการ** ในสินทรัพย์ แต่ละส่วนจะเพิ่มได้ถึง 100%</span><span class="sxs-lookup"><span data-stu-id="39902-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="39902-154">ความน่าจะเป็นขึ้นอยู่กับการรวมกันของ **อาการ** **พื้นที่** and **ชนิด** ในการวิเคราะห์ข้อบกพร่องนี้</span><span class="sxs-lookup"><span data-stu-id="39902-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="39902-155">ถ้าคุณมีรายการในสินทรัพย์จำนวนมาก แต่มีเปอร์เซ็นต์ขนาดใหญ่ที่โดดเด่นในรายการ นั่นจะเป็นตัวบ่งชี้ถึงชนิดของความบกพร่อง เพื่อตรวจสอบอย่างใกล้ชิดขึ้นและหาวิธีจำกัดจำนวนการลงทะเบียนสำหรับชนิดที่บกพร่องดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="39902-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![รูปที่ 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="39902-157">สำหรับภาพรวมของการลงทะเบียนความผิดพลาดทั้งหมดที่สร้างขึ้นในใบสั่งงานและคำขอการบำรุงรักษา คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **ข้อบกพร่องของสินทรัพย์** > **ข้อบกพร่องของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="39902-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="39902-158">บนหน้า **ข้อบกพร่องของสินทรัพย์** ให้เลือกการลงทะเบียนข้อบกพร่องของสินทรัพย์ที่และขยายหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** เพื่อดูข้อมูลเกี่ยวกับใบสั่งงานหรือคำขอการบำรุงรักษาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="39902-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]