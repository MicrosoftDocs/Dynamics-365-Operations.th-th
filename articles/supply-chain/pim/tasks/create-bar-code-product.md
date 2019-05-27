---
title: สร้างบาร์โค้ดให้ผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 เป็นตัวอย่าง '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568615"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="bbe20-103">สร้างบาร์โค้ดให้ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bbe20-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbe20-104">กระบวนงานนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 เป็นตัวอย่าง </span><span class="sxs-lookup"><span data-stu-id="bbe20-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="bbe20-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="bbe20-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bbe20-106">คลิก การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="bbe20-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="bbe20-107">คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="bbe20-107">Click Released products.</span></span>
3. <span data-ttu-id="bbe20-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bbe20-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bbe20-109">ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="bbe20-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="bbe20-110">คลิก บาร์โคด</span><span class="sxs-lookup"><span data-stu-id="bbe20-110">Click Bar codes.</span></span>
6. <span data-ttu-id="bbe20-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bbe20-111">Click New.</span></span>
7. <span data-ttu-id="bbe20-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bbe20-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bbe20-113">ในฟิลด์การตั้งค่าบาร์โค้ด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bbe20-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="bbe20-114">ในฟิลด์รหัสบาร์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bbe20-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="bbe20-115">ในฟิลด์รหัสบาร์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bbe20-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="bbe20-116">กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="bbe20-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="bbe20-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bbe20-117">Close the page.</span></span>
12. <span data-ttu-id="bbe20-118">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="bbe20-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="bbe20-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bbe20-119">Click Save.</span></span>
    * <span data-ttu-id="bbe20-120">เมื่อคุณคลิก บันทึก ระบบจะดำเนินการตรวจสอบบาร์โค้ด ในกรณีนี้ จะแสดงข้อผิดพลาดที่ระบุว่าตัวเลขการตรวจสอบที่คาดไว้คือ 8 แต่พบเป็น 3 </span><span class="sxs-lookup"><span data-stu-id="bbe20-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="bbe20-121">ให้ปรับปรุงหมายเลขบาร์โค้ดด้วยตนเองเพื่อให้ 8 อยู่ในตำแหน่งท้ายสุด</span><span class="sxs-lookup"><span data-stu-id="bbe20-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="bbe20-122">ในฟิลด์รหัสบาร์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bbe20-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="bbe20-123">ในฟิลด์รหัสบาร์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bbe20-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="bbe20-124">กดคีย์ Tab</span><span class="sxs-lookup"><span data-stu-id="bbe20-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="bbe20-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bbe20-125">Close the page.</span></span>
17. <span data-ttu-id="bbe20-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="bbe20-126">Click Save.</span></span>
18. <span data-ttu-id="bbe20-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bbe20-127">Close the page.</span></span>

