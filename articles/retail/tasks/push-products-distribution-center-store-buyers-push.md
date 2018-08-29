--- 
title: "กำหนดผลิตภัณฑ์จากศูนย์กระจายไปยังร้านค้าโดยใช้การจัดส่งสินค้าแบบผลัก"
description: "กระบวนงานนี้จะแนะนำขั้นตอนการสร้างและประมวลผลการจัดส่งสินค้าแบบผลัก เพื่อกระจายผลิตภัณฑ์จากสถานที่หนึ่งไปยังร้านค้าหนึ่งร้านหรือมากกว่านั้น"
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ed47b4f052dab99dec058910e4b8558481b34e59
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="push-products-from-distribution-centers-to-stores-via-buyers-push"></a><span data-ttu-id="7d6ed-103">กำหนดผลิตภัณฑ์จากศูนย์กระจายไปยังร้านค้าโดยใช้การจัดส่งสินค้าแบบผลัก</span><span class="sxs-lookup"><span data-stu-id="7d6ed-103">Push products from distribution centers to stores via buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7d6ed-104">กระบวนงานนี้จะแนะนำขั้นตอนการสร้างและประมวลผลการจัดส่งสินค้าแบบผลัก เพื่อกระจายผลิตภัณฑ์จากสถานที่หนึ่งไปยังร้านค้าหนึ่งร้านหรือมากกว่านั้น</span><span class="sxs-lookup"><span data-stu-id="7d6ed-104">This procedure walks through the steps to create and process a Buyer's push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="7d6ed-105">ผู้ใช้สามารถกำหนดโครงแบบหลายชนิดและให้ระบบแนะนำวิธีการกระจายผลิตภัณฑ์ หรือป้อนสถานที่ที่จะกระจายผลิตภัณฑ์และจำนวนที่จะกระจายให้กับร้านค้าแต่ละร้านด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="7d6ed-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="7d6ed-106">กระบวนงานนี้ไม่ได้รวมการตั้งค่าข้อมูลที่สามารถใช้ในการจัดส่งสินค้าแบบผลักได้ เช่น กฎการเติมสินค้า ลำดับชั้นขององค์กร และน้ำหนักของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="7d6ed-106">This procedure doesn't include setup of data that can be used in the Buyer's push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="7d6ed-107">ขั้นตอนนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="7d6ed-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="7d6ed-108">ไปที่การจัดส่งสินค้าแบบผลัก</span><span class="sxs-lookup"><span data-stu-id="7d6ed-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="7d6ed-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7d6ed-109">Click New.</span></span>
3. <span data-ttu-id="7d6ed-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7d6ed-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="7d6ed-111">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7d6ed-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="7d6ed-112">ในฟิลด์คลังสินค้า ป้อนหรือเลือกคลังสินค้าที่มีผลิตภัณฑ์ที่มีปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="7d6ed-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="7d6ed-113">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7d6ed-113">Click Add.</span></span>
7. <span data-ttu-id="7d6ed-114">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d6ed-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7d6ed-115">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7d6ed-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="7d6ed-116">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7d6ed-116">Click Add.</span></span>
10. <span data-ttu-id="7d6ed-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d6ed-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="7d6ed-118">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="7d6ed-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="7d6ed-119">เมื่อป้อนผลิตภัณฑ์ย่อย บรรทัดจะถูกสร้างขึ้นสำหรับตัวแปรแต่ละตัว</span><span class="sxs-lookup"><span data-stu-id="7d6ed-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="7d6ed-120">ในรายการนี้ ทำเครื่องหมายที่แถว</span><span class="sxs-lookup"><span data-stu-id="7d6ed-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="7d6ed-121">ในฟิลด์ปริมาณแบบผลัก พิมพ์จำนวนของผลิตภัณฑ์ที่เลือกว่าคุณต้องการกระจายมากแค่ไหน</span><span class="sxs-lookup"><span data-stu-id="7d6ed-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="7d6ed-122">ในฟิลด์ปริมาณเพิ่มเติมที่จะผลัก ป้อนปริมาณของผลิตภัณฑ์ที่มีปริมาณพร้อมใช้งานเพื่อกระจาย</span><span class="sxs-lookup"><span data-stu-id="7d6ed-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="7d6ed-123">ในฟิลด์การกระจาย ป้อน 'น้ำหนักของสถานที่เก็บ'</span><span class="sxs-lookup"><span data-stu-id="7d6ed-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="7d6ed-124">คุณสามารถเลือกประเภทอื่นๆ เพื่อใช้กฎอื่นๆ สำหรับการกระจาย</span><span class="sxs-lookup"><span data-stu-id="7d6ed-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="7d6ed-125">ในฟิลด์ลำดับชั้นการเพิ่มเติมสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="7d6ed-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="7d6ed-126">เลือก ใช่ ในฟิลด์คำนึงถึงการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="7d6ed-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="7d6ed-127">คลิกคำนวณปริมาณและตรวจสอบปริมาณที่ถูกเพิ่มลงในแถวในส่วนคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="7d6ed-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="7d6ed-128">คลิกสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="7d6ed-128">Click Create order.</span></span>
20. <span data-ttu-id="7d6ed-129">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="7d6ed-129">Click Yes.</span></span>


