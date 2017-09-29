--- 
title: "สร้างองค์ประกอบต้นทุน  "
description: "มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน "
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="create-cost-elements"></a><span data-ttu-id="fc19a-103">สร้างองค์ประกอบต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="fc19a-103">Create cost elements</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc19a-104">มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน </span><span class="sxs-lookup"><span data-stu-id="fc19a-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="fc19a-105">กระบวนงานนี้แสดงวิธีการสร้างองค์ประกอบต้นทุนโดยการนำเข้าบัญชีหลักผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fc19a-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="fc19a-106">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="fc19a-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="fc19a-107">ขั้นตอนนี้ใช้สำหรับคุณลักษณะการบัญชีต้นทุนที่ถูกเพิ่มเข้ามาใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="fc19a-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="fc19a-108">สร้างองค์ประกอบต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="fc19a-108">Create new cost elements</span></span>
1. <span data-ttu-id="fc19a-109">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fc19a-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="fc19a-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc19a-110">Click New.</span></span>
3. <span data-ttu-id="fc19a-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="fc19a-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fc19a-112">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc19a-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="fc19a-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="fc19a-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="fc19a-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc19a-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="fc19a-115">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fc19a-115">Configure the data connector</span></span>
1. <span data-ttu-id="fc19a-116">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="fc19a-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="fc19a-117">ในฟิลด์ผังบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc19a-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="fc19a-118">เลือก ใช้ร่วมกัน เพื่อใช้ผังบัญชีร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="fc19a-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="fc19a-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc19a-119">Click New.</span></span>
4. <span data-ttu-id="fc19a-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fc19a-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fc19a-121">คุณสามารถใช้ตัวกรองบัญชีเพื่อให้ตรงกับเกณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fc19a-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="fc19a-122">ในฟิลด์จากบัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc19a-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="fc19a-123">ในฟิลด์ถึงบัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="fc19a-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="fc19a-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fc19a-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="fc19a-125">นำเข้าบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="fc19a-125">Import main accounts</span></span>
1. <span data-ttu-id="fc19a-126">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="fc19a-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="fc19a-127">บัญชีหลักจะถูกนำเข้าไปยังการลงบัญชีต้นทุนสินค้า และใช้เป็นองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fc19a-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="fc19a-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="fc19a-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="fc19a-129">ดูบัญชีที่นำเข้าเป็นองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="fc19a-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="fc19a-130">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="fc19a-130">Click View dimension members.</span></span>
    * <span data-ttu-id="fc19a-131">ดูบัญชีแยกประเภทที่นำเข้าเป็นองค์ประกอบต้นทุนในธุรกิจของคุณที่ต้นทุนสามารถไปได้</span><span class="sxs-lookup"><span data-stu-id="fc19a-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


