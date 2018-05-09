--- 
title: "ข้ามเทียบผลิตภัณฑ์จากคลังสินค้าที่รับเข้าไปยังร้านค้า"
description: "ขั้นตอนนี้จะแนะนำขั้นตอนสร้างและประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเพื่อกระจายผลิตภัณฑ์จากสถานที่ที่รับสินค้าในใบสั่งซื้อไปยังร้านค้าหนึ่งร้านหรือมากกว่านั้น "
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1182474504f7d1c051fe995c516367420ccc9701
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="11fc1-103">ข้ามเทียบผลิตภัณฑ์จากคลังสินค้าที่รับเข้าไปยังร้านค้า</span><span class="sxs-lookup"><span data-stu-id="11fc1-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11fc1-104">ขั้นตอนนี้จะแนะนำขั้นตอนสร้างและประมวลผลการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเพื่อกระจายผลิตภัณฑ์จากสถานที่ที่รับสินค้าในใบสั่งซื้อไปยังร้านค้าหนึ่งร้านหรือมากกว่านั้น </span><span class="sxs-lookup"><span data-stu-id="11fc1-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="11fc1-105">ผู้ใช้สามารถกำหนดโครงแบบหลายชนิดและให้ระบบแนะนำวิธีการกระจายผลิตภัณฑ์ หรือป้อนสถานที่ที่จะกระจายผลิตภัณฑ์และจำนวนที่จะกระจายให้กับร้านค้าแต่ละร้านด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="11fc1-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="11fc1-106">กระบวนงานนี้ไม่ได้รวมการตั้งค่าข้อมูลที่สามารถใช้ในการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า เช่นกฎการเพิ่มเติมสินค้า ลำดับชั้นขององค์กร และน้ำหนักของร้านค้า </span><span class="sxs-lookup"><span data-stu-id="11fc1-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="11fc1-107">ขั้นตอนนี้จะใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="11fc1-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="11fc1-108">ไปที่ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="11fc1-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="11fc1-109">เลือกใบสั่งซื้อในรายการ และคลิกลิงค์เพื่อเปิดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="11fc1-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="11fc1-110">ในบานหน้าต่างการดำเนินการ คลิกการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="11fc1-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="11fc1-111">คลิกการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า</span><span class="sxs-lookup"><span data-stu-id="11fc1-111">Click Cross docking.</span></span>
5. <span data-ttu-id="11fc1-112">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="11fc1-112">Click Edit.</span></span>
    * <span data-ttu-id="11fc1-113">หมวดหมู่สามารถใช้เพื่อกรองสินค้าในส่วนรายการ</span><span class="sxs-lookup"><span data-stu-id="11fc1-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="11fc1-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="11fc1-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11fc1-115">ในฟิลด์ปริมาณการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า พิมพ์ค่าเพื่อระบุปริมาณผลิตภัณฑ์ที่ถูกเลือกที่มี่การสั่งซื้อว่าควรถูกกระจายมากแค่ไหน</span><span class="sxs-lookup"><span data-stu-id="11fc1-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="11fc1-116">ในฟิลด์การส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้าเพิ่มเติมข้ามฟิลด์ ป้อนค่าเพื่อระบุปริมาณที่จะกระจายสินค้าสำหรับผลิตภัณฑ์ที่มีอยู่ที่มีการสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="11fc1-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="11fc1-117">ในฟิลด์การกระจาย ป้อน 'น้ำหนักของสถานที่เก็บ'</span><span class="sxs-lookup"><span data-stu-id="11fc1-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="11fc1-118">คุณสามารถเลือกประเภทอื่นๆ เพื่อใช้กฎที่แตกต่างกันสำหรับการกระจาย</span><span class="sxs-lookup"><span data-stu-id="11fc1-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="11fc1-119">ในฟิลด์ลำดับชั้นการเพิ่มเติมสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="11fc1-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="11fc1-120">เลือก ใช่ ในฟิลด์คำนึงถึงการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="11fc1-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="11fc1-121">คลิกคำนวณปริมาณ</span><span class="sxs-lookup"><span data-stu-id="11fc1-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="11fc1-122">คลิกสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="11fc1-122">Click Create order.</span></span>
14. <span data-ttu-id="11fc1-123">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="11fc1-123">Click Yes.</span></span>
15. <span data-ttu-id="11fc1-124">ในรายการ ค้นหาและเลือกคลังสินค้าที่ได้รับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="11fc1-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="11fc1-125">คลิกใบสั่งเพื่อดูใบสั่งที่ถูกสร้างขึ้นสำหรับคลังสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="11fc1-125">Click Order to view the orders that got created for the selected warehouse</span></span>


