---
title: " ตั้งค่ากฎและพารามิเตอร์สำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก"
description: 'ขั้นตอนนี้จะสาธิตขั้นตอนสร้างกฎการเพิ่มเติมสินค้า '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141151"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="a3a8f-103"> ตั้งค่ากฎและพารามิเตอร์สำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก</span><span class="sxs-lookup"><span data-stu-id="a3a8f-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3a8f-104">ขั้นตอนนี้จะสาธิตขั้นตอนสร้างกฎการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="a3a8f-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="a3a8f-105">กฎการเพิ่มเติมสินค้าสามารถใช้เพื่อควบคุมวิธีการกระจายผลิตภัณฑ์ไปยังร้านค้าเมื่อใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก </span><span class="sxs-lookup"><span data-stu-id="a3a8f-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="a3a8f-106">กฎการเติมสินค้าสามารถถูกตั้งค่าให้กับร้านค้าหรือกลุ่มร้านค้าได้ </span><span class="sxs-lookup"><span data-stu-id="a3a8f-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="a3a8f-107">น้ำหนักที่กำหนดไว้สำหรับแต่ละบรรทัดรายการในกฎจะควบคุมวิธีที่ปริมาณของผลิตภัณฑ์นั้นถูกกระจายระหว่างร้านค้าเมื่อใช้กฎการเพิ่มเติมสินค้าเป็นวิธีการกระจายในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก </span><span class="sxs-lookup"><span data-stu-id="a3a8f-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="a3a8f-108">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="a3a8f-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="a3a8f-109">ไปที่กฎการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="a3a8f-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="a3a8f-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a3a8f-110">Click New.</span></span>
3. <span data-ttu-id="a3a8f-111">ในฟิลด์กฎการเพิ่มเติมสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="a3a8f-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="a3a8f-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a3a8f-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3a8f-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a3a8f-113">Click Save.</span></span>
6. <span data-ttu-id="a3a8f-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3a8f-114">Click Add.</span></span>
7. <span data-ttu-id="a3a8f-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a3a8f-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a3a8f-116">คุณสามารถเลือกลำดับชั้นการเพิ่มเติมสินค้าหรือช่องทางสำหรับชนิดนี้ </span><span class="sxs-lookup"><span data-stu-id="a3a8f-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="a3a8f-117">ค่าจะควบคุมว่าการเลือกด้วยชื่อจะเป็นลำดับชั้นของช่องทางหรือช่องทางเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="a3a8f-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="a3a8f-118">สำหรับตัวอย่างนี้ ปล่อยให้ตั้งค่าเป็นลำดับชั้นการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="a3a8f-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="a3a8f-119">ในฟิลด์ชื่อ ให้เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a3a8f-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="a3a8f-120">ค่าน้ำหนักเริ่มต้นได้มาจากน้ำหนักที่กำหนดไว้ในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="a3a8f-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="a3a8f-121">น้ำหนักนี้สามารถใช้สำหรับกฎการเพิ่มเติมสินค้าหรือคุณสามารถป้อนน้ำหนักใหม่ในฟิลด์น้ำหนัก </span><span class="sxs-lookup"><span data-stu-id="a3a8f-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="a3a8f-122">ในฟิลด์น้ำหนัก ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="a3a8f-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="a3a8f-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="a3a8f-123">Click Add.</span></span>
11. <span data-ttu-id="a3a8f-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a3a8f-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="a3a8f-125">ในฟิลด์ชนิด เลือก 'ช่องทาง' </span><span class="sxs-lookup"><span data-stu-id="a3a8f-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="a3a8f-126">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a3a8f-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="a3a8f-127">ในฟิลด์น้ำหนัก ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="a3a8f-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="a3a8f-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="a3a8f-128">Click Save.</span></span>

