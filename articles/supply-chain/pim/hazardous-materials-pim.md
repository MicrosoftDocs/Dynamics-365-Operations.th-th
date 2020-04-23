---
title: วัตถุอันตราย
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับเอกสารและข้อมูลวัสดุที่เป็นอันตรายซึ่งจัดเก็บไว้ในสภาพแวดล้อมของคุณ
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
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208481"
---
# <a name="hazardous-materials"></a><span data-ttu-id="8ad1b-103">วัตถุอันตราย</span><span class="sxs-lookup"><span data-stu-id="8ad1b-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ad1b-104">ข้อมูลเกี่ยวกับวัสดุที่เป็นอันตรายถูกตั้งค่าในการจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad1b-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="8ad1b-105">โมดูลนี้ยังมีเอกสารที่สามารถพิมพ์ได้โดยใช้การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="8ad1b-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="8ad1b-106">เมื่อคุณจัดส่งวัสดุที่จัดประเภทเป็นสินค้าอันตรายเอกสารเพิ่มเติมจะต้องรวมไปในการจัดส่งนั้น</span><span class="sxs-lookup"><span data-stu-id="8ad1b-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="8ad1b-107">ฟังก์ชันของวัสดุที่เป็นอันตรายช่วยให้ลูกค้าจัดเก็บข้อมูลการจัดประเภทและสัมพันธ์ข้อมูลการจัดประเภทกับการนำสินค้าออกใช้</span><span class="sxs-lookup"><span data-stu-id="8ad1b-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="8ad1b-108">คุณสามารถใช้ข้อมูลนี้เพื่อช่วยจัดเตรียมเอกสารการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="8ad1b-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ad1b-109">เพื่อช่วยในการจัดการการจัดส่งที่เป็นอันตราย Microsoft Dynamics 365 Supply Chain Management จะช่วยให้คุณสามารถตั้งค่าข้อมูลอ้างอิงเพิ่มเติมที่เกี่ยวข้องกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad1b-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="8ad1b-110">นอกจากนี้คุณยังสามารถตั้งค่าเอกสารการจัดส่งเพิ่มเติมได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8ad1b-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="8ad1b-111">อย่างไรก็ตามระบบจะเป็นไปตามกฎระเบียบข้อบังคบของประเทศหรือภูมิภาคของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8ad1b-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="8ad1b-112">แทนที่จะเป็นเครื่องมือที่จะช่วยโปรแกรมโดยรวมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8ad1b-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="8ad1b-113">ก่อนที่คุณจะสามารถใช้ฟังก์ชันนี้ได้ต้องมีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8ad1b-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="8ad1b-114">**การจัดการข้อมูลผลิตภัณฑ์** : ตั้งค่ารหัสที่สามารถใช้กับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="8ad1b-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="8ad1b-115">**การจัดการคลังสินค้า:** ใช้เอกสารการจัดส่งเพิ่มเติมเพื่อพิมพ์ข้อมูลการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8ad1b-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="8ad1b-116">การจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad1b-116">Product information management</span></span>

<span data-ttu-id="8ad1b-117">ในการจัดการข้อมูลผลิตภัณฑ์มีช่วงของตารางการตั้งค่าที่คุณสามารถเพิ่มข้อมูลอ้างอิงที่ระบุไว้ในรายการสินค้าอันตรายสำหรับการขนส่งทางถนน ทางอากาศ และทางทะเล</span><span class="sxs-lookup"><span data-stu-id="8ad1b-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="8ad1b-118">นี่คือบางข้อบังคับที่ถูกอ้างอิงบ่อยครั้ง:</span><span class="sxs-lookup"><span data-stu-id="8ad1b-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="8ad1b-119">**ADR** – ข้อบังคับที่เกี่ยวข้องกับการขนส่งระหว่างประเทศของสินค้าอันตรายตามถนน</span><span class="sxs-lookup"><span data-stu-id="8ad1b-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="8ad1b-120">**CFR 49** – ข้อบังคับในสหรัฐอเมริกาสำหรับการขนส่งสินค้าอันตราย</span><span class="sxs-lookup"><span data-stu-id="8ad1b-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="8ad1b-121">**IMDG** – รหัสสินค้าอันตรายทางทะเลระหว่างประเทศ (IMDG)</span><span class="sxs-lookup"><span data-stu-id="8ad1b-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="8ad1b-122">**IATA** – ข้อบังคับของสินค้าที่เป็นอันตรายสำหรับสมาคมขนส่งทางอากาศระหว่างประเทศ (IATA)</span><span class="sxs-lookup"><span data-stu-id="8ad1b-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="8ad1b-123">แต่ละข้อบังคับเหล่านี้จะมีรายการสินค้าอันตรายที่รวมรหัสอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="8ad1b-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="8ad1b-124">รายการสำหรับการขนส่งแต่ละชนิดจะรวมอยู่ในการจัดประเภทระหว่างประเทศที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="8ad1b-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="8ad1b-125">Supply Chain Management มีตารางอ้างอิงสำหรับรหัสที่ใช้ร่วมกันในรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="8ad1b-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="8ad1b-126">แต่ละรายการจะมีบางรหัสเฉพาะที่คุณสามารถกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="8ad1b-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="8ad1b-127">เมื่อต้องการเริ่มต้นการตั้งค่าคอนฟิกข้อมูลนี้ให้สร้างข้อบังคับที่คุณสามารถใช้เพื่อตั้งค่าคอนฟิกพารามิเตอร์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8ad1b-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="8ad1b-128">การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="8ad1b-128">Warehouse management</span></span>

<span data-ttu-id="8ad1b-129">เมื่อการจัดส่งมีการเตรียมไว้รายงานใหม่จะสามารถพิมพ์ได้หลายฉบับ</span><span class="sxs-lookup"><span data-stu-id="8ad1b-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="8ad1b-130">รายงานเหล่านี้จะใช้ข้อมูลที่คุณตั้งค่าไว้ในการจัดการข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8ad1b-130">These reports use the information that you set up in Product information management.</span></span>
