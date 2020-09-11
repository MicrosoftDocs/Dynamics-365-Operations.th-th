---
title: แนวคิดของบริษัทใน Common Data Service
description: หัวข้อนี้อธิบายการรวมของข้อมูลบริษัทระหว่าง Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728424"
---
# <a name="company-concept-in-common-data-service"></a><span data-ttu-id="03985-103">แนวคิดของบริษัทใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03985-103">Company concept in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="03985-104">ใน Finance and Operations แนวคิดของ *บริษัท* เป็นทั้งโครงสร้างทางกฎหมายและการสร้างธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="03985-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="03985-105">นอกจากนี้ ยังเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="03985-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="03985-106">ผู้ใช้มักจะทำงานในบริบทของบริษัทเดียว และข้อมูลส่วนใหญ่จะถูกแบ่งโดยบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="03985-107">Common Data Service ไม่มีแนวคิดที่เทียบเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="03985-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="03985-108">แนวคิดที่ใกล้เคียงที่สุดคือ *หน่วยธุรกิจ* ซึ่งส่วนใหญ่แล้วเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูลผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="03985-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="03985-109">แนวคิดนี้ไม่มีผลกระทบทางกฎหมายหรือทางธุรกิจเดียวกันกับแนวคิดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="03985-110">เนื่องจากหน่วยธุรกิจและบริษัทไม่มีแนวคิดที่เทียบเท่ากัน คุณจึงไม่สามารถบังคับการแม็ปแบบหนึ่งต่อหนึ่ง (1:1) ระหว่างรายการเหล่านั้น เพื่อวัตถุประสงค์ของการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03985-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="03985-111">อย่างไรก็ตาม เนื่องจากผู้ใช้ต้อง โดยค่าเริ่มต้น จะสามารถดูเรกคอร์ดเดียวกันได้ในแอพลิเคชัน และ Common Data Service Microsoft ได้แนะนำเอนทิตีใหม่ใน Common Data Service ที่มีชื่อว่า cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="03985-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="03985-112">เอนทิตีนี้เทียบเท่ากับเอนทิตีของบริษัทในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="03985-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="03985-113">เพื่อช่วยรับประกันว่าความสามารถในการมองเห็นของเรกคอร์ดเทียบเท่ากับแอพลิเคชั่นและ Common Data Service แบบสำเร็จรูป และเราขอแนะนำขั้นตอนต่อไปนี้สำหรับข้อมูลใน Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="03985-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="03985-114">สำหรับเรกคอร์ดของบริษัท Finance and Operations แต่ละรายการที่เปิดใช้งานสำหรับการเขียนแบบคู่ จะมีการสร้างเรกคอร์ด cdm\_Company ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="03985-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="03985-115">เมื่อมีการสร้าง cdm\_Company และมีการเปิดใช้งานสำหรับการเขียนแบบคู่ จะมีการสร้างหน่วยธุรกิจเริ่มต้นที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="03985-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="03985-116">แม้ว่าทีมงานเริ่มต้นจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับหน่วยธุรกิจนั้น แต่ไม่มีการใช้หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="03985-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="03985-117">มีการสร้างทีมเจ้าของที่แยกต่างหากที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="03985-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="03985-118">นอกจากนี้ ยังมีการเชื่อมโยงกับหน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="03985-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="03985-119">โดยค่าเริ่มต้น เจ้าของของเรกคอร์ดใดๆ ที่สร้างขึ้นและมีการเขียนแบบคู่ไปยัง Common Data Service จะถูกตั้งค่าเป็นทีมงาน "เจ้าของ DW" ที่เชื่อมโยงกับหน่วยธุรกิจที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="03985-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="03985-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าข้อมูลนี้ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03985-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![การตั้งค่าข้อมูลใน Common Data Service](media/dual-write-company-1.png)

<span data-ttu-id="03985-122">เนื่องจากการตั้งค่าคอนฟิกนี้ เรกคอร์ดใด ๆ ที่เกี่ยวข้องกับบริษัท USMF จะเป็นเจ้าของโดยทีมงานที่เชื่อมโยงกับหน่วยธุรกิจ USMF ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03985-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="03985-123">ดังนั้น ผู้ใช้ใดๆ ที่มีการเข้าถึงหน่วยธุรกิจนั้นผ่านทางบทบาทความปลอดภัยที่ถูกตั้งค่าเป็นความสามารถในการมองเห็นระดับหน่วยธุรกิจ ในขณะนี้สามารถดูเรกคอร์ดเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="03985-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="03985-124">ตัวอย่างต่อไปนี้แสดงวิธีการที่สามารถใช้ทีมงานเพื่อให้การเข้าถึงที่ถูกต้องแก่เรกคอร์ดเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="03985-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="03985-125">บทบาท "ผู้จัดการฝ่ายขาย" ถูกกำหนดให้กับสมาชิกของทีมงาน "ฝ่ายขาย USMF"</span><span class="sxs-lookup"><span data-stu-id="03985-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="03985-126">ผู้ใช้ที่มีบทบาท "ผู้จัดการฝ่ายขาย" สามารถเข้าถึงเรกคอร์ดบัญชีใดๆ ที่เป็นสมาชิกของหน่วยธุรกิจเดียวกันที่พวกเขาเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="03985-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="03985-127">ทีมงาน "การขาย USMF" เชื่อมโยงกับหน่วยธุรกิจ USMF ที่กล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="03985-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="03985-128">ดังนั้น สมาชิกของทีม "ฝ่ายขาย USMF" สามารถดูบัญชีใดๆ ที่เป็นเจ้าของโดยผู้ใช้ "USMF DW" ซึ่งจะมาจากเอนทิตีบริษัท USMF ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="03985-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![วิธีการที่จะสามารถใช้ทีมได้](media/dual-write-company-2.png)

<span data-ttu-id="03985-130">เมื่อภาพประกอบก่อนหน้านี้แสดงขึ้น การแม็ป 1:1 นี้ระหว่างหน่วยธุรกิจ บริษัท และทีม เป็นเพียงจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="03985-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="03985-131">ในตัวอย่างนี้ จะมีการสร้างหน่วยธุรกิจ "ยุโรป" ใหม่ด้วยตนเองใน Common Data Service เป็นรายการหลักสำหรับทั้ง DEMF และ ESMF</span><span class="sxs-lookup"><span data-stu-id="03985-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="03985-132">หน่วยธุรกิจรากใหม่นี้ไม่เกี่ยวข้องกับการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="03985-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="03985-133">อย่างไรก็ตาม คุณสามารถใช้เพื่อให้สมาชิกของทีมงาน "การขาย EUR" มีการเข้าถึงข้อมูลบัญชีทั้งใน DEMF และ ESMF โดยการตั้งค่าการแสดงผลข้อมูลเป็น **BU หลัก/รอง** ในบทบาทความปลอดภัยที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="03985-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="03985-134">หัวข้อสุดท้ายเพื่อหารือเกี่ยวกับวิธีการเขียนแบบคู่กำหนดทีมงานของเจ้าของที่ควรกำหนดเรกคอร์ดให้</span><span class="sxs-lookup"><span data-stu-id="03985-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="03985-135">ลักษณะการทำงานนี้จะถูกควบคุมโดยฟิลด์ **ทีมงานที่เป็นเจ้าของเริ่มต้น** บนเรกคอร์ด cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="03985-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="03985-136">เมื่อมีการเปิดใช้งานเรกคอร์ด dm\_Company สำหรับการเขียนแบบคู่ ปลั๊กอินจะสร้างหน่วยธุรกิจที่เกี่ยวข้องและทีมงานของเจ้าของ (ถ้าไม่ได้มีอยู่แล้ว) และตั้งค่าฟิลด์ **ทีมงานที่เป็นเจ้าของเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="03985-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="03985-137">ผู้ดูแลระบบสามาเปลี่ยนฟิลด์นี้เป็นค่าอื่นได้</span><span class="sxs-lookup"><span data-stu-id="03985-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="03985-138">อย่างไรก็ตาม ผู้ดูแลระบบไม่สามารถล้างฟิลด์ ตราบใดที่เอนทิตีถูกเปิดใช้งานสำหรับการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="03985-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="03985-139">![ฟิลด์ทีมที่เป็นเจ้าของเริ่มต้น](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="03985-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="03985-140">การแบ่งและการระดมทุนของบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="03985-141">การรวม Common Data Service นำพาริตี้ของบริษัทมาโดยใช้ตัวระบุบริษัทเพื่อแบ่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="03985-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="03985-142">เมื่อภาพประกอบต่อไปนี้แสดงขึ้น เอนทิตีเฉพาะบริษัททั้งหมดจะถูกขยายเพื่อให้มีความสัมพันธ์แบบกลุ่มต่อหนึ่ง (N:1) กับ cdm\_เอนทิตีของบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="03985-143">![ความสัมพันธ์แบบ N:1 ระหว่างเอนทิตีเฉพาะบริษัทและเอนทิตี cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="03985-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="03985-144">สำหรับเรกคอร์ด หลังจากที่มีการเพิ่มและบันทึกบริษัท ค่าจะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="03985-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="03985-145">ดังนั้น ผู้ใช้ควรตรวจสอบให้แน่ใจว่าได้เลือกบริษัทที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="03985-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="03985-146">เฉพาะเรกคอร์ดที่มีข้อมูลของบริษัทเท่านั้นที่มีสิทธิ์ในการเขียนแบบคู่ระหว่างแอพลิเคชันและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="03985-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="03985-147">สำหรับข้อมูล Common Data Service ที่มีอยู่ ประสบการณ์ระดมทุนที่นำโดยผู้ดูแลระบบจะพร้อมใช้งานเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="03985-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="03985-148">เติมข้อมูลชื่อบริษัทอัตโนมัติในแอปการมีส่วนร่วมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="03985-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="03985-149">การเติมข้อมูลชื่อบริษัทอัตโนมัติในแอปการมีส่วนร่วมของลูกค้ามีหลายวิธี</span><span class="sxs-lookup"><span data-stu-id="03985-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="03985-150">ถ้าคุณเป็นผู้ดูแลระบบ คุณสามารถตั้งค่าบริษัทเริ่มต้นด้วยการไปยัง **การตั้งค่าขั้นสูง > ระบบ > ความปลอดภัย > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="03985-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="03985-151">เปิดแบบฟอร์ม **ผู้ใช้** และในส่วน **ข้อมูลองค์กร** ให้กำหนดค่า **บริษัทเป็นค่าเริ่มต้นในแบบฟอร์ม**</span><span class="sxs-lookup"><span data-stu-id="03985-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="ตั้งค่าบริษัทเริ่มต้นในส่วนข้อมูลองค์กร":::

+ <span data-ttu-id="03985-153">ถ้าคุณมีสิทธิ์ **การเขียน** ในเอนทิตี้ **SystemUser** สำหรับ **ระดับของหน่วยธุรกิจ** คุณสามารถเปลี่ยนบริษัทเริ่มต้นในแบบฟอร์มใดๆ ได้โดยการเลือกบริษัทจากเมนูแบบหล่นลงของ **บริษัท**</span><span class="sxs-lookup"><span data-stu-id="03985-153">If you have **Write** access to the **SystemUser** entity for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="การเปลี่ยนชื่อบริษัทในบัญชีใหม่":::

+ <span data-ttu-id="03985-155">หากคุณมีสิทธิ์ **การเขียน** ข้อมูลในบริษัทมากกว่าหนึ่งบริษัท คุณสามารถเปลี่ยนบริษัทเริ่มต้นได้ด้วยการเลือกเรกคอร์ดที่เป็นของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="03985-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a record that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="การเลือกเรกคอร์ดจะเปลี่ยนบริษัทเริ่มต้น":::

+ <span data-ttu-id="03985-157">หากคุณเป็นผู้ตั้งค่าคอนฟิกระบบหรือผู้ดูแลระบบ และคุณต้องการเติมข้อมูลบริษัทอัตโนมัติในแบบฟอร์มที่กำหนดเอง คุณก็สามารถใช้ [เหตุการณ์แบบฟอร์ม](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids)</span><span class="sxs-lookup"><span data-stu-id="03985-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="03985-158">เพิ่มการอ้างอิง JavaScript ไปยัง **msdyn_/DefaultCompany.js** และใช้เหตุการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="03985-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="03985-159">คุณสามารถใช้แบบฟอร์มสำเร็จรูปใดๆ ก็ได้ ตัวอย่างเช่น แบบฟอร์ม **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="03985-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="03985-160">เหตุการณ์ **OnLoad** สำหรับแบบฟอร์ม: ตั้งค่าฟิลด์ **defaultCompany**</span><span class="sxs-lookup"><span data-stu-id="03985-160">**OnLoad** event for the form: Set the **defaultCompany** field.</span></span>
    + <span data-ttu-id="03985-161">เหตุการณ์ **OnChange** สำหรับฟิลด์ **บริษัท**: ตั้งค่าฟิลด์ **updateDefaultCompany**</span><span class="sxs-lookup"><span data-stu-id="03985-161">**OnChange** event for the **Company** field: Set the **updateDefaultCompany** field.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="03985-162">ใช้การกรองตามบริบทของบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="03985-163">เมื่อต้องการใช้การกรองตามบริบทของบริษัทในแบบฟอร์มที่กำหนดเองของคุณ หรือในฟิลด์การค้นหาแบบกำหนดเองที่เพิ่มเข้าในแบบฟอร์มมาตรฐาน ให้เปิดแบบฟอร์มและใช้ส่วน **การกรองเรกคอร์ดที่เกี่ยวข้อง** เพื่อใช้ตัวกรองบริษัท</span><span class="sxs-lookup"><span data-stu-id="03985-163">To apply filtering based on the company context on your custom forms or on custom lookup fields added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="03985-164">คุณต้องตั้งค่านี้สำหรับฟิลด์การค้นหาแต่ละฟิลด์ที่จำเป็นต้องมีการกรองตามบริษัทพื้นฐานของเรกคอร์ดที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="03985-164">You must set this for each lookup field that requires filtering based on the underlying company on a given record.</span></span> <span data-ttu-id="03985-165">การตั้งค่าดังกล่าวแสดงสำหรับ **บัญชี** ในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="03985-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="ใช้บริบทของบริษัท":::

