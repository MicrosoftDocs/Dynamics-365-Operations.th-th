---
title: การควบคุมชั่วโมงการทำงาน
description: หัวข้อนี้จะอธิบายถึงการควบคุมชั่วโมงการทำงานในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ba1c9548ac7ad54a459f42fd9f8f20c6936f14c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216387"
---
# <a name="work-hour-control"></a><span data-ttu-id="0916b-103">การควบคุมชั่วโมงการทำงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0916b-104">ในการจัดการสินทรัพย์ คุณสามารถคำนวณชั่วโมงเพื่อดูภาพรวมของชั่วโมงจริงเปรียบเทียบกับงบประมาณชั่วโมงในสินทรัพย์ ตำเเหน่งที่ทำงาน หรือใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="0916b-105">ชั่วโมงจริงจะขึ้นอยู่กับธุรกรรมที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="0916b-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="0916b-106">การควบคุมชั่วโมงการทำงานสำหรับสินทรัพย์ ตำเเหน่งที่ทำงาน และใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="0916b-107">การคำนวณสำหรับสินทรัพย์ ตำเเหน่งที่ทำงาน และใบสั่งงานที่เกือบจะเหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="0916b-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="0916b-108">ความแตกต่างเพียงอย่างเดียวคือสำหรับสินทรัพย์ และตำเเหน่งที่ทำงาน คุณยังสามารถรวมสินทรัพย์ย่อย และที่ตั้งย่อยไว้ในการคำนวณของคุณได้</span><span class="sxs-lookup"><span data-stu-id="0916b-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="0916b-109">วันที่ทำธุรกรรมคือวันที่การลงทะเบียนถูกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="0916b-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="0916b-110">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **การควบคุมชั่วโมงของสินทรัพย์** หรือ **การควบคุมชั่วโมงของตำแหน่งที่ทำงาน** หรือ **การจัดการสินทรัพย์** > **การสอบถาม** > **ใบสั่งงาน** > **การควบคุมชั่วโมงการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="0916b-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="0916b-111">ในกล่องโต้ตอบ **การควบคุมชั่วโมงของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="0916b-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="0916b-112">ในกล่องโต้ตอบ **การควบคุมชั่วโมงของสินทรัพย์** / **การควบคุมชั่วโมงของตำเเหน่งที่ทำงาน** / **การควบคุมชั่วโมงการทำงาน** เลือกรอบระยะเวลาที่จะคำนวณใน **วันที่เริ่มต้น** เเละ **วันที่สิ้นสุด** ของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="0916b-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="0916b-113">หากจำเป็น เลือก **เซ็ตมิติทางการเงิน** รวมอยู่ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0916b-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="0916b-114">เลือก "ใช่" บนปุ่มสลับ **ข้ามเลขศูนย์** ถ้าคุณไม่ต้องการแสดงผลลัพธ์ที่มีชั่วโมงเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="0916b-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="0916b-115">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้รายการการควบคุมชั่วโมงเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="0916b-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="0916b-116">ตัวอย่างเช่น หากคุณเเทรกหมายเลข "1" ในฟิลด์ และคุณมีลำดับตำเเหน่งที่ทำงานหลายระดับ รายการการควบคุมชั่วโมงทั้งหมดสำหรับตำเเหน่งที่ทำงานจะถูกเเสดงบนระดับบนสุด ดังนั้นชั่วโมงในรายการอาจจะมีการเพิ่มจากตำเเหน่งที่ทำงานอยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="0916b-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="0916b-117">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการควบคุมชั่วโมงทั้งหมดบนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0916b-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="0916b-118">เลือก "ใช่" บนปุ่มสลับ **รวมของสินทรัพย์ย่อย** เพื่อแสดงต้นทุนที่เกี่ยวข้องกับสินทรัพย์ย่อยเป็นรายการแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="0916b-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="0916b-119">ถ้าคุณต้องการจำกัดการค้นหา คุณสามารถเลือกสินทรัพย์เฉพาะ ตำเเหน่งที่ทำงาน ใบสั่งงาน บนเเท็บด่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="0916b-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="0916b-120">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0916b-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="0916b-121">บนหน้า **การควบคุมชั่วโมงของสินทรัพย์** คลิกปุ่ม **จัดกลุ่มโดย** เพื่อแสดงระดับรายละเอียดที่จำเป็นต้องใช้ในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="0916b-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="0916b-122">ปุ่ม **จัดกลุ่มโดย** ที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="0916b-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="0916b-123">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0916b-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="0916b-124">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="0916b-124">Example</span></span>

<span data-ttu-id="0916b-125">ภาพหน้าจอด้านล่างแสดงตัวอย่างของผลการคำนวณ **การควบคุมชั่วโมงของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="0916b-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="0916b-126">ฟิลด์ **งบประมาณเดิม** แสดงชั่วโมงของงบประมาณจากการคาดการณ์ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="0916b-127">ฟิลด์ **ชั่วโมงจริง** แสดงชั่วโมงที่ลงรายการบัญชีบนใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="0916b-128">ฟิลด์ **ชั่วโมงผูกมัด** แสดงจำนวนรวมของชั่วโมงที่บริษัทของคุณจะได้รับการกำหนดในความสัมพันธ์กับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="0916b-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![ตัวอย่างของการคำนวณการควบคุมชั่วโมงของสินทรัพย์](media/04-controlling-and-reporting.png)

<span data-ttu-id="0916b-130">อีกวิธีหนึ่งในการทำการคำนวณชั่วโมงเป็นการเลือกสินทรัพย์หลายรายการใน **สินทรัพย์ทั้งหมด** หรือ **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0916b-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="0916b-131">จากนั้น คุณคลิกปุ่ม **การควบคุมชั่วโมง** บน FastTab **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="0916b-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="0916b-132">สินทรัพย์ที่เลือกจะถูกแทรกโดยอัตโนมัติในฟิลด์ **สินทรัพย์** บนเเท็บด่วน **เรกคอร์ดเพื่อรวม**</span><span class="sxs-lookup"><span data-stu-id="0916b-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="0916b-133">คลิก **ตกลง** ในกล่องโต้ตอบ **การควบคุมชั่วโมงของสินทรัพย์** และการคำนวณสำหรับสินทรัพย์ที่เลือกจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="0916b-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="0916b-134">กระบวนงานเดียวกันสามารถใช้สำหรับตำเเหน่งที่ทำงานใน **ตำเเหน่งที่ทำงานทั้งหมด** หรือ **ตำเเหน่งที่ทำงานที่ใช้งานอยู่** เเละสำหรับใบสั่งงานใน **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="0916b-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


