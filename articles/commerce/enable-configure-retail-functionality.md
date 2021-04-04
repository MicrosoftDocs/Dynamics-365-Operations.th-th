---
title: เริ่มต้นข้อมูลเบื้องต้นในสภาพแวดล้อม Commerce ใหม่
description: บทความนี้อธิบายข้อมูลที่ถูกสร้างเป็นส่วนหนึ่งของกระบวนการการเริ่มต้นสำหรับ Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a12bd7a178d8d40db8c919410a00fbf021625f50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238761"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="d77e8-103">เริ่มต้นข้อมูลเบื้องต้นในสภาพแวดล้อม Commerce ใหม่</span><span class="sxs-lookup"><span data-stu-id="d77e8-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d77e8-104">บทความนี้อธิบายข้อมูลที่ถูกสร้างเป็นส่วนหนึ่งของกระบวนการการเริ่มต้นสำหรับ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d77e8-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d77e8-105">หลังจากโซลูชันเชิงพาณิชย์ได้รับการปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) คุณต้องเริ่มต้นการกำหนดค่าการค้า เพื่อสร้างข้อมูลการกำหนดค่าพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d77e8-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d77e8-106">ก่อนที่คุณจะเริ่มต้นการกำหนดค่าการค้า ตรวจสอบให้แน่ใจว่าคุณได้ระบุภาษาและที่อยู่ทางไปรษณีย์สำหรับเอนทิตีทางกฎหมายแต่ละแห่งที่คุณจะตั้งค่าร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="d77e8-107">ขั้นตอนนี้จะต้องดำเนินการให้เสร็จสมบูรณ์สำหรับแต่ละเอนทิตีทางกฎหมายที่คุณใช้เพื่อการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="d77e8-108">เพื่อเริ่มต้นการกำหนดค่า ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d77e8-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="d77e8-109">เริ่มต้นไคลเอ็นการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="d77e8-110">คลิก **การขายปลีกและการค้า** &gt; **การตั้งสำนักงานใหญ่** &gt; **พารามิเตอร์** &gt; **พารามิเตอร์การค้า**</span><span class="sxs-lookup"><span data-stu-id="d77e8-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="d77e8-111">คลิก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d77e8-111">Click **Initialize**.</span></span>

<span data-ttu-id="d77e8-112">การเริ่มต้นจะสร้างข้อมูลการตั้งค่าคอนฟิกเริ่มต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d77e8-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="d77e8-113">งานและงานย่อยของตัวจัดกำหนดการการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="d77e8-114">แบบแผนช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-114">Commerce channel schema</span></span>
- <span data-ttu-id="d77e8-115">กำหนดการกระจายสินค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="d77e8-116">โครงร่างหน้าจอเริ่มต้น ซึ่งได้แก่ กริดปุ่ม รูปภาพ และชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="d77e8-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="d77e8-117">ข้อมูลโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="d77e8-117">Time zone information</span></span>
- <span data-ttu-id="d77e8-118">การดำเนินการการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="d77e8-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="d77e8-119">สิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="d77e8-119">POS permissions</span></span>
- <span data-ttu-id="d77e8-120">รายงานของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="d77e8-120">Channel reports</span></span>
- <span data-ttu-id="d77e8-121">ข้อมูลเมตาของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="d77e8-121">Attribute metadata</span></span>
- <span data-ttu-id="d77e8-122">เท็มเพลตการตรวจสอบเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="d77e8-122">Entity validation templates</span></span>
- <span data-ttu-id="d77e8-123">ชุดงานที่จะล้างประวัติเซสชัน Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="d77e8-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="d77e8-124">นอกจากนี้ การบันทึกที่เกี่ยวข้องกับอุตสาหกรรมบัตรชำระเงิน (PCI) ถูกเปิดใช้งานสำหรับฐานข้อมูลการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="d77e8-125">มีตัวเลือกในการกำหนดค่าตัวจัดกำหนดการการค้าแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="d77e8-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="d77e8-126">ตัวเลือกนี้ช่วยให้คุณตั้งค่าการกำหนดค่าตัวจัดกำหนดการการค้าใหม่เป็นการตั้งค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d77e8-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="d77e8-127">หลังจากการเริ่มต้นเสร็จสมบูรณ์ คุณต้องกำหนดค่าข้อมูลการค้าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d77e8-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="d77e8-128">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="d77e8-128">Here are some examples:</span></span>

- <span data-ttu-id="d77e8-129">พารามิเตอร์การค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-129">Commerce parameters</span></span>
- <span data-ttu-id="d77e8-130">พารามิเตอร์ตัวจัดกำหนดการการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="d77e8-131">ช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="d77e8-131">Commerce channels</span></span>
- <span data-ttu-id="d77e8-132">การลงทะเบียนและอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="d77e8-132">Registers and devices</span></span>
- <span data-ttu-id="d77e8-133">การจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="d77e8-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]