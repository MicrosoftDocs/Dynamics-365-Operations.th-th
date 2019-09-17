---
title: การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ
description: การป้อนข้อมูลสำหรับผู้ปฏิบัติงานใน Dynamics 365 for Talent ได้รับการปรับปรุงเพื่ออนุญาตให้มีการป้อนข้อมูลด่วนสำหรับพนักงานทั้งหมดในอดีต ปัจจุบัน หรืออนาคต แบบจำลองการนำทางแบบง่าย/แบบรวมได้รับการปรับปรุง เพื่อให้ค้นหาข้อมูลที่เกี่ยวข้องและดูและทำการปรับปรุงที่จำเป็นใดๆ อย่างรวดเร็ว
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: be0253ffc4396f36050ef02c51a20d378e44473d
ms.sourcegitcommit: 4176c333ce3f88c5c68e95bd47e5791d32365dd2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918225"
---
# <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="14c77-104">การป้อนข้อมูลและการนำทางของพนักงานที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="14c77-104">Streamlined employee entry and navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14c77-105">Dynamics 365 for Talent อนุญาตให้มีการป้อนข้อมูลพนักงานและข้อมูลการจ้างงานได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="14c77-105">Dynamics 365 for Talent allows efficient entry of employee and employment data.</span></span> <span data-ttu-id="14c77-106">คุณสามารถปรับปรุงข้อมูลประวัติการทำงานสำหรับพนักงานและผู้รับเหมาในอดีต ปัจจุบัน และอนาคตได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="14c77-106">You can quickly update work history information for past, active, and future employees and contractors.</span></span>

<span data-ttu-id="14c77-107">นอกจากนี้ คุณยังสามารถเปิดใช้งานประสบการณ์การนำทางแบบง่าย เพื่อให้สามารถค้นหาข้อมูลที่เกี่ยวข้องและทำการเปลี่ยนแปลงใดๆ ที่จำเป็นได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="14c77-107">You can also enable a simplified navigation experience to quickly find related information and make any necessary changes.</span></span> <span data-ttu-id="14c77-108">ขณะนี้ฟังก์ชันนี้พร้อมใช้งานในสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="14c77-108">This functionality is now available in sandbox environments.</span></span> <span data-ttu-id="14c77-109">เมื่อต้องการเปิดใช้งานคุณลักษณะนี้ นำทางไปที่ **การจัดการระบบ > ลิงค์ > การตั้งค่า > พารามิเตอร์ระบบ > คุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="14c77-109">To turn this feature on, navigate to **System administration > Links > Setup > System parameters > Preview features**.</span></span> <span data-ttu-id="14c77-110">เลือก **ฟอร์มผู้ปฏิบัติงานที่มีการปรับปรุงและการนำทาง**</span><span class="sxs-lookup"><span data-stu-id="14c77-110">Select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="14c77-111">การทำเช่นนี้จะเปิดใช้งานการเปลี่ยนแปลงเหล่านี้สำหรับผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="14c77-111">This will enable these changes for all users.</span></span> <span data-ttu-id="14c77-112">คุณสามารถปิดตัวเลือกนี้ได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="14c77-112">You can turn this option off at any time.</span></span>

## <a name="view-options"></a><span data-ttu-id="14c77-113">ตัวเลือกมุมมอง</span><span class="sxs-lookup"><span data-stu-id="14c77-113">View options</span></span>

<span data-ttu-id="14c77-114">คุณสามารถใช้ **ตัวเลือกมุมมอง** บนฟอร์มผู้ปฏิบัติงาน เพื่อเลือกชุดใดๆ ของพนักงานและผู้รับเหมาจากรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="14c77-114">You can use **View options** on the worker form to select any combination of employees and contractors from a single list.</span></span> <span data-ttu-id="14c77-115">ตัวเลือกเหล่านี้ช่วยให้คุณสามารถดูผู้ปฏิบัติงานในนิติบุคคลหรือสำหรับนิติบุคคลที่คุณกำลังลงชื่อเข้าใช้ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="14c77-115">These options allow you to view workers across legal entities or for the legal entity you're currently signed into.</span></span> <span data-ttu-id="14c77-116">นอกจากนี้ คุณยังสามารถดูผู้ปฏิบัติงานที่ใช้งานอยู่ ที่ค้างอยู่ และที่ออกจากงานได้ และคุณสามารถจำกัดผลลัพธ์ตามชนิดของผู้ปฏิบัติงาน (พนักงาน หรือผู้รับเหมา)</span><span class="sxs-lookup"><span data-stu-id="14c77-116">You can also view active, pending, and exited workers, and you can restrict results based on the type of worker (employee or contractor).</span></span> <span data-ttu-id="14c77-117">ถ้ามีการเปิดใช้งานการรักษาความปลอดภัยขั้นสูง คุณจะเห็นเฉพาะพนักงานและผู้รับเหมาเหล่านั้นในนิติบุคคลที่คุณมีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="14c77-117">If advanced security is enabled, you will only see those employees and contractors in the legal entities you have access to.</span></span>

<span data-ttu-id="14c77-118">คอลัมน์ในมุมมองรายการจะเปลี่ยนตามการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="14c77-118">Columns in the list view change based on your selections.</span></span> <span data-ttu-id="14c77-119">ตัวอย่างเช่น เมื่อดูพนักงานที่ออกจากงาน วันที่สิ้นสุดการจ้างงานและรหัสเหตุผลจะแสดงเป็นคอลัมน์เพิ่มเติมในรายการ</span><span class="sxs-lookup"><span data-stu-id="14c77-119">For example, when viewing exited employees, the termination date and reason codes display as additional columns in the list.</span></span> 

<span data-ttu-id="14c77-120">[![ตัวเลือกมุมมอง](./media/Worker-view-option.png)](./media/worker-view-option.png)</span><span class="sxs-lookup"><span data-stu-id="14c77-120">[![View options](./media/Worker-view-option.png)](./media/worker-view-option.png)</span></span>

## <a name="navigation-and-banner"></a><span data-ttu-id="14c77-121">การนำทางและแบนเนอร์</span><span class="sxs-lookup"><span data-stu-id="14c77-121">Navigation and banner</span></span>

<span data-ttu-id="14c77-122">แบนเนอร์จะแสดงข้อมูลสำคัญสำหรับผู้ปฏิบัติงานแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="14c77-122">A banner displays key information for each worker.</span></span> <span data-ttu-id="14c77-123">แบนเนอร์สำหรับผู้ปฏิบัติงานที่ใช้งานอยู่จะแสดงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14c77-123">The banner for active workers displays the following fields:</span></span>

- <span data-ttu-id="14c77-124">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="14c77-124">**Title**</span></span>
- <span data-ttu-id="14c77-125">**แผนก**</span><span class="sxs-lookup"><span data-stu-id="14c77-125">**Department**</span></span>
- <span data-ttu-id="14c77-126">**ชนิดของตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="14c77-126">**Position type**</span></span>
- <span data-ttu-id="14c77-127">**ชนิดผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="14c77-127">**Worker type**</span></span>
- <span data-ttu-id="14c77-128">**ผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="14c77-128">**Manager**</span></span>
- <span data-ttu-id="14c77-129">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="14c77-129">**Legal entity**</span></span>

<span data-ttu-id="14c77-130">แบนเนอร์สำหรับผู้ปฏิบัติงานที่ออกจะแสดงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14c77-130">The banner for exited workers displays the following fields:</span></span>

- <span data-ttu-id="14c77-131">**วันที่ออก**</span><span class="sxs-lookup"><span data-stu-id="14c77-131">**Exited date**</span></span>
- <span data-ttu-id="14c77-132">**เหตุผล**</span><span class="sxs-lookup"><span data-stu-id="14c77-132">**Reason**</span></span>

<span data-ttu-id="14c77-133">แบนเนอร์สำหรับพนักงานที่ค้างอยู่จะแสดงฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14c77-133">The banner for pending employees displays the following fields:</span></span>

- <span data-ttu-id="14c77-134">**ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="14c77-134">**Title**</span></span>
- <span data-ttu-id="14c77-135">**แผนก**</span><span class="sxs-lookup"><span data-stu-id="14c77-135">**Department**</span></span>
- <span data-ttu-id="14c77-136">**ชนิดของตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="14c77-136">**Position type**</span></span>
- <span data-ttu-id="14c77-137">**ผู้จัดการ**</span><span class="sxs-lookup"><span data-stu-id="14c77-137">**Manager**</span></span>
- <span data-ttu-id="14c77-138">**วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="14c77-138">**Starting date**</span></span>
- <span data-ttu-id="14c77-139">**นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="14c77-139">**Legal entity**</span></span>

<span data-ttu-id="14c77-140">บานหน้าต่างการดำเนินการของหน้าผู้ปฏิบัติงานได้รับการจัดระเบียบใหม่เพื่อให้มีตัวเลือกที่น้อยลง</span><span class="sxs-lookup"><span data-stu-id="14c77-140">The action pane of the worker page has been re-organized to include fewer options.</span></span> <span data-ttu-id="14c77-141">ขณะนี้มีการจัดระเบียบข้อมูลในประเภทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="14c77-141">Information is now organized in the following categories:</span></span> 

- <span data-ttu-id="14c77-142">งาน</span><span class="sxs-lookup"><span data-stu-id="14c77-142">Work</span></span>
- <span data-ttu-id="14c77-143">บุคคล</span><span class="sxs-lookup"><span data-stu-id="14c77-143">Person</span></span>
- <span data-ttu-id="14c77-144">ออก</span><span class="sxs-lookup"><span data-stu-id="14c77-144">Leave</span></span>
- <span data-ttu-id="14c77-145">ค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="14c77-145">Compensation</span></span>
- <span data-ttu-id="14c77-146">สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="14c77-146">Benefits</span></span>
- <span data-ttu-id="14c77-147">การปฏิบัติตาม</span><span class="sxs-lookup"><span data-stu-id="14c77-147">Compliance</span></span>

<span data-ttu-id="14c77-148">นอกจากนี้ แท็บ **ลิงค์** ใหม่บนหน้าผู้ปฏิบัติงานหลัก จะช่วยให้ผู้ใช้มีตำแหน่งศูนย์กลางเพื่อเข้าถึงข้อมูลที่เกี่ยวข้องทั้งหมดสำหรับผู้ปฏิบัติงานได้</span><span class="sxs-lookup"><span data-stu-id="14c77-148">In addtion, a new **Links** tab on the main worker page gives users a central location to access all related information for a worker.</span></span>

<span data-ttu-id="14c77-149">เนื่องจากการเปลี่ยนแปลงเหล่านี้ ข้อมูลอาจปรากฏในสถานที่อื่นนอกเหนือจากที่คุณเคย</span><span class="sxs-lookup"><span data-stu-id="14c77-149">Due to these changes, information may appear in a different location than you're used to.</span></span> <span data-ttu-id="14c77-150">ตัวอย่างเช่น ข้อมูลค่าจ้างที่แสดงไว้ก่อนหน้านี้บนฟอร์มผู้ปฏิบัติงานในขณะนี้จะปรากฏในบานหน้าต่างการดำเนินการที่อยู่ภายใต้ **ค่าตอบแทน** และในขณะนี้แท็บ **ข้อมูลส่วนบุคคล** มีปุ่ม **ข้อมูลเพิ่มเติม** เพื่อซ่อนฟิลด์ที่ไม่ถูกเข้าถึงบ่อยครั้ง</span><span class="sxs-lookup"><span data-stu-id="14c77-150">For example, payroll information that previously displayed on the worker form now appears in the action pane under **Compensation > Payroll**, and the **Personal information** tab now has a **More information** button to hide fields that aren't accessed often.</span></span>

<span data-ttu-id="14c77-151">[![แบนเนอร์](./media/Banner.png)](./media/Banner.png)</span><span class="sxs-lookup"><span data-stu-id="14c77-151">[![Banner](./media/Banner.png)](./media/Banner.png)</span></span>

## <a name="work-history"></a><span data-ttu-id="14c77-152">ประวัติการทำงาน</span><span class="sxs-lookup"><span data-stu-id="14c77-152">Work history</span></span>

<span data-ttu-id="14c77-153">แท็บ **ประวัติการทำงาน** จะแสดงประวัติการทำงานระหว่างนิติบุคคลทั้งหมด และพร้อมใช้งานสำหรับพนักงานและผู้รับเหมาที่ออก ที่ทำงานอยู่ และที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="14c77-153">The **Work history** tab shows work history accross all legal entities and is available for exited, active, and pending employees and contractors.</span></span> <span data-ttu-id="14c77-154">ขณะนี้คุณสามารถดูประวัติการทำงานทั้งหมดในครั้งเดียวสำหรับนิติบุคคลที่คุณมีสิทธิ์เข้าถึง</span><span class="sxs-lookup"><span data-stu-id="14c77-154">You can now view all work history at once for the legal entities you have access to.</span></span> <span data-ttu-id="14c77-155">นอกจากนี้ คุณสามารถแก้ไขข้อมูลสำหรับรายการประวัติการทำงานแต่ละรายการได้โดยไม่ต้องเปลี่ยนบริบทข้อมูล</span><span class="sxs-lookup"><span data-stu-id="14c77-155">In addition, you can edit information for each of the work history entries without changing the data context.</span></span> <span data-ttu-id="14c77-156">คุณสามารถปรับปรุงข้อมูลทั้งหมดได้โดยตรงบนหน้า</span><span class="sxs-lookup"><span data-stu-id="14c77-156">You can update all information directly on the page.</span></span> 

<span data-ttu-id="14c77-157">[![ประวัติการทำงาน](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span><span class="sxs-lookup"><span data-stu-id="14c77-157">[![Work history](./media/Worker-work-history.png)](./media/Worker-work-history.png)</span></span>

## <a name="position-history"></a><span data-ttu-id="14c77-158">ประวัติตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="14c77-158">Position history</span></span>

<span data-ttu-id="14c77-159">แท็บ **ตำแหน่ง** บนหน้าผู้ปฏิบัติงานหลักจะให้มุมมองแบบเต็มของตำแหน่งงานทั้งหมดที่จัดไว้ภายในองค์กร ซึ่งรวมถึงการกำหนดในอดีต ปัจจุบัน และในอนาคตใดๆ</span><span class="sxs-lookup"><span data-stu-id="14c77-159">The **Positions** tab on the main worker page provides a full view of all positions held within the organization, including past, present, and any future assignments.</span></span> <span data-ttu-id="14c77-160">นอกจากนี้ คุณยังสามารถนำทางไปยังประวัติตำแหน่งของผู้ปฏิบัติงานในบานหน้าต่างการดำเนินการได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="14c77-160">You can still navigate directly to the worker's position history in the action pane as well.</span></span>

<span data-ttu-id="14c77-161">[![ตำแหน่งงาน](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span><span class="sxs-lookup"><span data-stu-id="14c77-161">[![Positions](./media/Worker-position-history.png)](./media/Worker-position-history.png)</span></span>

