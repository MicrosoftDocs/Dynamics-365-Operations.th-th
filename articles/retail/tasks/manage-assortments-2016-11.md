--- 
title: " จัดการการจัดประเภท "
description: "กระบวนงานนี้อธิบายวิธีการสร้างและเผยแพร่การจัดประเภทผลิตภัณฑ์ใหม่และการใช้ข้อมูลบริษัทสาธิต USRT "
author: jashanno
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1c353a135559a1901f98ae6e7c9671254ab625c3
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="manage-assortments"></a><span data-ttu-id="b82ee-103"> จัดการการจัดประเภท </span><span class="sxs-lookup"><span data-stu-id="b82ee-103">Manage assortments</span></span> 

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b82ee-104">กระบวนงานนี้อธิบายวิธีการสร้างและเผยแพร่การจัดประเภทผลิตภัณฑ์ใหม่และการใช้ข้อมูลบริษัทสาธิต USRT </span><span class="sxs-lookup"><span data-stu-id="b82ee-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="b82ee-105">กระบวนงานนี้จำเป็นต้องใช้แอพลิเคชัน Dynamics AX 7.0.1 หรือใหม่กว่า และแพลตฟอร์ม Dynamics AX 7.1</span><span class="sxs-lookup"><span data-stu-id="b82ee-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="b82ee-106">คลิกการจัดการประเภทและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b82ee-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="b82ee-107">สร้างการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="b82ee-107">Create an assortment</span></span>
1. <span data-ttu-id="b82ee-108">คลิกแท็บการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="b82ee-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="b82ee-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b82ee-109">Click New.</span></span>
3. <span data-ttu-id="b82ee-110">คลิก การจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="b82ee-110">Click Assortment.</span></span>
    * <span data-ttu-id="b82ee-111">จำเป็นต้องมีรหัสการจัดประเภทและจะต้องเป็นค่าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="b82ee-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="b82ee-112">ในฟิลด์ชื่อการจัดประเภท ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b82ee-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="b82ee-113">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="b82ee-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="b82ee-114">ในฟิลด์วันที่สิ้นสุด ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="b82ee-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="b82ee-115">ขยายส่วนช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="b82ee-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="b82ee-116">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b82ee-116">Click Add line.</span></span>
9. <span data-ttu-id="b82ee-117">ในแผนภูมิ ให้เลือก 'Contoso Retail\Electronics\Boston'</span><span class="sxs-lookup"><span data-stu-id="b82ee-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="b82ee-118">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b82ee-118">Click Add.</span></span>
11. <span data-ttu-id="b82ee-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b82ee-119">Click OK.</span></span>
12. <span data-ttu-id="b82ee-120">ขยายส่วนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b82ee-120">Expand the Products section.</span></span>
13. <span data-ttu-id="b82ee-121">คลิก เพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="b82ee-121">Click Add line.</span></span>
14. <span data-ttu-id="b82ee-122">ในฟิลด์ประเภท ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b82ee-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="b82ee-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b82ee-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="b82ee-124">เผยแพร่การจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="b82ee-124">Publish an assortment</span></span>
1. <span data-ttu-id="b82ee-125">คลิกที่เผยแพร่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b82ee-125">Click Publish.</span></span>
2. <span data-ttu-id="b82ee-126">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="b82ee-126">Click Yes.</span></span>


