---
title: สร้างลำดับชั้นการจำลององค์กรขององค์กร B2B
description: หัวข้อนี้จะอธิบายวิธีการสร้างลำดับชั้นการจำลององค์กรขององค์กรระหว่างธุรกิจ (B2B)
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799840"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="cedf2-103">สร้างลำดับชั้นการจำลององค์กรขององค์กร B2B</span><span class="sxs-lookup"><span data-stu-id="cedf2-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cedf2-104">หัวข้อนี้อธิบายวิธีการสร้างลำดับชั้นการจำลององค์กรขององค์กรระหว่างธุรกิจ (B2B) ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cedf2-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cedf2-105">ในศูนย์ควบคุม Commerce องค์กรคู่ค้าทางธุรกิจจะแสดงโดยเอนทิตีลำดับชั้นของลูกค้าและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="cedf2-106">องค์กรคู่ค้าทางธุรกิจและผู้ใช้ของคู่ค้าแสดงเป็นลูกค้า และลำดับชั้นของลูกค้าจะใช้ในการเชื่อมโยงลูกค้าเหล่านั้นกับลูกค้ารายอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="cedf2-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="cedf2-107">เมื่อคำขอคู่ค้าทางธุรกิจเพื่อเข้าร่วมไซต์อีคอมเมิร์ซของ B2B ได้รับการอนุมัติ การขั้นตอนต่อไปนี้จะ:</span><span class="sxs-lookup"><span data-stu-id="cedf2-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="cedf2-108">เรกคอร์ดลูกค้าใหม่สองเรกคอร์ดจะถูกสร้างขึ้นในระบบ: เรกคอร์ดลูกค้าที่ **ชนิดองค์กร** สำหรับองค์กรคู่ค้าธุรกิจและเรกคอร์ดลูกค้า **ชนิดบุคคล** สำหรับผู้ขอ (คือผู้ใช้ที่เป็นคู่ค้าธุรกิจที่ส่งคำขอ)</span><span class="sxs-lookup"><span data-stu-id="cedf2-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="cedf2-109">เรกคอร์ดลำดับชั้นของลูกค้าใหม่จะถูกสร้างขึ้นภายใต้ **ลูกค้า \> ลำดับชั้นของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="cedf2-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="cedf2-110">เรกคอร์ดนี้มีคุณสมบัติส่วนหัวต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cedf2-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="cedf2-111">**รหัสลำดับชั้นของลูกค้า** – รหัสเฉพาะของลำดับชั้นของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="cedf2-112">รหัสนี้ใช้ลำดับหมายเลขที่กําหนดในพารามิเตอร์ที่ใช้ร่วมกันของ Commerce ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="cedf2-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="cedf2-113">**ชื่อ** – ชื่อองค์กรของคู่ค้าธุรกิจ ตามที่ระบุในการร้องขอการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="cedf2-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="cedf2-114">**วัตถุประสงค์** – คุณสมบัตินี้ตั้งค่าเป็น **องค์กร B2B** ค่าที่กําหนดล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="cedf2-115">**องค์กร** – รหัสลูกค้าของคู่ค้าธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="cedf2-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="cedf2-116">ต่อไปนี้เป็นรายละเอียดของเรกคอร์ดลำดับชั้นของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="cedf2-117">เรกคอร์ดลูกค้าของผู้ขอสัมพันธ์กับลำดับชั้นของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="cedf2-118">บทบาทผู้ดูแลระบบสัมพันธ์กับผู้ขอ</span><span class="sxs-lookup"><span data-stu-id="cedf2-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="cedf2-119">เมื่อผู้ดูแลระบบเพิ่มผู้ใช้เพิ่มเติมให้กับองค์กรคู่ค้าทางธุรกิจบนไซต์ B2B เรกคอร์ดลูกค้าใหม่ของผู้ใช้แต่ละคนจะถูกสร้างขึ้นในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="cedf2-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="cedf2-120">นอกจากนี้ เรกคอร์ดลูกค้านี้ยังถูกเพิ่มเข้าในเรกคอร์ดลำดับชั้นของลูกค้าที่เกี่ยวข้องของคู่ค้าธุรกิจด้วย และมีบทบาทของ "ผู้ใช้"</span><span class="sxs-lookup"><span data-stu-id="cedf2-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="cedf2-121">โดยส่วนใหญ่ ค่าคุณสมบัติที่สอดคล้องกันของเรกคอร์ดลูกค้าทั้งหมดในลำดับชั้นควรตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cedf2-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="cedf2-122">ตัวอย่างเช่น เนื่องจากผู้ใช้คู่ค้าทางธุรกิจทั้งหมดควรได้รับราคาที่คล้ายกันของผลิตภัณฑ์ กลุ่มราคา และการตั้งค่าคอนฟิกที่เกี่ยวข้องควรตรงกัน</span><span class="sxs-lookup"><span data-stu-id="cedf2-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="cedf2-123">อย่างไรก็ตาม ระบบไม่ได้บังคับใช้ความสอดคล้องกันนี้</span><span class="sxs-lookup"><span data-stu-id="cedf2-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="cedf2-124">ดังนั้น ผู้ใช้ศูนย์ควบคุม Commerce ที่เกี่ยวข้องจึงรับผิดชอบในการตรวจสอบให้แน่ใจว่าค่าคุณสมบัติและการตั้งค่าคอนฟิกตรงกับลูกค้าทั้งหมดในลำดับชั้นที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="cedf2-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="cedf2-125">ผู้ใช้ศูนย์ควบคุม Commerce สามารถดูค่าคุณสมบัติต่างๆ ของเรกคอร์ดลูกค้าทั้งหมดในลำดับชั้นในมุมมองแบบทีละขั้นตอนได้</span><span class="sxs-lookup"><span data-stu-id="cedf2-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="cedf2-126">เลือกคุณสมบัติของเรกคอร์ดลูกค้าที่เกี่ยวข้อง โดยการเลือกชื่อแท็บบนเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="cedf2-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="cedf2-127">ผู้ใช้สามารถดูและแก้ไขค่าคุณสมบัติจากมุมมองนี้โดยตรงได้</span><span class="sxs-lookup"><span data-stu-id="cedf2-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="cedf2-128">หรือถ้าคุณต้องการใช้ค่าทั้งหมดจากเรกคอร์ดลูกค้าของผู้ดูแลระบบกับเรกคอร์ดลูกค้าผู้ใช้ทั้งหมด ให้เลือก **แทนที่** ในรายละเอียดลำดับชั้นของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="cedf2-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cedf2-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cedf2-129">Additional resources</span></span>

[<span data-ttu-id="cedf2-130">ตั้งค่าไซต์อีคอมเมิร์ซ B2B</span><span class="sxs-lookup"><span data-stu-id="cedf2-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="cedf2-131">จัดการผู้ใช้คู่ค้าทางธุรกิจบนไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="cedf2-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="cedf2-132">ตั้งค่าคอนฟิกวิธีการชำระเงินด้วยบัญชีลูกค้าสำหรับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="cedf2-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="cedf2-133">ตั้งค่าขีดจํากัดปริมาณผลิตภัณฑ์เกี่ยวกับไซต์อีคอมเมิร์ซของ B2B</span><span class="sxs-lookup"><span data-stu-id="cedf2-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]