---
title: สร้างนิติบุคคล
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างนิติบุคคลใน Microsoft Dynamics 365 Commerce ซึ่งต้องมีการสร้างและตั้งค่าคอนฟิกก่อนการสร้างช่องทาง
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800626"
---
# <a name="create-legal-entities"></a><span data-ttu-id="05529-103">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="05529-104">หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างนิติบุคคลใน Microsoft Dynamics 365 Commerce ซึ่งต้องมีการสร้างและตั้งค่าคอนฟิกก่อนการสร้างช่องทาง</span><span class="sxs-lookup"><span data-stu-id="05529-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="05529-105">นิติบุคคลมีโครงสร้างที่มีโครงสร้างทางกฎหมายจดทะเบียน หรือ legislated</span><span class="sxs-lookup"><span data-stu-id="05529-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="05529-106">นิติบุคคลที่สามารถป้อนลงในสัญญาทางกฎหมาย และจำเป็นต้องใช้เพื่อจัดเตรียมรายงานที่รายงานเกี่ยวกับประสิทธิภาพการทำงานของตน</span><span class="sxs-lookup"><span data-stu-id="05529-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="05529-107">บริษัทเป็นนิติบุคคลชนิดหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="05529-107">A company is a type of legal entity.</span></span> <span data-ttu-id="05529-108">ปัจจุบัน บริษัทเป็นชนิดเดียวของนิติบุคคลที่คุณสามารถสร้างขึ้นได้ และนิติบุคคลทุกรายการถูกเชื่อมโยงกับรหัสบริษัท</span><span class="sxs-lookup"><span data-stu-id="05529-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="05529-109">ความสัมพันธ์นี้เกิดขึ้นเนื่องจากบางขอบเขตหน้าที่ในโปรแกรมใช้รหัสบริษัท หรือ *DataAreaId* ในแบบจำลองข้อมูลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="05529-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="05529-110">ในพื้นที่ทำงานเหล่านี้ บริษัทจะถูกใช้เป็นเส้นขอบเขตสำหรับความปลอดภัยของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="05529-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="05529-111">ผู้ใช้สามารถเข้าถึงข้อมูลสำหรับบริษัทที่พวกเขาจะเข้าสู่ระบบในปัจจุบันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="05529-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="05529-112">เมื่อกำลังสร้างช่องทาง คุณต้องระบุว่านิติบุคคลใดที่ช่องทางเป็นสมาชิกอยู่</span><span class="sxs-lookup"><span data-stu-id="05529-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="05529-113">สร้างนิติบุคคลใหม่</span><span class="sxs-lookup"><span data-stu-id="05529-113">Create a new legal entity</span></span>

<span data-ttu-id="05529-114">เมื่อต้องการสร้างนิติบุคคลใหม่ใน Dynamics 365 Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="05529-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="05529-115">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การตั้งค่าศูนย์ควบคุม \> นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="05529-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="05529-116">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="05529-116">On the action pane, select **New**.</span></span> <span data-ttu-id="05529-117">บานหน้าต่าง **นิติบุคคลใหม่** จะปรากฏขึ้นที่ด้านขวา</span><span class="sxs-lookup"><span data-stu-id="05529-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="05529-118">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="05529-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="05529-119">ในฟิลด์ **บริษัท** ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="05529-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="05529-120">ในฟิลด์ **ประเทศ/ภูมิภาค**  ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="05529-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="05529-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="05529-121">Select **OK**.</span></span> 

   ![การสร้างนิติบุคคล](media/legal-entities.png)

1. <span data-ttu-id="05529-123">ในส่วน **ทั่วไป** ให้ข้อมูลทั่วไปต่อไปนี้เกี่ยวกับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="05529-124">ป้อนชื่อสำหรับค้นหา ถ้าต้องการชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="05529-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="05529-125">ชื่อสำหรับค้นหาเป็นชื่ออื่นที่สามารถใช้ในการค้นหาสำหรับนิติบุคคลนี้</span><span class="sxs-lookup"><span data-stu-id="05529-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="05529-126">เลือกว่านิติบุคคลนี้ถูกใช้เป็นบริษัทสำหรับการรวมบัญชีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="05529-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="05529-127">เลือกว่านิติบุคคลนี้กำลังจะถูกใช้เป็นบริษัทที่ตัดออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="05529-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="05529-128">เลือก **ภาษาเริ่มต้น** สำหรับเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="05529-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="05529-129">เลือก **โซนเวลา** สำหรับเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="05529-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="05529-130">ในส่วน **ที่อยู่** ให้เลือก **แก้ไข** เพื่อป้อนข้อมูลที่อยู่ เช่นชื่อถนน เลขที่บ้าน รหัสไปรษณีย์ และชื่อเมือง</span><span class="sxs-lookup"><span data-stu-id="05529-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="05529-131">ในส่วน **ข้อมูลผู้ติดต่อ** ให้ป้อนข้อมูลเกี่ยวกับวิธีการสื่อสาร เช่น ที่อยู่อีเมล์, URLs และหมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="05529-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="05529-132">ในส่วน **การรายงานตามกฎหมาย** ให้ป้อนหมายเลขทะเบียนภาษีที่ใช้สำหรับการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="05529-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="05529-133">ในส่วน **หมายเลขทะเบียนภาษี** ให้ป้อนข้อมูลใด ๆ ก็ตามที่นิติบุคคลต้องการ</span><span class="sxs-lookup"><span data-stu-id="05529-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="05529-134">ในส่วน **ข้อมูลบัญชีธนาคาร** ให้ป้อนบัญชีธนาคารและหมายเลขเส้นทางสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="05529-135">ในส่วน **การค้าต่างประเทศและลอจิสติกส์** ให้ป้อนข้อมูลการจัดส่งสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="05529-136">ในส่วน **ลำดับหมายเลข** คุณสามารถดูลำดับหมายเลขที่เชื่อมโยงกับนิติบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="05529-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="05529-137">การทำเช่นนี้จะว่าง เพื่อเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="05529-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="05529-138">ในส่วน **รูปภาพในแดชบอร์ด** สามารถดูหรือเปลี่ยนรูปโลโก้ และรูปภาพแดชบอร์ดที่เชื่อมโยงกับนิติบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="05529-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="05529-139">ในส่วน **ทะเบียนภาษี** ให้ป้อนหมายเลขทะเบียนที่ใช้เพื่อรายงานกับหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="05529-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="05529-140">ในส่วน **ภาษี 1099** ให้ป้อนข้อมูล 1099 สำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="05529-141">ในส่วน **ข้อมูลภาษี** ป้อนข้อมูลภาษีสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="05529-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="05529-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="05529-142">Select **Save**.</span></span>

<span data-ttu-id="05529-143">รูปภาพต่อไปนี้แสดงรายละเอียดของนิติบุคคลตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="05529-143">The following image shows details of an example legal entity.</span></span>

![ส่วนทั่วไปของนิติบุคคล](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="05529-145">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="05529-145">Additional resources</span></span>

[<span data-ttu-id="05529-146">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="05529-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="05529-147">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="05529-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="05529-148">ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="05529-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="05529-149">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="05529-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="05529-150">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="05529-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
