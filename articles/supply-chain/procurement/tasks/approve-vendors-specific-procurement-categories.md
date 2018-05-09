--- 
title: "อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ"
description: "เมื่อมีการสร้างใบสั่งซื้อ อาจจำเป็นต้องเลือกผู้จัดจำหน่ายที่ได้รับอนุมัติหรือที่ต้องการ โดยขึ้นอยู่กับวิธีตั้งค่านโยบายการจัดซื้อ "
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 26aa675e51957596cce9a1147df1fa300fcfe351
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="8482b-103">อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8482b-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8482b-104">เมื่อมีการสร้างใบสั่งซื้อ อาจจำเป็นต้องเลือกผู้จัดจำหน่ายที่ได้รับอนุมัติหรือที่ต้องการ โดยขึ้นอยู่กับวิธีตั้งค่านโยบายการจัดซื้อ </span><span class="sxs-lookup"><span data-stu-id="8482b-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="8482b-105">กระบวนงานนี้แสดงวิธีการระบุว่าผู้จัดจำหน่ายได้รับอนุมัติหรือเป็นที่ต้องการสำหรับประเภทการจัดซื้อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8482b-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="8482b-106">งานนี้อาจมักจะถูกดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา</span><span class="sxs-lookup"><span data-stu-id="8482b-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="8482b-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="8482b-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="8482b-108">ไปที่การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8482b-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="8482b-109">เลือกผู้จัดจำหน่ายที่คุณต้องการเพื่อกำหนดเป็นผู้จัดจำหน่ายที่ต้องการหรือได้รับอนุมัติสำหรับประเภท</span><span class="sxs-lookup"><span data-stu-id="8482b-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="8482b-110">ในบานหน้าต่างการดำเนินการ ให้คลิก ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8482b-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="8482b-111">คลิกประเภท</span><span class="sxs-lookup"><span data-stu-id="8482b-111">Click Categories.</span></span>
5. <span data-ttu-id="8482b-112">คลิกเพิ่มประเภท</span><span class="sxs-lookup"><span data-stu-id="8482b-112">Click Add category.</span></span>
6. <span data-ttu-id="8482b-113">ในฟิลด์ประเภท เลือก สำนักงานและโต๊ะเบ็ดเตล็ด (OFFICE AND DESK ACCESSORIES)</span><span class="sxs-lookup"><span data-stu-id="8482b-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="8482b-114">ในฟิลด์สถานะประเภทผู้จัดจำหน่าย เลือก 'ที่ต้องการ'</span><span class="sxs-lookup"><span data-stu-id="8482b-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="8482b-115">สามารถระบุผู้จัดจำหน่ายที่ต้องการได้มากกว่าหนี่งรายการสำหรับแต่ละประเภท</span><span class="sxs-lookup"><span data-stu-id="8482b-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="8482b-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="8482b-116">Click Save.</span></span>
9. <span data-ttu-id="8482b-117">ไปที่การจัดซื้อและการจัดหา > ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="8482b-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="8482b-118">ในแผนภูมิ เลือก 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'</span><span class="sxs-lookup"><span data-stu-id="8482b-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="8482b-119">ขยายส่วนผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8482b-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="8482b-120">ตรวจสอบว่าผู้จัดจำหน่ายที่คุณเลือกปรากฏเป็นผู้จัดจำหน่ายที่ต้องการสำหรับประเภทสำนักงานและโต๊ะเบ็ดเตล็ดหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="8482b-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="8482b-121">ถ้าคุณกำลังรันกระบวนงานนี้เป็นคู่มืองาน คุณอาจต้องคลิกปุ่มปลดล็อกเพื่อให้สามารถเลื่อนลงไปยังรายการของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8482b-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="8482b-122">นอกจากนี้ยังสามารถเพิ่มผู้จัดจำหน่ายที่ต้องการและผู้จัดจำหน่ายที่ได้รับอนุมัติในหน้านี้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="8482b-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="8482b-123">ในแผนภูมิ ขยาย 'OFFICE AND DESK ACCESSORIES'</span><span class="sxs-lookup"><span data-stu-id="8482b-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="8482b-124">ในแผนภูมิ เลือก 'กรรไกร'</span><span class="sxs-lookup"><span data-stu-id="8482b-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="8482b-125">เลือกไม่ในฟิลด์ผู้จัดจำหน่ายที่สืบทอดจากประเภทหลัก</span><span class="sxs-lookup"><span data-stu-id="8482b-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="8482b-126">เลือกใช่ในฟิลด์ผู้จัดจำหน่ายที่สืบทอดจากประเภทหลัก</span><span class="sxs-lookup"><span data-stu-id="8482b-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


