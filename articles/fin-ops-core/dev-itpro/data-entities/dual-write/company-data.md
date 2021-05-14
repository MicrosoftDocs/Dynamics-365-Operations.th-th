---
title: แนวคิดของบริษัทใน Dataverse
description: หัวข้อนี้อธิบายการรวมของข้อมูลบริษัทระหว่าง Finance and Operations และ Dataverse
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6a858135d377b30d6e8885ae18b2dc50da11813b
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941040"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="ae18a-103">แนวคิดของบริษัทใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae18a-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="ae18a-104">ใน Finance and Operations แนวคิดของ *บริษัท* เป็นทั้งโครงสร้างทางกฎหมายและการสร้างธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ae18a-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="ae18a-105">นอกจากนี้ ยังเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae18a-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="ae18a-106">ผู้ใช้มักจะทำงานในบริบทของบริษัทเดียว และข้อมูลส่วนใหญ่จะถูกแบ่งโดยบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae18a-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="ae18a-107">Dataverse ไม่มีแนวคิดที่เทียบเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="ae18a-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="ae18a-108">แนวคิดที่ใกล้เคียงที่สุดคือ *หน่วยธุรกิจ* ซึ่งส่วนใหญ่แล้วเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูลผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ae18a-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="ae18a-109">แนวคิดนี้ไม่มีผลกระทบทางกฎหมายหรือทางธุรกิจเดียวกันกับแนวคิดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae18a-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="ae18a-110">เนื่องจากหน่วยธุรกิจและบริษัทไม่มีแนวคิดที่เทียบเท่ากัน คุณจึงไม่สามารถบังคับการแม็ปแบบหนึ่งต่อหนึ่ง (1:1) ระหว่างรายการเหล่านั้น เพื่อวัตถุประสงค์ของการรวม Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae18a-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="ae18a-111">อย่างไรก็ตาม เนื่องจากโดยค่าเริ่มต้น ผู้ใช้ต้องสามารถดูแถวเดียวกันได้ในแอปพลิเคชันและ Dataverse Microsoft ได้แนะนำตารางใหม่ใน Dataverse ที่มีชื่อว่า cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="ae18a-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="ae18a-112">ตารางนี้เทียบเท่ากับตารางของบริษัทในแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="ae18a-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="ae18a-113">เพื่อช่วยรับประกันว่าความสามารถในการมองเห็นของแถวเทียบเท่ากับแอปพลิเคชั่นและ Dataverse แบบสำเร็จรูป เราขอแนะนำขั้นตอนต่อไปนี้สำหรับข้อมูลใน Dataverse:</span><span class="sxs-lookup"><span data-stu-id="ae18a-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="ae18a-114">สำหรับแถวของบริษัท Finance and Operations แต่ละแถวที่เปิดใช้งานสำหรับการรวมแบบสองทิศทาง จะมีการสร้างแถว cdm\_Company ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae18a-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="ae18a-115">เมื่อมีการสร้างแถว cdm\_Company และมีการเปิดใช้งานสำหรับการรวมแบบสองทิศทาง จะมีการสร้างหน่วยธุรกิจเริ่มต้นที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ae18a-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="ae18a-116">แม้ว่าทีมงานเริ่มต้นจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับหน่วยธุรกิจนั้น แต่ไม่มีการใช้หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ae18a-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="ae18a-117">มีการสร้างทีมเจ้าของที่แยกต่างหากที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ae18a-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="ae18a-118">นอกจากนี้ ยังมีการเชื่อมโยงกับหน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ae18a-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="ae18a-119">โดยค่าเริ่มต้น เจ้าของของแถวใดๆ ที่สร้างขึ้นและมีการรวมแบบสองทิศทางไปยัง Dataverse จะถูกตั้งค่าเป็นทีมงาน "เจ้าของ DW" ที่เชื่อมโยงกับหน่วยธุรกิจที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae18a-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="ae18a-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าข้อมูลนี้ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae18a-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![การตั้งค่าข้อมูลใน Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="ae18a-122">เนื่องจากการตั้งค่าคอนฟิกนี้ แถวใด ๆ ที่เกี่ยวข้องกับบริษัท USMF จะเป็นเจ้าของโดยทีมงานที่เชื่อมโยงกับหน่วยธุรกิจ USMF ใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae18a-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="ae18a-123">ดังนั้น ผู้ใช้ใดๆ ที่มีการเข้าถึงหน่วยธุรกิจนั้นผ่านทางบทบาทความปลอดภัยที่ถูกตั้งค่าเป็นความสามารถในการมองเห็นระดับหน่วยธุรกิจ สามารถดูแถวเหล่านั้นได้ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="ae18a-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="ae18a-124">ตัวอย่างต่อไปนี้แสดงวิธีการที่สามารถใช้ทีมงานเพื่อให้การเข้าถึงที่ถูกต้องแก่แถวเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="ae18a-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="ae18a-125">บทบาท "ผู้จัดการฝ่ายขาย" ถูกกำหนดให้กับสมาชิกของทีมงาน "ฝ่ายขาย USMF"</span><span class="sxs-lookup"><span data-stu-id="ae18a-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="ae18a-126">ผู้ใช้ที่มีบทบาท "ผู้จัดการฝ่ายขาย" สามารถเข้าถึงแถวบัญชีใดๆ ที่เป็นสมาชิกของหน่วยธุรกิจเดียวกันที่พวกเขาเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ae18a-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="ae18a-127">ทีมงาน "การขาย USMF" เชื่อมโยงกับหน่วยธุรกิจ USMF ที่กล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ae18a-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="ae18a-128">ดังนั้น สมาชิกของทีมงาน "ฝ่ายขาย USMF" สามารถดูบัญชีใดๆ ที่เป็นเจ้าของโดยผู้ใช้ "USMF DW" ซึ่งจะมาจากตารางบริษัท USMF ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ae18a-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![วิธีการที่จะสามารถใช้ทีมได้](media/dual-write-company-2.png)

<span data-ttu-id="ae18a-130">เมื่อภาพประกอบก่อนหน้านี้แสดงขึ้น การแม็ป 1:1 นี้ระหว่างหน่วยธุรกิจ บริษัท และทีม เป็นเพียงจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ae18a-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="ae18a-131">ในตัวอย่างนี้ จะมีการสร้างหน่วยธุรกิจ "ยุโรป" ใหม่ด้วยตนเองใน Dataverse เป็นรายการหลักสำหรับทั้ง DEMF และ ESMF</span><span class="sxs-lookup"><span data-stu-id="ae18a-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="ae18a-132">หน่วยธุรกิจรากใหม่นี้ไม่เกี่ยวข้องกับการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="ae18a-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="ae18a-133">อย่างไรก็ตาม คุณสามารถใช้เพื่อให้สมาชิกของทีมงาน "การขาย EUR" มีการเข้าถึงข้อมูลบัญชีทั้งใน DEMF และ ESMF โดยการตั้งค่าการแสดงผลข้อมูลเป็น **BU หลัก/รอง** ในบทบาทความปลอดภัยที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae18a-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="ae18a-134">หัวข้อสุดท้ายเพื่อหารือเกี่ยวกับวิธีการรวมแบบสองทิศทาง จะกำหนดทีมงานของเจ้าของที่ควรกำหนดแถวให้</span><span class="sxs-lookup"><span data-stu-id="ae18a-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="ae18a-135">ลักษณะการทำงานนี้จะถูกควบคุมโดยคอลัมน์ **ทีมงานที่เป็นเจ้าของเริ่มต้น** บนแถว cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="ae18a-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="ae18a-136">เมื่อมีการเปิดใช้งานแถว dm\_Company สำหรับการรวมแบบสองทิศทาง ปลั๊กอินจะสร้างหน่วยธุรกิจและทีมงานที่เป็นเจ้าของที่เกี่ยวข้อง (ถ้าไม่ได้มีอยู่แล้ว) และตั้งค่าคอลัมน์ **ทีมงานที่เป็นเจ้าของเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ae18a-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="ae18a-137">ผู้ดูแลระบบสามาเปลี่ยนคอลัมน์นี้เป็นค่าอื่นได้</span><span class="sxs-lookup"><span data-stu-id="ae18a-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="ae18a-138">อย่างไรก็ตาม ผู้ดูแลระบบไม่สามารถล้างคอลัมน์ได้ ตราบใดที่ตารางถูกเปิดใช้งานสำหรับการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="ae18a-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="ae18a-139">![คอลัมน์ทีมที่เป็นเจ้าของเริ่มต้น](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="ae18a-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="ae18a-140">การแบ่งและการระดมทุนของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae18a-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="ae18a-141">การรวม Dataverse นำพาริตี้ของบริษัทมาโดยใช้ตัวระบุบริษัทเพื่อแบ่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ae18a-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="ae18a-142">เมื่อภาพประกอบต่อไปนี้แสดงขึ้น ตารางเฉพาะบริษัททั้งหมดจะถูกขยายเพื่อให้มีความสัมพันธ์แบบกลุ่มต่อหนึ่ง (N:1) กับตาราง cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="ae18a-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="ae18a-143">![ความสัมพันธ์แบบ N:1 ระหว่างตารางเฉพาะบริษัทและตาราง cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="ae18a-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="ae18a-144">สำหรับแถว หลังจากที่มีการเพิ่มและบันทึกบริษัท ค่าจะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ae18a-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="ae18a-145">ดังนั้น ผู้ใช้ควรตรวจสอบให้แน่ใจว่าได้เลือกบริษัทที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ae18a-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="ae18a-146">เฉพาะแถวที่มีข้อมูลของบริษัทเท่านั้นที่มีสิทธิ์ในการรวมแบบสองทิศทางระหว่างแอปพลิเคชันและ Dataverse</span><span class="sxs-lookup"><span data-stu-id="ae18a-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="ae18a-147">สำหรับข้อมูล Dataverse ที่มีอยู่ ประสบการณ์ระดมทุนที่นำโดยผู้ดูแลระบบจะพร้อมใช้งานเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="ae18a-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="ae18a-148">เติมข้อมูลชื่อบริษัทอัตโนมัติในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ae18a-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="ae18a-149">การเติมข้อมูลชื่อบริษัทอัตโนมัติในแอปการมีส่วนร่วมของลูกค้ามีหลายวิธี</span><span class="sxs-lookup"><span data-stu-id="ae18a-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="ae18a-150">ถ้าคุณเป็นผู้ดูแลระบบ คุณสามารถตั้งค่าบริษัทเริ่มต้นด้วยการไปยัง **การตั้งค่าขั้นสูง > ระบบ > ความปลอดภัย > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="ae18a-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="ae18a-151">เปิดแบบฟอร์ม **ผู้ใช้** และในส่วน **ข้อมูลองค์กร** ให้กำหนดค่า **บริษัทเป็นค่าเริ่มต้นในแบบฟอร์ม**</span><span class="sxs-lookup"><span data-stu-id="ae18a-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="ตั้งค่าบริษัทเริ่มต้นในส่วนข้อมูลองค์กร":::

+ <span data-ttu-id="ae18a-153">ถ้าคุณมีสิทธิ์ **เขียน** ในตาราง **SystemUser** สำหรับระดับของ **หน่วยธุรกิจ** คุณสามารถเปลี่ยนบริษัทเริ่มต้นในฟอร์มใดๆ ได้โดยการเลือกบริษัทจากเมนูแบบหล่นลงของ **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="ae18a-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="การเปลี่ยนชื่อบริษัทในบัญชีใหม่":::

+ <span data-ttu-id="ae18a-155">หากคุณมีการเข้าถึง **การเขียน** ไปยังข้อมูลในบริษัทมากกว่าหนึ่งแห่ง คุณสามารถเปลี่ยนบริษัทเริ่มต้นได้ด้วยการเลือกแถวที่เป็นของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="ae18a-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="การเลือกแถวจะเปลี่ยนบริษัทเริ่มต้น":::

+ <span data-ttu-id="ae18a-157">หากคุณเป็นผู้ตั้งค่าคอนฟิกระบบหรือผู้ดูแลระบบ และคุณต้องการเติมข้อมูลบริษัทอัตโนมัติในแบบฟอร์มที่กำหนดเอง คุณก็สามารถใช้ [เหตุการณ์แบบฟอร์ม](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids)</span><span class="sxs-lookup"><span data-stu-id="ae18a-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="ae18a-158">เพิ่มการอ้างอิง JavaScript ไปยัง **msdyn_/DefaultCompany.js** และใช้เหตุการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ae18a-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="ae18a-159">คุณสามารถใช้แบบฟอร์มสำเร็จรูปใดๆ ก็ได้ ตัวอย่างเช่น แบบฟอร์ม **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="ae18a-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="ae18a-160">เหตุการณ์ **OnLoad** สำหรับฟอร์ม: ตั้งค่าคอลัมน์ **defaultCompany**</span><span class="sxs-lookup"><span data-stu-id="ae18a-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="ae18a-161">เหตุการณ์ **OnChange** สำหรับคอลัมน์ **บริษัท**: ตั้งค่าคอลัมน์ **updateDefaultCompany**</span><span class="sxs-lookup"><span data-stu-id="ae18a-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="ae18a-162">ใช้การกรองตามบริบทของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae18a-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="ae18a-163">เมื่อต้องการใช้การกรองตามบริบทของบริษัทในฟอร์มที่กำหนดเองของคุณ หรือในคอลัมน์การค้นหาแบบกำหนดเองที่เพิ่มเข้าในฟอร์มมาตรฐาน ให้เปิดฟอร์มและใช้ส่วน **การกรองเรกคอร์ดที่เกี่ยวข้อง** เพื่อใช้ตัวกรองบริษัท</span><span class="sxs-lookup"><span data-stu-id="ae18a-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="ae18a-164">คุณต้องตั้งค่านี้สำหรับคอลัมน์การค้นหาแต่ละคอลัมน์ที่จำเป็นต้องมีการกรองตามบริษัทพื้นฐานในแถวที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="ae18a-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="ae18a-165">การตั้งค่าดังกล่าวแสดงสำหรับ **บัญชี** ในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ae18a-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="ใช้บริบทของบริษัท":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]