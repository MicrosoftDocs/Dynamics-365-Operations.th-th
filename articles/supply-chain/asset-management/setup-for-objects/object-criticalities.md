---
title: ประเภทการวิพากษ์วิจารณ์สินทรัพย์
description: หัวข้อจะอธิบายชนิดการวิพากษ์วิจารณ์สินทรัพย์ในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb2da2d58b7f98fad80d0ea63bf4445ec4d08163
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808363"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="ef25d-103">ประเภทการวิพากษ์วิจารณ์สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ef25d-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ef25d-104">หัวข้อจะอธิบายชนิดการวิพากษ์วิจารณ์สินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ef25d-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="ef25d-105">การวิพากษ์วิจารณ์สินทรัพย์เกี่ยวข้องกับสินทรัพย์ และจะถูกโอนย้ายไปยังใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ef25d-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="ef25d-106">ไม่สามารถเปลี่ยนแปลงในใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="ef25d-106">It can't be changed on a work order.</span></span> <span data-ttu-id="ef25d-107">การวิพากษ์วิจารณ์สินทรัพย์ถูกใช้ในการคำนวณการวิพากษ์วิจารณ์ใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ef25d-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="ef25d-108">กล่าวคือ มีการใช้ในการคำนวณขอบเขตที่งานบำรุงรักษาในสินทรัพย์มีผลต่อกำหนดการผลิตและผลผลิตในบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="ef25d-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="ef25d-109">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าที่เกี่ยวข้องกับการคำนวณของคะแนนการจัดอันดับสำหรับการจัดกำหนดการใบสั่งงาน ดู [พารามิเตอร์การจัดการสินทรัพย์](../setup-for-objects/enterprise-asset-management-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="ef25d-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="ef25d-110">ในการตั้งค่าการวิพากษ์วิจารณ์ อันดับแรกคุณจะสร้างชนิดของการวิพากษ์วิจารณ์ที่ควรใช้ในการตั้งค่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ef25d-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="ef25d-111">จากนั้น คุณตั้งค่าการวิพากษ์วิจารณ์สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ef25d-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="ef25d-112">ตั้งค่าชนิดการวิพากษ์วิจารณ์</span><span class="sxs-lookup"><span data-stu-id="ef25d-112">Set up criticality types</span></span>

1. <span data-ttu-id="ef25d-113">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **ชนิดการวิพากษ์วิจารณ์**</span><span class="sxs-lookup"><span data-stu-id="ef25d-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="ef25d-114">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="ef25d-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="ef25d-115">ในฟิลด์ **การวิพากษ์วิจารณ์** ให้ป้อนหมายเลขที่บ่งชี้การวิพากษ์วิจารณ์</span><span class="sxs-lookup"><span data-stu-id="ef25d-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="ef25d-116">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับชนิดการวิพากษ์วิจารณ์</span><span class="sxs-lookup"><span data-stu-id="ef25d-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="ef25d-117">ในฟิลด์ **ปัจจัย** ให้ป้อนปัจจัย</span><span class="sxs-lookup"><span data-stu-id="ef25d-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="ef25d-118">ปัจจัยนี้จะใช้ในระหว่างการคำนวณการจัดกำหนดการใบสั่งงาน เพื่อกำหนดเรกคอร์ดการวิพากษ์วิจารณ์ที่ควรใช้</span><span class="sxs-lookup"><span data-stu-id="ef25d-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="ef25d-119">(เรกคอร์ดที่มีการใช้ปัจจัยสูงสุดอยู่เสมอ) การตั้งค่านี้จะเกี่ยวข้องถ้า ดังที่แสดงในภาพประกอบต่อไปนี้ มีการสร้างรายการการวิพากษ์วิจารณ์ที่มีค่าการวิพากษ์วิจารณ์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ef25d-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![หน้าชนิดการวิพากษ์วิจารณ์](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="ef25d-121">ตั้งค่าการวิพากษ์วิจารณ์สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ef25d-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="ef25d-122">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **การวิพากษ์วิจารณ์สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ef25d-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="ef25d-123">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="ef25d-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="ef25d-124">โดยขึ้นอยู่กับระดับที่ต้องการของรายละเอียดสำหรับการวิพากษ์วิจารณ์สินทรัพย์ ทำให้การเลือกที่เกี่ยวข้องในฟิลด์ **ตำแหน่งที่ทำงาน** **ชนิดสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** **สินทรัพย์** **ประเภทชนิดงาน** **ชนิดงาน** **ตัวแปรชนิดงาน** และ **ข้อกำหนดเกี่ยวกับงาน**</span><span class="sxs-lookup"><span data-stu-id="ef25d-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef25d-125">เมื่อมีการเลือกการวิพากษ์วิจารณ์สินทรัพย์ การจัดการสินทรัพย์จะผ่านเรกคอร์ดการวิพากษ์วิจารณ์สินทรัพย์ทั้งหมดเพื่อตรวจสอบการจับคู่ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="ef25d-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="ef25d-126">ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="ef25d-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="ef25d-127">กล่าวอีกนัยหนึ่งคือ อันดับแรกการจัดการสินทรัพย์จะตรวจสอบ **ข้อกำหนดเกี่ยวกับงาน**</span><span class="sxs-lookup"><span data-stu-id="ef25d-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="ef25d-128">ถ้าไม่พบการจับคู่ จะตรวจสอบ **ตัวแปรชนิดงาน**</span><span class="sxs-lookup"><span data-stu-id="ef25d-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="ef25d-129">ถ้าไม่พบการจับคู่ จะตรวจสอบ **ชนิดงาน** และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ef25d-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="ef25d-130">ดังที่คุณสามารถดูได้ในโครงร่างของหน้า ลักษณะการทำงานนี้หมายความว่า การค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์จะตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายสำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="ef25d-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="ef25d-131">ถ้าไม่พบการจับคู่ จะมีการใช้เรกคอร์ด "เริ่มต้น" ที่ไม่มีการใช้การเลือก</span><span class="sxs-lookup"><span data-stu-id="ef25d-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="ef25d-132">ในฟิลด์ **การวิพากษ์วิจารณ์** ให้เลือกหนึ่งในค่าการวิพากษ์วิจารณ์ที่คุณสร้างไว้ในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ef25d-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="ef25d-133">บันทึกย่อเกี่ยวกับการตั้งค่าการวิพากษ์วิจารณ์</span><span class="sxs-lookup"><span data-stu-id="ef25d-133">Notes about criticality setup</span></span>

- <span data-ttu-id="ef25d-134">ถ้าคุณเปลี่ยนแปลงการวิพากษ์วิจารณ์สินทรัพย์ในการตั้งค่านี้ หลังจากที่คุณได้ใช้ในใบสั่งงานแล้ว จะไม่มีการปรับปรุงการวิพากษ์วิจารณ์ในใบสั่งงานให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="ef25d-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="ef25d-135">การวิพากษ์วิจารณ์ในใบสั่งงานจะถูกคำนวณใหม่ทุกครั้งที่มีการเพิ่มหรือลบรายการใบสั่งงานจากใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="ef25d-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="ef25d-136">ถ้าใบสั่งงานประกอบด้วยงานในใบสั่งงานหลายงาน การวิพากษ์วิจารณ์สูงสุด ตามฟิลด์ **ปัจจัย** ในหน้า **ชนิดการวิพากษ์วิจารณ์** จะใช้ในใบสั่งงานเสมอ</span><span class="sxs-lookup"><span data-stu-id="ef25d-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="ef25d-137">โดยทั่วไป การวิพากษ์วิจารณ์สินทรัพย์สามารถเปลี่ยนแปลงได้ตลอดรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="ef25d-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="ef25d-138">การวิพากษ์วิจารณ์อาจได้รับผลกระทบจากการซื้ออุปกรณ์ใหม่ การตกแต่งใหม่ และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="ef25d-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="ef25d-139">พิจารณาการประเมินการวิพากษ์วิจารณ์สินทรัพย์ของคุณใหม่ในช่วงเวลาปกติ (ตัวอย่างเช่น ปีละครั้ง หรือปีเว้นปี) เพื่อให้แน่ใจว่าคำนิยามการวิพากษ์วิจารณ์ของคุณตรงกับการตั้งค่าการผลิตปัจจุบันของคุณ</span><span class="sxs-lookup"><span data-stu-id="ef25d-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]