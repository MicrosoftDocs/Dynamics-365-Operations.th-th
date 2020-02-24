---
title: แนวคิดของบริษัทใน Common Data Service
description: หัวข้อนี้อธิบายการรวมของข้อมูลบริษัทระหว่าง Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: 20a3f89821af56cb4c3969c89301d4a8a32ab848
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020045"
---
# <a name="company-concept-in-common-data-service"></a><span data-ttu-id="ba490-103">แนวคิดของบริษัทใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba490-103">Company concept in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="ba490-104">ใน Finance and Operations แนวคิดของ *บริษัท* เป็นทั้งโครงสร้างทางกฎหมายและการสร้างธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ba490-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="ba490-105">นอกจากนี้ ยังเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba490-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="ba490-106">ผู้ใช้มักจะทำงานในบริบทของบริษัทเดียว และข้อมูลส่วนใหญ่จะถูกแบ่งโดยบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba490-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="ba490-107">Common Data Service ไม่มีแนวคิดที่เทียบเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="ba490-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="ba490-108">แนวคิดที่ใกล้เคียงที่สุดคือ *หน่วยธุรกิจ* ซึ่งส่วนใหญ่แล้วเป็นขอบเขตความปลอดภัยและการมองเห็นสำหรับข้อมูลผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ba490-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="ba490-109">แนวคิดนี้ไม่มีผลกระทบทางกฎหมายหรือทางธุรกิจเดียวกันกับแนวคิดของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba490-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="ba490-110">เนื่องจากหน่วยธุรกิจและบริษัทไม่มีแนวคิดที่เทียบเท่ากัน คุณจึงไม่สามารถบังคับการแม็ปแบบหนึ่งต่อหนึ่ง (1:1) ระหว่างรายการเหล่านั้น เพื่อวัตถุประสงค์ของการรวม Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba490-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="ba490-111">อย่างไรก็ตาม เนื่องจากผู้ใช้ต้อง โดยค่าเริ่มต้น จะสามารถดูเรกคอร์ดเดียวกันได้ในแอพลิเคชัน และ Common Data Service Microsoft ได้แนะนำเอนทิตีใหม่ใน Common Data Service ที่มีชื่อว่า cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="ba490-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="ba490-112">เอนทิตีนี้เทียบเท่ากับเอนทิตีของบริษัทในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="ba490-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="ba490-113">เพื่อช่วยรับประกันว่าความสามารถในการมองเห็นของเรกคอร์ดเทียบเท่ากับแอพลิเคชั่นและ Common Data Service แบบสำเร็จรูป และเราขอแนะนำขั้นตอนต่อไปนี้สำหรับข้อมูลใน Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="ba490-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="ba490-114">สำหรับเรกคอร์ดของบริษัท Finance and Operations แต่ละรายการที่เปิดใช้งานสำหรับการเขียนแบบคู่ จะมีการสร้างเรกคอร์ด cdm\_Company ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ba490-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="ba490-115">เมื่อมีการสร้าง cdm\_Company และมีการเปิดใช้งานสำหรับการเขียนแบบคู่ จะมีการสร้างหน่วยธุรกิจเริ่มต้นที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ba490-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="ba490-116">แม้ว่าทีมงานเริ่มต้นจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับหน่วยธุรกิจนั้น แต่ไม่มีการใช้หน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ba490-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="ba490-117">มีการสร้างทีมเจ้าของที่แยกต่างหากที่มีชื่อเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="ba490-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="ba490-118">นอกจากนี้ ยังมีการเชื่อมโยงกับหน่วยธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="ba490-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="ba490-119">โดยค่าเริ่มต้น เจ้าของของเรกคอร์ดใดๆ ที่สร้างขึ้นและมีการเขียนแบบคู่ไปยัง Common Data Service จะถูกตั้งค่าเป็นทีมงาน "เจ้าของ DW" ที่เชื่อมโยงกับหน่วยธุรกิจที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ba490-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="ba490-120">ภาพประกอบต่อไปนี้แสดงตัวอย่างของการตั้งค่าข้อมูลนี้ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba490-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![การตั้งค่าข้อมูลใน Common Data Service](media/dual-write-company-1.png)

<span data-ttu-id="ba490-122">เนื่องจากการตั้งค่าคอนฟิกนี้ เรกคอร์ดใด ๆ ที่เกี่ยวข้องกับบริษัท USMF จะเป็นเจ้าของโดยทีมงานที่เชื่อมโยงกับหน่วยธุรกิจ USMF ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba490-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="ba490-123">ดังนั้น ผู้ใช้ใดๆ ที่มีการเข้าถึงหน่วยธุรกิจนั้นผ่านทางบทบาทความปลอดภัยที่ถูกตั้งค่าเป็นความสามารถในการมองเห็นระดับหน่วยธุรกิจ ในขณะนี้สามารถดูเรกคอร์ดเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="ba490-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="ba490-124">ตัวอย่างต่อไปนี้แสดงวิธีการที่สามารถใช้ทีมงานเพื่อให้การเข้าถึงที่ถูกต้องแก่เรกคอร์ดเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="ba490-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="ba490-125">บทบาท "ผู้จัดการฝ่ายขาย" ถูกกำหนดให้กับสมาชิกของทีมงาน "ฝ่ายขาย USMF"</span><span class="sxs-lookup"><span data-stu-id="ba490-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="ba490-126">ผู้ใช้ที่มีบทบาท "ผู้จัดการฝ่ายขาย" สามารถเข้าถึงเรกคอร์ดบัญชีใดๆ ที่เป็นสมาชิกของหน่วยธุรกิจเดียวกันที่พวกเขาเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="ba490-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="ba490-127">ทีมงาน "การขาย USMF" เชื่อมโยงกับหน่วยธุรกิจ USMF ที่กล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ba490-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="ba490-128">ดังนั้น สมาชิกของทีม "ฝ่ายขาย USMF" สามารถดูบัญชีใดๆ ที่เป็นเจ้าของโดยผู้ใช้ "USMF DW" ซึ่งจะมาจากเอนทิตีบริษัท USMF ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ba490-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![วิธีการที่จะสามารถใช้ทีมได้](media/dual-write-company-2.png)

<span data-ttu-id="ba490-130">เมื่อภาพประกอบก่อนหน้านี้แสดงขึ้น การแม็ป 1:1 นี้ระหว่างหน่วยธุรกิจ บริษัท และทีม เป็นเพียงจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ba490-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="ba490-131">ในตัวอย่างนี้ จะมีการสร้างหน่วยธุรกิจ "ยุโรป" ใหม่ด้วยตนเองใน Common Data Service เป็นรายการหลักสำหรับทั้ง DEMF และ ESMF</span><span class="sxs-lookup"><span data-stu-id="ba490-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="ba490-132">หน่วยธุรกิจรากใหม่นี้ไม่เกี่ยวข้องกับการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="ba490-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="ba490-133">อย่างไรก็ตาม คุณสามารถใช้เพื่อให้สมาชิกของทีมงาน "การขาย EUR" มีการเข้าถึงข้อมูลบัญชีทั้งใน DEMF และ ESMF โดยการตั้งค่าการแสดงผลข้อมูลเป็น **BU หลัก/รอง** ในบทบาทความปลอดภัยที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ba490-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="ba490-134">หัวข้อสุดท้ายเพื่อหารือเกี่ยวกับวิธีการเขียนแบบคู่กำหนดทีมงานของเจ้าของที่ควรกำหนดเรกคอร์ดให้</span><span class="sxs-lookup"><span data-stu-id="ba490-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="ba490-135">ลักษณะการทำงานนี้จะถูกควบคุมโดยฟิลด์ **ทีมงานที่เป็นเจ้าของเริ่มต้น** บนเรกคอร์ด cdm\_Company</span><span class="sxs-lookup"><span data-stu-id="ba490-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="ba490-136">เมื่อมีการเปิดใช้งานเรกคอร์ด dm\_Company สำหรับการเขียนแบบคู่ ปลั๊กอินจะสร้างหน่วยธุรกิจที่เกี่ยวข้องและทีมงานของเจ้าของ (ถ้าไม่ได้มีอยู่แล้ว) และตั้งค่าฟิลด์ **ทีมงานที่เป็นเจ้าของเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="ba490-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="ba490-137">ผู้ดูแลระบบสามาเปลี่ยนฟิลด์นี้เป็นค่าอื่นได้</span><span class="sxs-lookup"><span data-stu-id="ba490-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="ba490-138">อย่างไรก็ตาม ผู้ดูแลระบบไม่สามารถล้างฟิลด์ ตราบใดที่เอนทิตีถูกเปิดใช้งานสำหรับการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="ba490-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="ba490-139">![ฟิลด์ทีมที่เป็นเจ้าของเริ่มต้น](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="ba490-139">![Default owning team field](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="ba490-140">การแบ่งและการระดมทุนของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba490-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="ba490-141">การรวม Common Data Service นำพาริตี้ของบริษัทมาโดยใช้ตัวระบุบริษัทเพื่อแบ่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ba490-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="ba490-142">เมื่อภาพประกอบต่อไปนี้แสดงขึ้น เอนทิตีเฉพาะบริษัททั้งหมดจะถูกขยายเพื่อให้มีความสัมพันธ์แบบกลุ่มต่อหนึ่ง (N:1) กับ cdm\_เอนทิตีของบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba490-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="ba490-143">![ความสัมพันธ์แบบ N:1 ระหว่างเอนทิตีเฉพาะบริษัทและเอนทิตี cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="ba490-143">![N:1 relationship between a company-specific entity and the cdm_Company entity](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="ba490-144">สำหรับเรกคอร์ด หลังจากที่มีการเพิ่มและบันทึกบริษัท ค่าจะกลายเป็นแบบอ่านอย่างเดียว</span><span class="sxs-lookup"><span data-stu-id="ba490-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="ba490-145">ดังนั้น ผู้ใช้ควรตรวจสอบให้แน่ใจว่าได้เลือกบริษัทที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="ba490-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="ba490-146">เฉพาะเรกคอร์ดที่มีข้อมูลของบริษัทเท่านั้นที่มีสิทธิ์ในการเขียนแบบคู่ระหว่างแอพลิเคชันและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ba490-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="ba490-147">สำหรับข้อมูล Common Data Service ที่มีอยู่ ประสบการณ์ระดมทุนที่นำโดยผู้ดูแลระบบจะพร้อมใช้งานเร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="ba490-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>
