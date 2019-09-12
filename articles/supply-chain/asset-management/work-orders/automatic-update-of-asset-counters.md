---
title: การอัปเดตตัวนับสินทรัพย์อัตโนมัติ
description: หัวข้อนี้อธิบายการอัปเดตตัวนับสินทรัพย์อัตโนมัติในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875931"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="e2b68-103">การอัปเดตตัวนับสินทรัพย์อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e2b68-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e2b68-104">ในส่วนก่อนหน้านี้ การลงทะเบียนด้วยตนเองของตัวนับสินทรัพย์จะถูกอธิบายไว้</span><span class="sxs-lookup"><span data-stu-id="e2b68-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="e2b68-105">การตั้งค่าของตัวนับสินทรัพย์จะถูกอธิบายใน [ตัวนับ](../setup-for-objects/counters.md)</span><span class="sxs-lookup"><span data-stu-id="e2b68-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="e2b68-106">ค่าตัวนับยังสามารถได้รับการอัพเดตจากการลงทะเบียนการผลิตโดยอัตโนมัติ ตามชั่วโมงการผลิตหรือปริมาณการผลิต</span><span class="sxs-lookup"><span data-stu-id="e2b68-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="e2b68-107">ซึ่งกระทำใน **อัพเดตตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e2b68-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="e2b68-108">คุณสามารถอัพเดตหนึ่งสินทรัพย์หรือหลายสินทรัพย์ได้โดยการแทรกหนึ่งพารามิเตอร์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e2b68-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="e2b68-109">พารามิเตอร์นี้ระบุวันที่เริ่มต้นสำหรับการลงทะเบียนการผลิต (ชั่วโมงหรือปริมาณที่ผลิต) ซึ่งหมายความว่าวันที่เริ่มต้นจากค่าตัวนับควรได้รับการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="e2b68-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="e2b68-110">สินทรัพย์ทั้งหมดที่เกี่ยวข้องกับทรัพยากร *และ* มีตัวนับสินทรัพย์ ซึ่งมีการตั้งค่าให้อัพเดตโดยยึดตามปริมาณที่ผลิตหรือชั่วโมงการผลิต จะถูกรวมไว้ในการอัพเดตอัตโนมัติ และจะมีการสร้างค่าตัวนับใหม่</span><span class="sxs-lookup"><span data-stu-id="e2b68-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="e2b68-111">สำหรับตัวนับตามปริมาณการผลิต ปริมาณสินค้าที่ดีและปริมาณสินค้าที่บกพร่องที่ลงทะเบียนจะรวมอยู่ในการตรวจนับ</span><span class="sxs-lookup"><span data-stu-id="e2b68-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="e2b68-112">ถ้าหน่วยที่ใช้สำหรับการลงทะเบียนปริมาณที่ผลิตแตกต่างจากหน่วยที่ใช้ในตัวนับ ปริมาณจะถูกแปลงให้สอดคล้องกับหน่วยตัวนับ</span><span class="sxs-lookup"><span data-stu-id="e2b68-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="e2b68-113">ดังกล่าวข้างต้น ตัวนับอัตโนมัติสามารถได้รับการอัพเดตจากการลงทะเบียนการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="e2b68-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="e2b68-114">ดังนั้น สินทรัพย์ที่คุณต้องการให้อัพเดตตัวนับโดยอัตโนมัติต้องสัมพันธ์กับทรัพยากร (เครื่องจักร)</span><span class="sxs-lookup"><span data-stu-id="e2b68-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="e2b68-115">คำอธิบายต่อไปนี้แสดงภาพรวมของการตั้งค่าและการประมวลผลของใบสั่งผลิต (ในโมดูล **การควบคุมการผลิต** ) ซึ่งใช้เป็นข้อมูลพื้นฐานสำหรับการอัพเดตตัวนับโดยอัตโนมัติบนสินทรัพย์ในโมดูล **การบริหารสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e2b68-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="e2b68-116">เมื่อปริมาณที่ผลิตหรือชั่วโมงการผลิตได้รับการลงทะเบียนในทรัพยากรแล้ว คุณสามารถอัพเดตตัวนับสินทรัพย์ที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="e2b68-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="e2b68-117">คลิก **การจัดการสินทรัพย์** > **ประจำงวด** > **สินทรัพย์** > **อัพเดตตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e2b68-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="e2b68-118">เลือกวันที่เริ่มต้นของการอัพเดตอัตโนมัติในฟิลด์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e2b68-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="e2b68-119">วันที่ในฟิลด์นี้เป็นวันที่ "งานระหว่างทำ" จาก **ธุรกรรมกระบวนการผลิต** (**การควบคุมการผลิต** > **การสอบถามและรายงาน** > **การผลิต** > **ธุรกรรมกระบวนการผลิต** > ฟิลด์**วันที่ทางกายภาพ** )</span><span class="sxs-lookup"><span data-stu-id="e2b68-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="e2b68-120">ถ้าคุณต้องการเลือกสินทรัพย์ ชนิดสินทรัพย์ หรือทรัพยากรเฉพาะสำหรับการอัพเดตอัตโนมัติ ให้คลิก **ตัวกรอง** บน **เรกคอร์ดเพื่อรวม** แท็บด่วน แล้วทำการเลือกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e2b68-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="e2b68-121">ถ้าจำเป็น คุณสามารถตั้งค่าการอัพเดตโดยอัตโนมัติเป็นชุดงานได้บนแท็บด่วน **รันในแบบเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="e2b68-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![รูปที่ 1](media/12-work-orders.png)

5. <span data-ttu-id="e2b68-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e2b68-123">Click **OK**.</span></span> <span data-ttu-id="e2b68-124">เมื่อการอัพเดตตัวนับสินทรัพย์อัตโนมัติเสร็จสมบูรณ์ คุณสามารถดูการลงทะเบียนตัวนับที่เกี่ยวข้องกับสินทรัพย์ใน **ตัวนับสินทรัพย์** (**การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด** > เลือกสินทรัพย์ > ปุ่ม **ตัวนับ** )</span><span class="sxs-lookup"><span data-stu-id="e2b68-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="e2b68-125">ใน **ผลรวมตัวนับสินทรัพย์** คุณสามารถดูภาพรวมของการลงทะเบียนล่าสุดที่ทำบนชนิดตัวนับทั้งหมดในสินทรัพย์ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="e2b68-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="e2b68-126">คลิก **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **มูลค่ารวมของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e2b68-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="e2b68-127">มุมมองนี้คล้ายกับ **ตัวนับสินทรัพย์** แต่คุณไม่สามารถเพิ่มหรือแก้ไขการลงทะเบียนใน **มูลค่ารวมของสินทรัพย์ได้**</span><span class="sxs-lookup"><span data-stu-id="e2b68-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="e2b68-128">สำหรับภาพรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e2b68-128">It is for overview only.</span></span>

![รูปที่ 2](media/13-work-orders.png)


- <span data-ttu-id="e2b68-130">อย่างไรก็ตาม คุณยังสามารถสร้างการลงทะเบียนค่าตัวนับด้วยตนเองสำหรับชนิดตัวนับที่มีการอัพเดตโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="e2b68-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="e2b68-131">อ้างอิงถึงส่วน "การอัพเดตตัวนับสินทรัพย์ด้วยตนเอง" สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e2b68-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="e2b68-132">คุณสามารถตั้งค่าตัวนับที่เกี่ยวข้องกับตัวนับอื่น ซึ่งหมายความว่าเมื่อมีการอัพเดตตัวนับ ตัวนับที่เกี่ยวข้องจะมีการอัพเดตโดยอัตโนมัติในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e2b68-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="e2b68-133">อ้างอิงถึง [ตัวนับ](../setup-for-objects/counters.md) เกี่ยวกับการตั้งค่าตัวนับที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e2b68-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
