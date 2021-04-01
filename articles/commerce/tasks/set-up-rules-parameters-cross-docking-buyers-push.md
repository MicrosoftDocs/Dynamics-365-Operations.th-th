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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d4cd276283483340f1dc0bc995cc9073a8aa9c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232700"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="6ae83-103"> ตั้งค่ากฎและพารามิเตอร์สำหรับการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก</span><span class="sxs-lookup"><span data-stu-id="6ae83-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ae83-104">ขั้นตอนนี้จะสาธิตขั้นตอนสร้างกฎการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="6ae83-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="6ae83-105">กฎการเพิ่มเติมสินค้าสามารถใช้เพื่อควบคุมวิธีการกระจายผลิตภัณฑ์ไปยังร้านค้าเมื่อใช้การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก </span><span class="sxs-lookup"><span data-stu-id="6ae83-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="6ae83-106">กฎการเติมสินค้าสามารถถูกตั้งค่าให้กับร้านค้าหรือกลุ่มร้านค้าได้ </span><span class="sxs-lookup"><span data-stu-id="6ae83-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="6ae83-107">น้ำหนักที่กำหนดไว้สำหรับแต่ละบรรทัดรายการในกฎจะควบคุมวิธีที่ปริมาณของผลิตภัณฑ์นั้นถูกกระจายระหว่างร้านค้าเมื่อใช้กฎการเพิ่มเติมสินค้าเป็นวิธีการกระจายในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าและการจัดส่งสินค้าแบบผลัก </span><span class="sxs-lookup"><span data-stu-id="6ae83-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="6ae83-108">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="6ae83-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="6ae83-109">ไปที่กฎการเพิ่มเติมสินค้า </span><span class="sxs-lookup"><span data-stu-id="6ae83-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="6ae83-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6ae83-110">Click New.</span></span>
3. <span data-ttu-id="6ae83-111">ในฟิลด์กฎการเพิ่มเติมสินค้า ให้พิมพ์ค่าใดค่าหนึ่ง </span><span class="sxs-lookup"><span data-stu-id="6ae83-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="6ae83-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6ae83-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6ae83-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ae83-113">Click Save.</span></span>
6. <span data-ttu-id="6ae83-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ae83-114">Click Add.</span></span>
7. <span data-ttu-id="6ae83-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6ae83-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6ae83-116">คุณสามารถเลือกลำดับชั้นการเพิ่มเติมสินค้าหรือช่องทางสำหรับชนิดนี้ </span><span class="sxs-lookup"><span data-stu-id="6ae83-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="6ae83-117">ค่าจะควบคุมว่าการเลือกด้วยชื่อจะเป็นลำดับชั้นของช่องทางหรือช่องทางเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="6ae83-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="6ae83-118">สำหรับตัวอย่างนี้ ปล่อยให้ตั้งค่าเป็นลำดับชั้นการเพิ่มเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="6ae83-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="6ae83-119">ในฟิลด์ชื่อ ให้เลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6ae83-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="6ae83-120">ค่าน้ำหนักเริ่มต้นได้มาจากน้ำหนักที่กำหนดไว้ในคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="6ae83-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="6ae83-121">น้ำหนักนี้สามารถใช้สำหรับกฎการเพิ่มเติมสินค้าหรือคุณสามารถป้อนน้ำหนักใหม่ในฟิลด์น้ำหนัก </span><span class="sxs-lookup"><span data-stu-id="6ae83-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="6ae83-122">ในฟิลด์น้ำหนัก ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="6ae83-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="6ae83-123">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6ae83-123">Click Add.</span></span>
11. <span data-ttu-id="6ae83-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6ae83-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="6ae83-125">ในฟิลด์ชนิด เลือก 'ช่องทาง' </span><span class="sxs-lookup"><span data-stu-id="6ae83-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="6ae83-126">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6ae83-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="6ae83-127">ในฟิลด์น้ำหนัก ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="6ae83-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="6ae83-128">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6ae83-128">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]