---
title: สร้างรายงานปริมาณการใช้
description: หัวข้อนี้อธิบายวิธีการสร้างรายงานปริมาณการใช้ในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8add0602e0ebe7a5c0cf2c76de6fa2f4f21a2f72
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837932"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="1b173-103">สร้างรายงานปริมาณการใช้</span><span class="sxs-lookup"><span data-stu-id="1b173-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1b173-104">เมื่อคุณสร้าง และการลงทะเบียนลงรายการบัญชีปริมาณการใช้บนใบสั่งงานในการจัดการสินทรัพย์ รายงานทั้งสองพร้อมใช้งานเพื่อการเเสดงรายละเอียดปริมาณ</span><span class="sxs-lookup"><span data-stu-id="1b173-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="1b173-105">รายงานปริมาณการใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1b173-105">Asset consumption report</span></span>

<span data-ttu-id="1b173-106">เมื่อคุณลงรายการบัญชีปริมาณการใช้บนใบสั่งงาน คุณสามารถพิมพ์รายงานปริมาณการใช้สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1b173-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="1b173-107">รายงานจะแสดงชั่วโมง ต้นทุนชั่วโมง ต้นทุนสินค้า และค่าใช้จ่ายที่ลงรายการบัญชีไว้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1b173-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="1b173-108">คลิก **การจัดการสินทรัพย์** > **รายงาน** > **สินทรัพย์** > **ปริมาณการใช้สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="1b173-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="1b173-109">ในกล่องโต้ตอบ **ปริมาณการใช้สินทรัพย์** เลือกพารามิเตอร์ และระดับรายละเอียดที่คุณต้องการดูโดยการเลือก **ใช่** บนปุ่มสลับที่เกี่ยวข้อง และแทรกระดับตำเเหน่งที่ทำงานในส่วน **เเสดง**</span><span class="sxs-lookup"><span data-stu-id="1b173-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="1b173-110">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการสินทรัพย์เกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="1b173-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="1b173-111">ตัวอย่างเช่น หากคุณป้อนหมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างตำเเหน่งที่ทำงานหลายระดับ สินทรัพย์ทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุดดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="1b173-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="1b173-112">หากคุณป้อนหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงสินทรัพย์ทั้งหมดบนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1b173-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="1b173-113">เลือก **ใช่** ในปุ่มสลับ **ผลรวมบนสินทรัพย์ย่อยทั้งหมด** เพื่อดูผลรวมของสินทรัพย์ย่อยแต่ละรายการในรายงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="1b173-114">เลือกช่วงวันที่ในส่วน **วันที่**</span><span class="sxs-lookup"><span data-stu-id="1b173-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="1b173-115">บนแท็บด่วน **ปลายทาง** เลือกถ้าคุณต้องการแสดงรายงานบนหน้าจอ ให้พิมพ์ หรือบันทึกเป็นไฟล์ หรืออีเมล</span><span class="sxs-lookup"><span data-stu-id="1b173-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="1b173-116">ถ้าจำเป็น คุณสามารถเลือกสินทรัพย์เฉพาะที่จะแสดงในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="1b173-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="1b173-117">บนเเท็บด่วน **เรกคอร์ดที่จะรวม** คลิก **ตัวกรอง** เเละเพิ่มสินทรัพย์ที่คุณต้องการรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="1b173-118">คลิก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="1b173-119">รายงานปริมาณการใช้ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-119">Work order consumption report</span></span>

<span data-ttu-id="1b173-120">เมื่อคุณลงรายการบัญชีปริมาณการใช้บนใบสั่งงาน คุณสามารถพิมพ์รายงานปริมาณการใช้ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="1b173-121">รายงานจะแสดงชั่วโมง ต้นทุนชั่วโมง ต้นทุนสินค้า และค่าใช้จ่ายที่ลงรายการบัญชีไว้ในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="1b173-122">คลิก **การจัดการสินทรัพย์** > **รายงาน** > **ใบสั่งงาน** > **ปริมาณการใช้ใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="1b173-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="1b173-123">ในกล่องโต้ตอบ **ปริมาณการใช้ใบสั่งงาน** เลือกพารามิเตอร์ที่คุณต้องการรวมไว้ในรายงานโดยเลือก **ใช่** บนปุ่มสลับที่เกี่ยวข้องในส่วน **เเสดง**</span><span class="sxs-lookup"><span data-stu-id="1b173-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="1b173-124">เลือกช่วงวันที่ในส่วน **วันที่**</span><span class="sxs-lookup"><span data-stu-id="1b173-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="1b173-125">บนแท็บด่วน **ปลายทาง** เลือกถ้าคุณต้องการแสดงรายงานบนหน้าจอ ให้พิมพ์ หรือบันทึกเป็นไฟล์ หรืออีเมล</span><span class="sxs-lookup"><span data-stu-id="1b173-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="1b173-126">ถ้าจำเป็น คุณสามารถเลือกใบสั่งงานเฉพาะที่จะแสดงในรายงานได้</span><span class="sxs-lookup"><span data-stu-id="1b173-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="1b173-127">บนเเท็บด่วน **เรกคอร์ดที่จะรวม** คลิก **ตัวกรอง** เเละเพิ่มใบสั่งงานที่คุณต้องการรวมไว้ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="1b173-128">คลิก **ตกลง** เพื่อสร้างรายงาน</span><span class="sxs-lookup"><span data-stu-id="1b173-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="1b173-129">นอกจากนี้คุณยังสามารถสร้าง [รายงานใบสั่งงาน](../work-orders/work-order-report.md) ซึ่งประกอบด้วยรายละเอียดของใบสั่งงานเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1b173-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]