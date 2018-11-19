---
title: "ตั้งค่าการจัดการข้อเสนอ"
description: "หัวข้อนี้อธิบายวิธีการตั้งค่าข้อเสนอใน Talent"
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: th-th
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="152a1-103">ตั้งค่าการจัดการข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="152a1-104">เมื่อผู้สมัครถูกย้ายไปยังระยะข้อเสนอใน Dynamics 365 for Talent: Attract คุณจำเป็นต้องแน่ใจว่า ข้อเสนอสามารถถูกสร้างได้อย่างรวดเร็วสำหรับผู้สมัคร ได้รับอนุมัติตามความจำเป็น และถูกส่งไปที่ผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="152a1-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="152a1-105">เนื่องจากข้อเสนอส่วนใหญ่เป็นมาตรฐาน สามารถสร้างรายการเหล่านั้นได้จากเท็มเพลตที่สามารถนำกลับมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="152a1-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="152a1-106">ใน Attract ข้อเสนอทั้งหมดถูกย้อนไปยังแพคเกจข้อเสนอ ซึ่งเป็นชุดของเอกสารข้อเสนออย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="152a1-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="152a1-107">หัวข้อนี้แสดงรายการขั้นตอนทั้งหมดที่ผู้ดูแลระบบ Attract จะปฏิบัติตาม เพื่อตั้งค่าเท็มเพลตแพคเกจข้อเสนอต่างๆ เป็นส่วนหนึ่งของความสามารถในการจัดการข้อเสนอใน Attract</span><span class="sxs-lookup"><span data-stu-id="152a1-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="152a1-108">ผู้ใช้ที่มีบทบาทที่ไม่ใช่ผู้ดูแลระบบจะไม่สามารถเข้าถึงความสามารถเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="152a1-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="152a1-109">มีความสามารถในการจัดการข้อเสนอที่พร้อมใช้งานเป็นส่วนหนึ่งของ Add-On การจ้างงานแบบครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="152a1-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="152a1-110">ข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-110">Offer data</span></span> 

<span data-ttu-id="152a1-111">ข้อมูลข้อเสนอเป็นหน่วยเล็กที่สุดภายในเท็มเพลตแพคเกจข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="152a1-112">ข้อเสนอโดยทั่วไปประกอบด้วยข้อความมาตรฐานและชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="152a1-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="152a1-113">ชุดของค่าเป็นเพียงส่วนที่สามารถเปลี่ยนได้ระหว่างข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="152a1-114">ในระหว่างการสร้างข้อเสนอ แง่ที่สำคัญที่สุดที่ผู้สร้างข้อเสนอสามารถมุ่งเน้นคือ รายการของตัวยึดตำแหน่งข้อมูลข้อเสนอที่มีอยู่ในเท็มเพลตแพคเกจข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="152a1-115">ในการตั้งค่าข้อมูลข้อเสนอ ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="152a1-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="152a1-116">ไปยัง **การจัดการข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="152a1-117">ขยายส่วน **ไลบรารี** ในบานหน้าต่างนำทางด้านซ้าย จากนั้นไปยัง **ข้อมูลข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="152a1-118">บนหน้า **ข้อมูลข้อเสนอ** มีส่วน **รายละเอียดผู้สมัคร** และ **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="152a1-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="152a1-119">Attract ให้ตัวยึดตำแหน่งข้อมูลข้อเสนอสองสามรายการแบบสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="152a1-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="152a1-120">มีส่วนต่างๆ บนหน้า เพื่อจัดระเบียบตัวยึดตำแหน่งข้อมูลข้อเสนอต่างๆ เข้าด้วยกันเป็นกลุ่มเชิงตรรกะ</span><span class="sxs-lookup"><span data-stu-id="152a1-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="152a1-121">ส่วนเหล่านี้สามารถช่วยในการบำรุงรักษาของข้อมูลข้อเสนอและการเติมของข้อมูลในระหว่างกระบวนการสร้างข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="152a1-122">เมื่อต้องการสร้างส่วนข้อมูลข้อเสนอ คลิก **เพิ่มส่วน** และป้อนชื่อเฉพาะสำหรับส่วน</span><span class="sxs-lookup"><span data-stu-id="152a1-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="152a1-123">เมื่อต้องการเพิ่มตัวยึดตำแหน่งข้อมูลข้อเสนอไปยังส่วนใดๆ คลิก **เพิ่มข้อมูลข้อเสนอ** และป้อนชื่อเฉพาะสำหรับตัวยึดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="152a1-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="152a1-124">เมื่อต้องการแก้ไขชื่อของส่วนใดๆ วางเมาส์ไว้เหนือชื่อส่วน และอัพเดตชื่อ</span><span class="sxs-lookup"><span data-stu-id="152a1-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="152a1-125">เพื่อแก้ไขชื่อของตัวยึดตำแหน่งข้อมูลข้อเสนอที่มีอยู่ใดๆ อันดับแรก ต้องแน่ใจว่าตัวยึดตำแหน่งไม่ได้เป็นส่วนหนึ่งของเท็มเพลตใดๆ อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="152a1-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="152a1-126">จากนั้น วางเมาส์ไว้เหนือชื่อของตัวยึดตำแหน่งข้อมูลข้อเสนอ และอัพเดตชื่อตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="152a1-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="152a1-127">เพื่อลบตัวยึดตำแหน่งข้อมูลข้อเสนอที่มีอยู่ใดๆ อันดับแรก ต้องแน่ใจว่าตัวยึดตำแหน่งไม่ได้เป็นส่วนหนึ่งของเท็มเพลตอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="152a1-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="152a1-128">จากนั้น วางเมาส์ไว้เหนือตัวยึดตำแหน่ง และเมื่อไอคอนถังขยะปรากฏขึ้น คลิกที่ถังขยะเพื่อลบตัวยึดตำแหน่งข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="152a1-129">คุณสามารถดูได้ว่า เท็มเพลตกี่รายการที่ตัวยึดตำแหน่งข้อมูลข้อเสนอเป็นส่วนหนึ่ง โดยตัวบ่งชี้หมายเลขถัดจากข้อมูลข้อเสนอแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="152a1-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="152a1-130">ในการลบส่วนใดๆ วางเมาส์ไว้เหนือชื่อ</span><span class="sxs-lookup"><span data-stu-id="152a1-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="152a1-131">ถ้าไม่มีตัวยึดตำแหน่งข้อมูลข้อเสนอภายในส่วนปรากฏในเท็มเพลตใดๆ คุณสามารถคลิกไอคอนถังขยะเพื่อลบออกได้</span><span class="sxs-lookup"><span data-stu-id="152a1-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="152a1-132">การลบส่วนยังจะลบตัวยึดข้อมูลข้อเสนอทั้งหมดภายในส่วนนั้นอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="152a1-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="152a1-133">หลังจากที่ตัวยึดตำแหน่งข้อมูลข้อเสนอได้ถูกตั้งค่า คุณสามารถใช้ทั่วทั้งเท็มเพลตเอกสารใดๆ ได้</span><span class="sxs-lookup"><span data-stu-id="152a1-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="152a1-134">ตัวยึดตำแหน่งข้อมูลข้อเสนอจะไม่ถูกจำกัดกับเท็มเพลตเฉพาะ -- ชุดเดียวกันสามารถใช้ได้ในเท็มเพลตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="152a1-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="152a1-135">กฎข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-135">Offer data rules</span></span>

<span data-ttu-id="152a1-136">องค์กรส่วนใหญ่มีกฎสำหรับวิธีที่ข้อเสนอต้องถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="152a1-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="152a1-137">ตัวอย่างเช่น องค์กรอาจต้องการกำหนดว่า ข้อเสนอเงินเดือนต่อปีสูงสุดสำหรับชุดของระดับอายุงานและตำแหน่งที่ตั้งที่ระบุ ต้องอยู่ภายในช่วงเฉพาะ หรือว่ามีเพียงค่าเฉพาะสองสามค่าที่เป็นไปได้สำหรับระดับข้อเสนอสำหรับการจ้างงานใหม่</span><span class="sxs-lookup"><span data-stu-id="152a1-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="152a1-138">ในขณะนี้ Attract สนับสนุนกฎข้อมูลดังกล่าวทั้งหมดโดยใช้ไฟล์ CSV</span><span class="sxs-lookup"><span data-stu-id="152a1-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="152a1-139">ในการจัดเตรียมไฟล์ CSV ของกฎข้อมูล ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="152a1-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="152a1-140">กำหนดตัวยึดตำแหน่งข้อมูลข้อเสนอสำหรับชุดกฎ</span><span class="sxs-lookup"><span data-stu-id="152a1-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="152a1-141">ตัวอย่างเช่น **เงินเดือนต่อปี**</span><span class="sxs-lookup"><span data-stu-id="152a1-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="152a1-142">ระบุค่าตัวยึดข้อมูลข้อเสนอที่ไม่เป็นอิสระ</span><span class="sxs-lookup"><span data-stu-id="152a1-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="152a1-143">ตัวอย่างเช่น **ตำแหน่งงาน** และ **ระดับ**</span><span class="sxs-lookup"><span data-stu-id="152a1-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="152a1-144">ระบุคอลัมน์ 1 และ 2 เป็น **ตำแหน่งงาน** และ **ระดับ**</span><span class="sxs-lookup"><span data-stu-id="152a1-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="152a1-145">ในการอัพโหลดค่าช่วง ทำคอลัมน์ 3 และ 4 ให้เป็น **เงินเดือนต่อปี**</span><span class="sxs-lookup"><span data-stu-id="152a1-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="152a1-146">เพื่ออัพโหลดค่าเฉพาะแทนช่วง ทำเฉพาะคอลัมน์ 3 ให้เป็น **เงินเดือนต่อปี**</span><span class="sxs-lookup"><span data-stu-id="152a1-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="152a1-147">เติมข้อมูลไฟล์ Microsoft Excel ตามบทบาทที่ต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="152a1-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="152a1-148">ให้แน่ใจว่า แถวแต่ละแถวเป็นชุดเฉพาะของค่าทั้งหมดที่รวมอยู่ด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="152a1-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="152a1-149">บันทึกไฟล์เป็นรูปแบบ CSV</span><span class="sxs-lookup"><span data-stu-id="152a1-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="152a1-150">ในการอัปโหลดกฎข้อมูลข้อเสนอ ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="152a1-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="152a1-151">ไปยัง **การจัดการข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="152a1-152">ขยายส่วน **ไลบรารี** ในแผงการนำทางด้านซ้าย จากนั้นไปยัง **กฎข้อมูลข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="152a1-153">คลิก **ชุดข้อมูลใหม่** เพื่อแสดงกล่องโต้ตอบ **อัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="152a1-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="152a1-154">ระบุชื่อที่ไม่ซ้ำสำหรับชุดกฎ และจากนั้น อัพโหลดไฟล์ CSV ที่บันทึกไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="152a1-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="152a1-155">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="152a1-155">Click **Add**.</span></span>
    <span data-ttu-id="152a1-156">ชุดกฎจะถูกประมวลผลอยู่เบื้องหลัง และคุณจะได้รับแจ้งในแอป และทางอีเมล เมื่อเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="152a1-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="152a1-157">คุณจะได้รับแจ้ง ถ้ามีข้อผิดพลาดขณะที่ประมวลผลการอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="152a1-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="152a1-158">จากนั้น คุณสามารถดาวน์โหลดล็อกข้อผิดพลาด แก้ไขไฟล์ และอัพโหลดอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="152a1-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="152a1-159">ใช้ตัวเลือกปุ่มจุดไข่ปลา (**...**) ถ้าคุณต้องการดาวน์โหลดชุดกฎ และปรับปรุงชุดของค่า</span><span class="sxs-lookup"><span data-stu-id="152a1-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="152a1-160">หลังจากการอัพเดต คุณสามารถอัพโหลดไฟล์อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="152a1-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="152a1-161">คุณสามารถลบการอัพโหลดชุดกฎที่มีอยู่ ถ้าไม่ได้ใช้ตัวยึดตำแหน่งที่กำหนดอยู่ในเท็มเพลตเอกสารอื่น</span><span class="sxs-lookup"><span data-stu-id="152a1-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!หมายเหตุ]
> - <span data-ttu-id="152a1-163">ตัวยึดตำแหน่งแต่ละรายการสามารถมีชุดของคอลัมน์เฉพาะที่ขึ้นอยู่</span><span class="sxs-lookup"><span data-stu-id="152a1-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="152a1-164">ตัวอย่างเช่น ถ้า **เงินเดือนรายปี** ขึ้นอยู่กับ **ตำแหน่งงาน** และ **ระดับ** คุณไม่สามารถอัพโหลดชุดกฎอื่นได้ ที่ซึ่ง **เงินเดือนรายปี** จะขึ้นอยู่กับชุดของคอลัมน์ต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="152a1-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="152a1-165">คุณสามารถดาวน์โหลดชุดกฎของข้อมูลข้อเสนอตัวอย่างบนแท็บ **ตัวอย่าง** บนหน้า **กฎของข้อมูลข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="152a1-166">เมื่อผู้สร้างข้อเสนอแทนค่าที่แนะนำโดยกฎข้อมูลข้อเสนอ ข้อเสนอถูกตั้งค่าสถานะเป็นไม่ได้มาตรฐาน และลำดับงานการอนุมัติข้อเสนอจะถูกบังคับ</span><span class="sxs-lookup"><span data-stu-id="152a1-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="152a1-167">เท็มเพลตเอกสาร</span><span class="sxs-lookup"><span data-stu-id="152a1-167">Document templates</span></span>

<span data-ttu-id="152a1-168">เท็มเพลตเอกสารการข้อเสนอสามารถช่วยให้ผู้ดูแลระบบสามารถสร้างจดหมายข้อเสนอได้</span><span class="sxs-lookup"><span data-stu-id="152a1-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="152a1-169">เท็มเพลตเอกสารข้อเสนอคือ ชุดของข้อความที่จะเป็นส่วนหนึ่งของข้อเสนอ ตลอดจนตัวยึดตำแหน่งข้อมูลข้อเสนอที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="152a1-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="152a1-170">เพื่อสร้างเท็มเพลตเอกสารข้อเสนอ ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="152a1-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="152a1-171">ไปยัง **การจัดการข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="152a1-172">ขยายส่วน **ไลบรารี** ในบานหน้าต่างนำทางด้านซ้าย และไปยัง **เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="152a1-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="152a1-173">หน้า **เท็มเพลต** จะแสดงรายการของเท็มเพลตเอกสารที่ได้กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="152a1-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="152a1-174">ในการสร้างเท็มเพลตเอกสารใหม่ คลิก **สร้างเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="152a1-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="152a1-175">ป้อนชื่อที่ไม่ซ้ำกันสำหรับเท็มเพลต และคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="152a1-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="152a1-176">ใช้โปรแกรมแก้ไขข้อความแบบ rich เพื่อแทรก หรือแก้ไขเนื้อหาของเอกสารข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="152a1-177">คุณสามารถแทรกตาราง รูปภาพ และการเชื่อมโยงหลายมิติได้ โดยใช้ตัวเลือกที่พร้อมใช้งานที่ด้านบนของโปรแกรมแก้ไขข้อความ</span><span class="sxs-lookup"><span data-stu-id="152a1-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="152a1-178">คุณสามารถแทรกตัวยึดตำแหน่งข้อมูลข้อเสนอในเอกสารเท็มเพลตข้อเสนอโดย:</span><span class="sxs-lookup"><span data-stu-id="152a1-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="152a1-179">การลากและการปล่อยจากบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="152a1-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="152a1-180">แฮชแท็กตัวยึดตำแหน่งข้อมูลข้อเสนอโดยตรงไปยังตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="152a1-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="152a1-181">พิมพ์ **\#** แล้วจากนั้น เริ่มพิมพ์ชื่อของตัวยึดตำแหน่งข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="152a1-182">ตัวเลือกจะปรากฏในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="152a1-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="152a1-183">คลิก หรือกด **ป้อน** เพื่อแทรกตัวยึดตำแหน่งข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!หมายเหตุ]
    > - <span data-ttu-id="152a1-185">ในการเชื่อมโยงตัวยึดตำแหน่งกับเท็มเพลตเอกสารข้อเสนอ โดยไม่มีการแสดงค่าต่อผู้สมัคร วางเมาส์ไว้เหนือตัวยึดตำแหน่งข้อมูลข้อเสนอ และคลิกไอคอน **ปักหมุด**</span><span class="sxs-lookup"><span data-stu-id="152a1-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="152a1-186">นี่จะผลักตัวยึดตำแหน่งไปยังส่วน **ข้อมูลข้อเสนอที่ปักหมุด** ของเท็มเพลตเอกสารข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="152a1-187">เมื่อต้องการถอนการปักหมุด ทำตามขั้นตอนเดียวกัน แต่คลิก **ถอนการปักหมุด** ในรายการของตัวยึดตำแหน่งข้อมูลข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="152a1-188">เมื่อต้องการดูรายการของตัวยึดตำแหน่งข้อมูลข้อเสนอที่ใช้งานอยู่ สลับไปยังแท็บ **ใช้งานอยู่** ในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="152a1-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="152a1-189">ถ้าคุณแทรกตัวยึดตำแหน่งที่ควบคุมโดยชุดกฎข้อมูลที่มีข้อเสนอ คุณสามารถดูการขึ้นต่อกันของที่เสนอตัวยึดตำแหน่งในค่าอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="152a1-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="152a1-190">อีกทางหนึ่งคือ คุณสามารถ **นำเข้า** เนื้อหาจากแฟ้ม .docx บนเครื่องคอมพิวเตอร์ของคุณ และแก้ไขตามความจำเป็นได้</span><span class="sxs-lookup"><span data-stu-id="152a1-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="152a1-191">วิธีนั้น คุณไม่ต้องพิมพ์ในเนื้อหาทั้งหมดในโปรแกรมแก้ไข</span><span class="sxs-lookup"><span data-stu-id="152a1-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="152a1-192">เมื่อต้องการแสดงตัวอย่างเอกสารข้อเสนอ ใช้ตัวเลือก **การแสดงตัวอย่าง** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="152a1-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="152a1-193">เมื่อต้องการควบคุมว่าผู้สร้างข้อเสนอสามารถแก้ไขเนื้อหาเอกสารข้อเสนอได้หรือไม่ ใช้ตัวเลือก **จัดการสิทธิ์** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="152a1-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="152a1-194">ถ้าคุณต้องการให้ผู้สร้างข้อเสนอสามารถแทรกค่าตัวยึดตำแหน่งได้เท่านั้น และไม่สามารถแก้ไขข้อความได้ ตั้งค่าสิทธิ์เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="152a1-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="152a1-195">คลิก **บันทึก** เพื่อบันทึกกระบวนการของคุณ</span><span class="sxs-lookup"><span data-stu-id="152a1-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="152a1-196">เท็มเพลตที่จะถูกบันทึกในสถานะร่าง</span><span class="sxs-lookup"><span data-stu-id="152a1-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="152a1-197">เมื่อต้องการทำให้เสร็จสิ้น และทำเครื่องหมายเอกสารเป็นเผยแพร่ คลิก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="152a1-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="152a1-198">คุณสามารถดูว่าเท็มเพลตเอกสารใดที่ใช้งานอยู่ในขณะนี้ ในโหมดแบบร่าง และได้ถูกเก็บถาวร และจะไม่ใช้งานในประสบการณ์เริ่มต้นของไลบรารีเท็มเพลตเอกสารอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="152a1-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="152a1-199">คุณสามารถลบเท็มเพลตเอกสารข้อเสนอใดๆ ที่ไม่ใช่ส่วนหนึ่งของเท็มเพลตแพคเกจข้อเสนอที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="152a1-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="152a1-200">เท็มเพลตในแพคเกจข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-200">Offer package templates</span></span>

<span data-ttu-id="152a1-201">แพคเกจข้อเสนอเป็นอาร์ทิแฟกต์ข้อเสนอที่ใช้ร่วมกับผู้สมัคร และประกอบด้วยชุดของเท็มเพลตเอกสารข้อเสนอหนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="152a1-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="152a1-202">เพื่อสร้างแพคเกจข้อเสนอ ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="152a1-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="152a1-203">ไปยัง **การจัดการข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="152a1-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="152a1-204">ไปยัง **แพคเกจ** จากบานหน้าต่างนำทางด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="152a1-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="152a1-205">รายการของเท็มเพลตแพคเกจที่ใช้งานอยู่ที่มีอยู่สำหรับข้อเสนอที่ผู้สร้างจะใช้ จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="152a1-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="152a1-206">เพื่อสร้างแพคเกจข้อเสนอใหม่ คลิก **สร้างแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="152a1-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="152a1-207">ป้อนชื่อที่ไม่ซ้ำกัน และคลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="152a1-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="152a1-208">คลิก **เพิ่มเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="152a1-208">Click **Add template**.</span></span>

    >[!หมายเหตุ]
    > - <span data-ttu-id="152a1-210">คุณสามารถเลือกที่จะสร้างเท็มเพลตใหม่ หรือเลือกจากที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="152a1-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="152a1-211">ถ้าคุณเลือกที่จะเพิ่มเท็มเพลตที่มีอยู่ คุณจำเป็นต้องแน่ใจว่า เท็มเพลตเอกสารข้อเสนอถูกบันทึก กำหนดขั้นสุดท้าย และทำเครื่องหมายเป็น ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="152a1-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="152a1-212">คุณสามารถเลือกเท็มเพลตเอกสารได้หลายรายการตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="152a1-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="152a1-213">คลิก **เสร็จสิ้น** เพื่อกลับสู่ **การจัดการแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="152a1-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="152a1-214">คุณสามารถตั้งค่าคอนฟิกลำดับของเอกสาร และยังสามารถทำเครื่องหมายได้ว่า ข้อเสนอเอกสารเฉพาะมีความจำเป็นในระหว่างการสร้างข้อเสนอหรือไม่</span><span class="sxs-lookup"><span data-stu-id="152a1-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="152a1-215">ผู้สร้างข้อเสนอจะมีตัวเลือกในการลบเอกสารที่ทำเครื่องหมายเป็น **ไม่จำเป็น**</span><span class="sxs-lookup"><span data-stu-id="152a1-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="152a1-216">เมื่อต้องการบันทึกเท็มเพลตแพคเกจข้อเสนอ เพื่อให้สามารถใช้ได้โดยผู้สร้างข้อเสนอทั้งหมด คลิก **บันทึก และเผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="152a1-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="152a1-217">เมื่อต้องการดูเท็มเพลตแพคเกจข้อเสนอแบบร่าง ไปที่แท็บ **แบบร่าง** ถ้ามีการเปลี่ยนแปลงไปยังเท็มเพลตแพคเกจข้อเสนอ จะต้องบันทึกและเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="152a1-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="152a1-218">ตั้งค่าคอนฟิกกระบวนการข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-218">Configure an offer process</span></span>

<span data-ttu-id="152a1-219">มีส่วนของกระบวนการสร้างข้อเสนอหลายส่วนที่สามารถตั้งค่าคอนฟิกได้โดยผู้ดูแลระบบ Attract</span><span class="sxs-lookup"><span data-stu-id="152a1-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="152a1-220">**การอนุมัติข้อเสนอ** - เลือกว่าการอนุมัติข้อเสนอมีความจำเป็นหรือไม่ ก่อนที่ข้อเสนอจะสามารถถูกส่งให้กับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="152a1-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="152a1-221">ในฐานะผู้ดูแลระบบ คุณยังสามารถตัดสินใจได้ว่า การอนุมัติข้อเสนอทั้งหมดจะเกิดขึ้นในลักษณะตามลำดับ หรือลำดับงานการอนุมัติแบบขนาน</span><span class="sxs-lookup"><span data-stu-id="152a1-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="152a1-222">คุณยังสามารถกำหนดได้ว่า ผู้อนุมัติข้อเสนอต้องเพิ่มข้อคิดเห็นพร้อมกับการอนุมัติข้อเสนอหรือไม่</span><span class="sxs-lookup"><span data-stu-id="152a1-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="152a1-223">การอนุมัติข้อเสนอเป็นส่วนบังคับสำหรับข้อเสนอทั้งหมดที่ไม่ใช่มาตรฐานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="152a1-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="152a1-224">**ประสบการณ์ข้อเสนอของผู้สมัคร** - ในฐานะผู้ดูแลระบบ คุณสามารถเลือกเพื่อกำหนดว่าข้อเสนอทั้งหมดที่มีวันหมดอายุหรือไม่ และถ้าเป็นเช่นนั้น ออฟเซ็ตเริ่มต้นสำหรับวันหมดอายุควรจะเป็นอะไร</span><span class="sxs-lookup"><span data-stu-id="152a1-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="152a1-225">คุณยังสามารถตั้งค่าคอนฟิกได้ว่าผู้สมัครสามารถปฏิเสธข้อเสนอได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="152a1-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="152a1-226">**ลายเซ็นอิเล็กทรอนิกส์** - ในปัจจุบัน ตัวเลือกลายเซ็นอิเล็กทรอนิกส์เท่านั้นที่พร้อมใช้งานคือสำหรับผู้สมัครที่จะพิมพ์ชื่อของพวกเขาในแพคเกจข้อเสนอ ขณะที่ยอมรับข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="152a1-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="152a1-227">เราจะนำการรวมคู่ค้ากับผู้ให้บริการลายเซ็นอิเล็กทรอนิกส์อื่นๆ มาใช้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="152a1-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="152a1-228">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับกระบวนการสร้างข้อเสนอ ดู [การสร้าง การอนุมัติ และการรับรองข้อเสนอ](./creating-offers.md)</span><span class="sxs-lookup"><span data-stu-id="152a1-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>

