---
title: "เริ่มต้นข้อมูลเบื้องต้นในสภาพแวดล้อม Retail ใหม่"
description: "บทความนี้อธิบายข้อมูลที่ถูกสร้างขึ้นเป็นส่วนหนึ่งของกระบวนการเริ่มต้นสำหรับ Microsoft Dynamics 365 for Retail"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 80fa443fc235496a111a8a866d2e703202721268
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="834fb-103">เริ่มต้นข้อมูลเบื้องต้นในสภาพแวดล้อม Retail ใหม่</span><span class="sxs-lookup"><span data-stu-id="834fb-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="834fb-104">บทความนี้อธิบายข้อมูลที่ถูกสร้างขึ้นเป็นส่วนหนึ่งของกระบวนการเริ่มต้นสำหรับ Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="834fb-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="834fb-105">หลังจากโซลูชันการขายปลีกได้ถูกจัดวางแล้วโดยใช้ Microsoft Dynamics Lifecycle Services (LCS) คุณต้องเริ่มการตั้งค่าคอนฟิกการขายปลีกเพื่อสร้างข้อมูลการตั้งค่าคอนฟิกพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="834fb-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="834fb-106">**สิ่งสำคัญ:** ก่อนที่คุณจะเริ่มต้นการตั้งค่าคอนฟิกการขายปลีก ให้ตรวจสอบให้แน่ใจว่าคุณได้ระบุภาษาและที่อยู่ทางไปรษณีย์สำหรับนิติบุคคลแต่ละรายที่คุณจะตั้งค่าร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="834fb-107">ขั้นตอนนี้ต้องมีการดำเนินงานให้เสร็จสมบูรณ์สำหรับนิติบุคคลแต่ละรายที่คุณใช้สำหรับการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="834fb-108">เพื่อเริ่มการตั้งค่าคอนฟิกการขายปลึก ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="834fb-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="834fb-109">เริ่มต้นใช้งานไคลเอนต์ Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="834fb-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="834fb-110">คลิก **การขายปลีก** &gt; **การตั้งค่าศูนย์ควบคุม** &gt; **พารามิเตอร์** &gt; **พารามิเตอร์การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="834fb-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="834fb-111">คลิก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="834fb-111">Click **Initialize**.</span></span>

<span data-ttu-id="834fb-112">การเริ่มต้นจะสร้างข้อมูลการตั้งค่าคอนฟิกเริ่มต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="834fb-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="834fb-113">งานและงานย่อยของตัวกำหนดตารางทำงานการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="834fb-114">Schema ช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-114">Retail channel schema</span></span>
-   <span data-ttu-id="834fb-115">กำหนดการการกระจายการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="834fb-116">โครงร่างหน้าจอเริ่มต้น ซึ่งได้แก่ กริดปุ่ม รูปภาพ และชุดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="834fb-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="834fb-117">ข้อมูลโซนเวลา</span><span class="sxs-lookup"><span data-stu-id="834fb-117">Time zone information</span></span>
-   <span data-ttu-id="834fb-118">การดำเนินการการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="834fb-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="834fb-119">สิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="834fb-119">POS permissions</span></span>
-   <span data-ttu-id="834fb-120">รายงานของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="834fb-120">Channel reports</span></span>
-   <span data-ttu-id="834fb-121">ข้อมูลเมตาของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="834fb-121">Attribute metadata</span></span>
-   <span data-ttu-id="834fb-122">เท็มเพลตการตรวจสอบเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="834fb-122">Entity validation templates</span></span>
-   <span data-ttu-id="834fb-123">ชุดงานที่จะล้างข้อมูลประวัติรอบเวลาการแลกเปลี่ยนข้อมูลทางการค้า</span><span class="sxs-lookup"><span data-stu-id="834fb-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="834fb-124">นอกจากนี้ การล็อกที่เกี่ยวข้องกับอุตสาหกรรมบัตรชำระเงิน (PCI) จะถูกเปิดใช้งานสำหรับฐานข้อมูล Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="834fb-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="834fb-125">**หมายเหตุ:** มีตัวเลือกเพื่อตั้งค่าคอนฟิกตัวจัดกำหนดการการขายปลีกโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="834fb-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="834fb-126">ตัวเลือกนี้ช่วยให้คุณรีเซ็ตการตั้งค่าคอนฟิกตัวกำหนดตารางทำงานการขายปลีกไปเป็นการตั้งค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="834fb-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="834fb-127">หลังจากการเริ่มต้นเสร็จสมบูรณ์แล้ว คุณต้องตั้งค่าคอนฟิกข้อมูลการขายปลีกเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="834fb-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="834fb-128">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="834fb-128">Here are some examples:</span></span>

-   <span data-ttu-id="834fb-129">พารามิเตอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-129">Retail parameters</span></span>
-   <span data-ttu-id="834fb-130">พารามิเตอร์ของตัวกำหนดตารางทำงานการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="834fb-131">ช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="834fb-131">Retail channels</span></span>
-   <span data-ttu-id="834fb-132">เครื่องบันทึกเงินสดและอุปกรณ์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="834fb-132">Registers and devices</span></span>
-   <span data-ttu-id="834fb-133">การจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="834fb-133">Assortments</span></span>





