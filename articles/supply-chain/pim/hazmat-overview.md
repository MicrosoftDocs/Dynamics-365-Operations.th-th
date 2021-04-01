---
title: ภาพรวมของวัตถุอันตราย
description: หัวข้อนี้แสดงภาพรวมของคุณลักษณะที่เกี่ยวข้องกับการจัดการและการจัดทำเอกสารวัตถุอันตรายระหว่างการจัดการข้อมูลผลิตภัณฑ์และการจัดการคลังสินค้า
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 4ff997214f80d97f6e558d32fbf66663cbc84143
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231899"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="80f36-103">ภาพรวมของวัตถุอันตราย</span><span class="sxs-lookup"><span data-stu-id="80f36-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="80f36-104">เพื่อให้ยังคงเป็นไปตามกฎระเบียบการจัดส่งและการขนส่ง องค์กรที่จัดส่งวัตถุที่จัดประเภทเป็นสินค้าอันตรายต้องมีเอกสารเพิ่มเติมพร้อมกับการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="80f36-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="80f36-105">คุณลักษณะวัตถุอันตรายให้ลูกค้าจัดเก็บข้อมูลที่เกี่ยวข้องกับสินค้าที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="80f36-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="80f36-106">คุณสามารถใช้ข้อมูลนี้เพื่อช่วยจัดเตรียมเอกสารการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="80f36-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="80f36-107">องค์กรที่จัดส่งสินค้าอันตรายต้องมีกระบวนการและขั้นตอนของตนเองสำหรับการจัดการกระบวนการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="80f36-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="80f36-108">Microsoft Dynamics 365 Supply Chain Management เป็นเพียงเครื่องมือที่จะช่วยในการสร้างเอกสารที่จำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="80f36-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="80f36-109">แผนภาพต่อไปนี้แสดงให้เห็นถึงขั้นตอนที่จำเป็นในการตั้งค่าและใช้คุณลักษณะวัตถุอันตราย</span><span class="sxs-lookup"><span data-stu-id="80f36-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="80f36-110">![การตั้งค่าและใช้งานคุณลักษณะวัตถุอันตราย](media/hazmat-overview.png "การตั้งค่าและใช้งานคุณลักษณะวัตถุอันตราย")</span><span class="sxs-lookup"><span data-stu-id="80f36-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="80f36-111">คุณลักษณะวัตถุอันตรายตั้งค่าในการจัดการข้อมูลผลิตภัณฑ์และจัดเตรียมเอกสารที่สามารถพิมพ์ผ่านทางการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="80f36-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="80f36-112">ดังนั้น เมื่อพูดอย่างกว้างๆ การดำเนินการเหล่านั้นเป็นสองส่วนหลักที่คุณจะตรวจสอบ ตั้งค่า และใช้ฟังก์ชันของคุณลักษณะนี้:</span><span class="sxs-lookup"><span data-stu-id="80f36-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="80f36-113">**การจัดการข้อมูลผลิตภัณฑ์** – ตั้งค่ารหัสที่สามารถใช้กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="80f36-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="80f36-114">**การจัดการคลังสินค้า** – ทำงานกับเอกสารการจัดส่งเพิ่มเติมที่จะพิมพ์สำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="80f36-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80f36-115">คุณลักษณะวัตถุอันตรายใน Supply Chain Management มีคอลเลกชันของฟิลด์ข้อมูลผลิตภัณฑ์ที่มีประโยชน์และฟังก์ชันที่เกี่ยวข้อง ซึ่งช่วยให้คุณสามารถบันทึกและอ้างอิงข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์อันตรายของคุณได้</span><span class="sxs-lookup"><span data-stu-id="80f36-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="80f36-116">คุณลักษณะเหล่านี้ยังสามารถช่วยให้คุณออกแบบและพิมพ์เอกสารการจัดส่งที่รวมข้อมูลบางอย่างที่เหมือนกันเกี่ยวกับวัตถุอันตรายใดๆ ที่คุณกำลังจัดส่งได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="80f36-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="80f36-117">อย่างไรก็ตาม ระบบจะไม่เป็นไปตามกฎระเบียบที่บังคับใช้ทั้งหมดของประเทศหรือภูมิภาคของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="80f36-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="80f36-118">ถึงแม้ว่าเครื่องมือเหล่านี้มีวัตถุประสงค์เพื่อช่วยคุณในการปฏิบัติตามกฎระเบียบทั่วไป แต่จะไม่เพียงพอหรือไม่มีการรับประกันถึงการเป็นไปตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="80f36-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="80f36-119">องค์กรของคุณเป็นผู้รับผิดชอบในการรับทราบถึงกฎระเบียบที่เกี่ยวข้องทั้งหมดและดำเนินการตามขั้นตอนทั้งหมดที่จำเป็นในการปฏิบัติตาม</span><span class="sxs-lookup"><span data-stu-id="80f36-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="80f36-120">การจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="80f36-120">Product information management</span></span>

<span data-ttu-id="80f36-121">การจัดการข้อมูลผลิตภัณฑ์มีช่วงของตารางการตั้งค่าที่คุณสามารถป้อนข้อมูลอ้างอิงสำหรับรายการสินค้าอันตรายสำหรับการขนส่งทางถนน ทางอากาศ และทางทะเล</span><span class="sxs-lookup"><span data-stu-id="80f36-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="80f36-122">ข้อกำหนดทั่วไปต่อไปนี้ได้รับการอ้างอิงเมื่อมีการพัฒนาฟังก์ชันนี้:</span><span class="sxs-lookup"><span data-stu-id="80f36-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="80f36-123">**ADR** – ข้อบังคับที่เกี่ยวข้องกับการขนส่งระหว่างประเทศของสินค้าอันตรายตามถนน</span><span class="sxs-lookup"><span data-stu-id="80f36-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="80f36-124">**CFR 49** – ข้อบังคับในสหรัฐอเมริกาสำหรับการขนส่งสินค้าอันตราย</span><span class="sxs-lookup"><span data-stu-id="80f36-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="80f36-125">**IMDG** – รหัสสินค้าอันตรายทางทะเลระหว่างประเทศ (IMDG)</span><span class="sxs-lookup"><span data-stu-id="80f36-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="80f36-126">**IATA** – ข้อบังคับของสินค้าอันตรายสำหรับสมาคมขนส่งทางอากาศระหว่างประเทศ (IATA)</span><span class="sxs-lookup"><span data-stu-id="80f36-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="80f36-127">แต่ละชุดของกฎระเบียบมีรายการมาตรฐานของสินค้าอันตรายและรหัสการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="80f36-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="80f36-128">ดังนั้น Supply Chain Management จึงมีตารางอ้างอิงสำหรับรหัสที่ใช้กันทั่วไปในรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="80f36-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="80f36-129">แต่ละรายการจะมีรหัสเฉพาะบางส่วนที่คุณสามารถกำหนดได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="80f36-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="80f36-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่ากฎระเบียบและค่าสำหรับวัตถุอันตราย และวิธีการกำหนดค่าให้กับผลิตภัณฑ์ที่เกี่ยวข้อง ให้ดูที่หัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80f36-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="80f36-131">ตั้งค่าวัตถุอันตราย</span><span class="sxs-lookup"><span data-stu-id="80f36-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="80f36-132">วัตถุอันตรายในผลิตภัณฑ์ ใบสั่ง การจัดส่ง และการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="80f36-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="80f36-133">การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="80f36-133">Warehouse management</span></span>

<span data-ttu-id="80f36-134">เมื่อคุณจัดเตรียมการจัดส่งในการจัดการคลังสินค้า คุณจะสามารถพิมพ์รายงานใหม่ได้หลายฉบับ ซึ่งใช้ข้อมูลที่คุณตั้งค่าไว้ในการจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="80f36-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="80f36-135">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายงานที่มีอยู่และวิธีการใช้รายงาน ให้ดูที่ [การสอบถามและรายงานเกี่ยวกับวัตถุอันตราย](hazmat-reports.md)</span><span class="sxs-lookup"><span data-stu-id="80f36-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]