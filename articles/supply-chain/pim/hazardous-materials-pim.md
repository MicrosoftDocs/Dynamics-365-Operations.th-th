---
title: วัตถุอันตราย
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับเอกสารและข้อมูลวัตถุอันตรายซึ่งจัดเก็บไว้ในสภาพแวดล้อมของคุณ
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979051"
---
# <a name="hazardous-materials"></a><span data-ttu-id="1c3b9-103">วัตถุอันตราย</span><span class="sxs-lookup"><span data-stu-id="1c3b9-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1c3b9-104">ข้อมูลเกี่ยวกับวัตถุอันตรายถูกตั้งค่าในการจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1c3b9-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="1c3b9-105">โมดูลนี้ยังมีเอกสารที่สามารถพิมพ์ได้โดยใช้การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="1c3b9-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="1c3b9-106">เมื่อคุณจัดส่งวัสดุที่จัดประเภทเป็นสินค้าอันตรายเอกสารเพิ่มเติมจะต้องรวมไปในการจัดส่งนั้น</span><span class="sxs-lookup"><span data-stu-id="1c3b9-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="1c3b9-107">ฟังก์ชันของวัตถุอันตรายช่วยให้ลูกค้าจัดเก็บข้อมูลการจัดประเภทและสัมพันธ์ข้อมูลการจัดประเภทกับการนำสินค้าออกใช้</span><span class="sxs-lookup"><span data-stu-id="1c3b9-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="1c3b9-108">คุณสามารถใช้ข้อมูลนี้เพื่อช่วยจัดเตรียมเอกสารการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="1c3b9-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c3b9-109">คุณลักษณะวัตถุอันตรายใน Microsoft Dynamics 365 Supply Chain Management มีคอลเลกชันของฟิลด์ข้อมูลผลิตภัณฑ์ที่มีประโยชน์และฟังก์ชันที่เกี่ยวข้อง ซึ่งช่วยให้คุณสามารถบันทึกและอ้างอิงข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์อันตรายของคุณได้</span><span class="sxs-lookup"><span data-stu-id="1c3b9-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="1c3b9-110">คุณลักษณะเหล่านี้ยังสามารถช่วยให้คุณออกแบบและพิมพ์เอกสารการจัดส่งที่รวมข้อมูลบางอย่างที่เหมือนกันเกี่ยวกับวัตถุอันตรายใดๆ ที่คุณกำลังจัดส่งได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="1c3b9-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="1c3b9-111">อย่างไรก็ตาม ระบบจะไม่เป็นไปตามกฎระเบียบที่บังคับใช้ทั้งหมดของประเทศหรือภูมิภาคของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1c3b9-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="1c3b9-112">ถึงแม้ว่าเครื่องมือเหล่านี้มีวัตถุประสงค์เพื่อช่วยคุณในการปฏิบัติตามกฎระเบียบทั่วไป แต่จะไม่เพียงพอหรือไม่มีการรับประกันถึงการเป็นไปตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="1c3b9-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="1c3b9-113">องค์กรของคุณเป็นผู้รับผิดชอบในการรับทราบถึงกฎระเบียบที่เกี่ยวข้องทั้งหมดและดำเนินการตามขั้นตอนทั้งหมดที่จำเป็นในการปฏิบัติตาม</span><span class="sxs-lookup"><span data-stu-id="1c3b9-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="1c3b9-114">ก่อนที่คุณจะสามารถใช้ฟังก์ชันนี้ได้ต้องมีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1c3b9-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="1c3b9-115">**การจัดการข้อมูลผลิตภัณฑ์** : ตั้งค่ารหัสที่สามารถใช้กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="1c3b9-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="1c3b9-116">**การจัดการคลังสินค้า:** ใช้เอกสารการจัดส่งเพิ่มเติมเพื่อพิมพ์ข้อมูลการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="1c3b9-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="1c3b9-117">การจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1c3b9-117">Product information management</span></span>

<span data-ttu-id="1c3b9-118">ในการจัดการข้อมูลผลิตภัณฑ์มีช่วงของตารางการตั้งค่าที่คุณสามารถเพิ่มข้อมูลอ้างอิงที่ระบุไว้ในรายการสินค้าอันตรายสำหรับการขนส่งทางถนน ทางอากาศ และทางทะเล</span><span class="sxs-lookup"><span data-stu-id="1c3b9-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="1c3b9-119">นี่คือบางข้อบังคับที่ถูกอ้างอิงบ่อยครั้ง:</span><span class="sxs-lookup"><span data-stu-id="1c3b9-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="1c3b9-120">**ADR** – ข้อบังคับที่เกี่ยวข้องกับการขนส่งระหว่างประเทศของสินค้าอันตรายตามถนน</span><span class="sxs-lookup"><span data-stu-id="1c3b9-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="1c3b9-121">**CFR 49** – ข้อบังคับในสหรัฐอเมริกาสำหรับการขนส่งสินค้าอันตราย</span><span class="sxs-lookup"><span data-stu-id="1c3b9-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="1c3b9-122">**IMDG** – รหัสสินค้าอันตรายทางทะเลระหว่างประเทศ (IMDG)</span><span class="sxs-lookup"><span data-stu-id="1c3b9-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="1c3b9-123">**IATA** – ข้อบังคับของสินค้าอันตรายสำหรับสมาคมขนส่งทางอากาศระหว่างประเทศ (IATA)</span><span class="sxs-lookup"><span data-stu-id="1c3b9-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="1c3b9-124">แต่ละข้อบังคับเหล่านี้จะมีรายการสินค้าอันตรายที่รวมรหัสอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="1c3b9-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="1c3b9-125">รายการสำหรับการขนส่งแต่ละชนิดจะรวมอยู่ในการจัดประเภทระหว่างประเทศที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1c3b9-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="1c3b9-126">Supply Chain Management มีตารางอ้างอิงสำหรับรหัสที่ใช้ร่วมกันในรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c3b9-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="1c3b9-127">แต่ละรายการจะมีบางรหัสเฉพาะที่คุณสามารถกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="1c3b9-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="1c3b9-128">เมื่อต้องการเริ่มต้นการตั้งค่าคอนฟิกข้อมูลนี้ให้สร้างข้อบังคับที่คุณสามารถใช้เพื่อตั้งค่าคอนฟิกพารามิเตอร์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="1c3b9-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="1c3b9-129">การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="1c3b9-129">Warehouse management</span></span>

<span data-ttu-id="1c3b9-130">เมื่อการจัดส่งมีการเตรียมไว้รายงานใหม่จะสามารถพิมพ์ได้หลายฉบับ</span><span class="sxs-lookup"><span data-stu-id="1c3b9-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="1c3b9-131">รายงานเหล่านี้จะใช้ข้อมูลที่คุณตั้งค่าไว้ในการจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1c3b9-131">These reports use the information that you set up in Product information management.</span></span>
