---
title: "ค่าเสื่อมราคาพิเศษ"
description: "บทความนี้แสดงภาพรวมของฟังก์ชันการคิดค่าเสื่อมราคาพิเศษ"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 89814bf54f09b91d7c23904c2f1ac31d5b284824
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="bonus-depreciation"></a><span data-ttu-id="b190b-103">ค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="b190b-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b190b-104">บทความนี้แสดงภาพรวมของฟังก์ชันการคิดค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="b190b-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="b190b-105">สำหรับค่าเสื่อมราคาพิเศษคุณสามารถคำนวณจำนวนเงินค่าเสื่อมราคาพิเศษหรือเพิ่มเติมในระหว่างปีแรกที่เริ่มใช้งานและคิดค่าเสื่อมราคาสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b190b-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="b190b-106">จะต้องหักค่าเสื่อมราคาพิเศษก่อนที่จะคำนวณค่าเสื่อมราคาอื่น</span><span class="sxs-lookup"><span data-stu-id="b190b-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="b190b-107">ดังนั้น วิธีที่ดีที่สุดคือการใช้ค่าเสื่อมราคาพิเศษกับสมุดบัญชีที่ปิดใช้งานฟังก์ชัน ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="b190b-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="b190b-108">คุณสามารถใช้ตัวเลือก **ลบธุรกรรมต้นทุนที่ไม่ได้ลงรายการบัญชีไปที่บัญชีแยกประเภททั่วไป** เพื่อลบธุรกรรมในอดีตสำหรับสมุดบัญชีที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="b190b-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="b190b-109">จากนั้นคุณสามารถรองรับค่าเสื่อมราคาพิเศษในภายหลังในวงจรอายุของสินทรัพย์ได้โดยการลบธุรกรรมค่าเสื่อมราคาที่ลงรายการบัญชีไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="b190b-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="b190b-110">คุณสามารถคำนวณค่าเสื่อมราคาพิเศษได้โดยการใช้กระบวนการข้อเสนอหรือ คุณสามารถสร้างธุรกรรมค่าเสื่อมราคาพิเศษด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="b190b-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="b190b-111">คุณไม่สามารถสร้างธุรกรรมค่าเสื่อมราคาพิเศษได้ถ้ามีธุรกรรมค่าเสื่อมราคาหรือธุรกรรมการปรับปรุงค่าเสื่อมราคาอยู่สำหรับสมุดบัญชีสินทรัพย์นั้น</span><span class="sxs-lookup"><span data-stu-id="b190b-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="b190b-112">เมื่อคุณใช้กระบวนการข้อเสนอเพื่อคำนวณค่าเสื่อมราคาพิเศษ ธุรกรรมพิเศษที่มีอยู่ทั้งหมดจะรวมอยู่ในการคำนวณข้อมูลพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b190b-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="b190b-113">การคำนวณยังรวมค่าเสื่อมราคาพิเศษใดๆ ก่อนหน้าที่คุณป้อนด้วยตนเองสำหรับสินทรัพย์ด้วย</span><span class="sxs-lookup"><span data-stu-id="b190b-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="b190b-114">ถ้าค่าเสื่อมราคาพิเศษมากกว่าหนึ่งจะใช้สำหรับสินทรัพย์ จะมีการพิจารณาถึงระดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="b190b-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="b190b-115">โบนัสแต่ละตัวลดเกณฑ์พื้นฐานของสินทรัพย์สำหรับโบนัสถัดไป</span><span class="sxs-lookup"><span data-stu-id="b190b-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="b190b-116">จะไม่มีการพิจารณามูลค่าซากในเกณฑ์พื้นฐานของสินทรัพย์สำหรับการคำนวณค่าเสื่อมราคาพิเศษ และไม่สามารถใช้แบบแผนการคิดค่าเสื่อมราคาสำหรับค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="b190b-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="b190b-117">ปัจจุบันในสหรัฐอเมริกา ทรัพย์สินบางอย่างมีคุณสมบัติเข้าเกณฑ์ทรัพย์สินตามมาตรา 179</span><span class="sxs-lookup"><span data-stu-id="b190b-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="b190b-118">โดยการใช้การหักลดตามมาตรา 179 คุณสามารถกู้คืนทั้งหมดหรือบางส่วนของต้นทุนของทรัพย์สินบางอย่าง จนถึงขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="b190b-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="b190b-119">คุณสามารถกู้คืนต้นทุนโดยการหักลดในปีที่คุณเริ่มใช้งานทรัพย์สินนั้น</span><span class="sxs-lookup"><span data-stu-id="b190b-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="b190b-120">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="b190b-120">Example</span></span>
<span data-ttu-id="b190b-121">ค่าเสื่อมราคาพิเศษต่อไปนี้สัมพันธ์กับสมุดบัญชีสินทรัพย์หนึ่ง ดังนี้</span><span class="sxs-lookup"><span data-stu-id="b190b-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="b190b-122">**มาตรา 179:** 1,000.00, ระดับความสำคัญ 1</span><span class="sxs-lookup"><span data-stu-id="b190b-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="b190b-123">**โซนปลอดภาษี:** 30 เปอร์เซ็นต์ ระดับความสำคัญ 2</span><span class="sxs-lookup"><span data-stu-id="b190b-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="b190b-124">ต้นทุนการซื้อสินทรัพย์คือ 5,000.00</span><span class="sxs-lookup"><span data-stu-id="b190b-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="b190b-125">จำนวนเงินค่าเสื่อมราคาพิเศษแรกจะเท่ากับ $1,000.00 สำหรับค่าเสื่อมราคาตามมาตรา 179</span><span class="sxs-lookup"><span data-stu-id="b190b-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="b190b-126">จำนวนเงินค่าเสื่อมราคาพิเศษต่อมา สำหรับค่าเสื่อมราคาของโซนปลอดภาษีจะคำนวณดังนี้:</span><span class="sxs-lookup"><span data-stu-id="b190b-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="b190b-127">ต้นทุนการซื้อสินทรัพย์ – 1,000 (ค่าเสื่อมราคาตามมาตรา 179) × 30 เปอร์เซ็นต์ = 1,200</span><span class="sxs-lookup"><span data-stu-id="b190b-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="b190b-128">ถ้าจำนวนเงินค่าเสื่อมราคาพิเศษสูงกว่าต้นทุนการซื้อที่เหลือ จำนวนเงินค่าเสื่อมราคาพิเศษจะเป็นผลลัพธ์ของการคำนวณค่าเสื่อมราคาพิเศษหรือต้นทุนการซื้อที่เหลือ แล้วแต่ว่าจำนวนเงินใดจะน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="b190b-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="b190b-129">ถ้าต้นทุนการซื้อที่เหลือเท่ากับ 0 (ศูนย์) หรือน้อยกว่า ธุรกรรมค่าเสื่อมราคาพิเศษจะไม่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b190b-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="b190b-130">เมื่อคำนวณค่าเสื่อมราคาพิเศษโดยใช้กระบวนการข้อเสนอ ธุรกรรมค่าเสื่อมราคาพิเศษจะถูกสร้างขึ้นสำหรับเรกคอร์ดค่าเสื่อมราคาพิเศษที่เกี่ยวข้องทั้งหมดที่สัมพันธ์กับสมุดบัญชีสินทรัพย์นั้น</span><span class="sxs-lookup"><span data-stu-id="b190b-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="b190b-131">คุณสามารถสร้างเรกคอร์ดค่าเสื่อมราคาพิเศษได้ไม่จำกัดจำนวน</span><span class="sxs-lookup"><span data-stu-id="b190b-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="b190b-132">หลังจากที่คุณกำหนดเรกคอร์ดเหล่านั้นให้กับสมุดบัญชีกลุ่มสินทรัพย์ จะถูกนำไปใช้กับสมุดบัญชีสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b190b-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="b190b-133">ค่าเสื่อมราคาพิเศษจะถูกป้อนเป็นเปอร์เซ็นต์หรือเป็นจำนวนเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="b190b-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="b190b-134">เมื่อคุณลงรายการบัญชีข้อเสนอค่าเสื่อมราคา จะมีการลงรายการบัญชีธุรกรรมค่าเสื่อมราคาพิเศษที่สมุดบัญชีโดยเป็นธุรกรรมที่แยกต่างหากจากธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b190b-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




