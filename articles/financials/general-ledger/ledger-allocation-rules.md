---
title: "กฎการปันส่วนบัญชีแยกประเภท"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับกฎการปันส่วนบัญชีแยกประเภท โดยจะอธิบายส่วนประกอบต่างๆ ของกฎการปันส่วนและวิธีการปันส่วนที่สามารถใช้สำหรับอุปกรณ์เหล่านี้"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e5eb9d79fee7ec2e288db24aee9535d6414fdeed
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="da2f6-104">กฎการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="da2f6-104">Ledger allocation rules</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="da2f6-105">บทความนี้แสดงข้อมูลเกี่ยวกับกฎการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="da2f6-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="da2f6-106">โดยจะอธิบายส่วนประกอบต่างๆ ของกฎการปันส่วนและวิธีการปันส่วนที่สามารถใช้สำหรับอุปกรณ์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="da2f6-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="da2f6-107">กฎการปันส่วนบัญชีแยกประเภทจะใช้เพื่อคำนวณ และสร้างสมุดรายวันและรายการบัญชีการปันส่วนสำหรับการปันส่วนยอดดุลบัญชีแยกประเภทหรือยอดเงินคงที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="da2f6-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="da2f6-108">วิธีการปันส่วนสามารถผันแปรหรือคงที่</span><span class="sxs-lookup"><span data-stu-id="da2f6-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="da2f6-109">วิธีการปันส่วนต่อไปนี้สามารถใช้สำหรับกฎการปันส่วนบัญชีแยกประเภท:</span><span class="sxs-lookup"><span data-stu-id="da2f6-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="da2f6-110">**ข้อมูลพื้นฐาน**– วิธีการผันแปรนี้จะใช้เมื่อการปันส่วนขึ้นอยู่กับยอดดุลบัญชีแยกประเภทจริง ตามเกณฑ์ตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="da2f6-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="da2f6-111">ตัวอย่างเช่น ค่าใช้จ่ายการโฆษณาสามารถถูกปันส่วนตามยอดขายของแต่ละแผนกในสัดส่วนที่สัมพันธ์กับยอดขายรวมของแผนกได้</span><span class="sxs-lookup"><span data-stu-id="da2f6-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="da2f6-112">**เปอร์เซ็นต์คงที่** และ **น้ำหนักคงที่** – สำหรับวิธีเหล่านี้ เปอร์เซ็นต์หรือน้ำหนักการปันส่วนจะถูกกำหนดสำหรับกฎโดยตรง</span><span class="sxs-lookup"><span data-stu-id="da2f6-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="da2f6-113">ตัวอย่างเช่น ค่าใช้จ่ายการโฆษณาสามารถปันส่วนเพื่อให้แผนก A มี 70 เปอร์เซ็นต์ของค่าใช้จ่ายการโฆษณา และแผนก B มี 30 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="da2f6-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="da2f6-114">**เท่ากัน**– วิธีการนี้กระจายจำนวนเงินเท่า ๆ กันให้แต่ละปลายทางที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="da2f6-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="da2f6-115">ตัวอย่างเช่น ถ้ากำหนดปลายทางสำหรับแผนก A และแผนก B ค่าใช้จ่ายการโฆษณาสามารถปันส่วนเพื่อให้ทั้งแผนก A และแผนก B มี 50 เปอร์เซ็นต์ของค่าใช้จ่ายการโฆษณา</span><span class="sxs-lookup"><span data-stu-id="da2f6-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="da2f6-116">หากใช้ข้อมูลพื้นฐานเป็นวิธีการปันส่วนสำหรับกฎการปันส่วน คุณต้องกำหนดกฎพื้นฐานสำหรับการปันส่วนบัญชีแยกประเภทแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="da2f6-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="da2f6-117">กระบวนการ "คำขอกระบวนการปันส่วน" ช่วยให้ผู้ใช้ประมวลผลกฎการปันส่วนบัญชีแยกประเภท และแสดงตัวอย่างผลของรายการสมุดรายวันการปันส่วนก่อนที่จะลงรายการบัญชี หรือลบการปันส่วนที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="da2f6-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="da2f6-118">ส่วนประกอบของกฎการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="da2f6-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="da2f6-119">กฎการปันส่วนแต่ละกฎมีส่วนประกอบสี่ส่วน: ทั่วไป แหล่งที่มา ปลายทาง และออฟเซ็ต</span><span class="sxs-lookup"><span data-stu-id="da2f6-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="da2f6-120">ส่วนประกอบเพิ่มเติมที่ต้องมี คือ ข้อมูลพื้นฐานของกฎการปันส่วนบัญชีแยกประเภท ถ้าจะใช้ข้อมูลพื้นฐานเป็นวิธีการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="da2f6-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="da2f6-121">แต่ละส่วนประกอบเป็นส่วนสำคัญของรายละเอียดที่จำเป็นในการประมวลผลการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="da2f6-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="da2f6-122">**ทั่วไป**– คอมโพเนนต์นี้เป็นกรณีที่ผู้ใช้ระบุตัวเลือก เช่น วิธีการปันส่วน การตั้งค่ากฎระหว่างบริษัท และกฎเป็นกฎที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="da2f6-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="da2f6-123">**แหล่งที่มา**– คอมโพเนนต์นี้เป็นกรณีที่ผู้ใช้ระบุแหล่งข้อมูลสำหรับการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="da2f6-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="da2f6-124">การปันส่วนอาจขึ้นอยู่กับยอดดุลบัญชีแยกประเภท (**แหล่งข้อมูล** = **บัญชีแยกประเภท**) หรือยอดเงินคงที่ (**แหล่งข้อมูล** = **ค่าคงที่**)</span><span class="sxs-lookup"><span data-stu-id="da2f6-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="da2f6-125">เมื่อ **แหล่งข้อมูล** ถูกตั้งค่าเป็น **บัญชีแยกประเภท** ต้องกำหนดเงื่อนไขตัวกรองข้อมูลต้นทางสำหรับกฎการปันส่วนบัญชีแยกประเภท (ตัวอย่างเช่น สำหรับค่าใช้จ่ายการโฆษณา)</span><span class="sxs-lookup"><span data-stu-id="da2f6-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="da2f6-126">**ปลายทาง** - คอมโพเนนต์นี้จะกำหนดการกระจายและนำผลลัพธ์ที่ได้จากการคำนวณการปันส่วนมาพิจารณาที่ควรจะเป็น</span><span class="sxs-lookup"><span data-stu-id="da2f6-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="da2f6-127">ตัวอย่างเช่น อาจมีปลายทางหนึ่งรายการสำหรับแต่ละแผนก</span><span class="sxs-lookup"><span data-stu-id="da2f6-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="da2f6-128">**ออฟเซ็ต**– คอมโพเนนต์นี้กำหนดว่าบัญชีหลักและมิติควรถูกกำหนดสำหรับรายการออฟเซ็ตที่ยอดดุลรายการปลายทาง</span><span class="sxs-lookup"><span data-stu-id="da2f6-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="da2f6-129">ตัวเลือกที่ผู้ใช้กำหนดโดยทั่วไปจะใช้แทนบัญชีและมิติที่ยึดตามแหล่งที่มา</span><span class="sxs-lookup"><span data-stu-id="da2f6-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="da2f6-130">เมื่อ **แหล่งข้อมูล** ถูกตั้งค่าเป็น **ค่าคงที่**, **แหล่งที่มา** ไม่สามารถใช้เป็นตัวเลือกได้</span><span class="sxs-lookup"><span data-stu-id="da2f6-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="da2f6-131">**กฎพื้นฐานการปันส่วนบัญชีแยกประเภท**– กฎเหล่านี้ใช้เงื่อนไขตัวกรองข้อมูลต้นทางของตนเองเพื่อกำหนดยอดดุลบัญชีแยกประเภทที่ควรจะใช้สำหรับการปันส่วน (ตัวอย่างเช่น รายได้ต่อแผนก)</span><span class="sxs-lookup"><span data-stu-id="da2f6-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="da2f6-132">แต่ละกฎพื้นฐานการปันส่วนสามารถใช้กับกฎการปันส่วนต่าง ๆ หลายกฎ</span><span class="sxs-lookup"><span data-stu-id="da2f6-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





