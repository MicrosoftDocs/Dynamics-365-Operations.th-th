---
title: คัดลอกสินค้าร่วมจากเวอร์ชั่นสูตรที่มีอยู่
description: 'กระบวนงานนี้แสดงวิธีการคัดลอกผลิตภัณฑ์ร่วมจากเวอร์ชันสูตรที่มีอยู่ ไปที่เวอร์ชันสูตรที่แตกต่างกันสำหรับผลิตภัณฑ์ที่นำออกใช้ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438211"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="2d36d-103">คัดลอกสินค้าร่วมจากเวอร์ชั่นสูตรที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="2d36d-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d36d-104">กระบวนงานนี้แสดงวิธีการคัดลอกผลิตภัณฑ์ร่วมจากเวอร์ชันสูตรที่มีอยู่ ไปที่เวอร์ชันสูตรที่แตกต่างกันสำหรับผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="2d36d-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="2d36d-105">ซึ่งเป็นข้อกำหนดเบื้องต้นที่ต้องมีเวอร์ชันสูตรอย่างน้อยหนึ่งรายการที่เชื่อมโยงกับผลิตภัณฑ์ร่วม </span><span class="sxs-lookup"><span data-stu-id="2d36d-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="2d36d-106">เราจะใช้ข้อมูลสาธิตของบริษัท USP2 เพื่อสร้างขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="2d36d-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="2d36d-107">ค้นหาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="2d36d-107">Find a released product</span></span>
1. <span data-ttu-id="2d36d-108">ไปที่ผลิตภัณฑ์ที่จะนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="2d36d-108">Go to Released products.</span></span>
2. <span data-ttu-id="2d36d-109">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="2d36d-109">Click Show filters.</span></span>
    * <span data-ttu-id="2d36d-110">คุณกำลังจะเพิ่่มชนิดการผลิตฟิลด์ในกล่องข้อความตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="2d36d-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="2d36d-111">คลิกเพิ่มฟิลด์ตัวกรองเพื่อเพิ่มชนิดการผลิตฟิลด์</span><span class="sxs-lookup"><span data-stu-id="2d36d-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="2d36d-112">ในขั้นตอนต่อไป คุณต้องป้อนสูตรในฟิลด์ชนิดการผลิต ก่อนที่คุณจะเลือก นำไปใช้งาน </span><span class="sxs-lookup"><span data-stu-id="2d36d-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="2d36d-113">นี่จะตั้งค่าตัวกรองข้อมูลตามรายการของผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="2d36d-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="2d36d-114">ป้อนสูตรในฟิลด์ชนิดผลิตภัณฑ์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="2d36d-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="2d36d-115">คลิก ใช้</span><span class="sxs-lookup"><span data-stu-id="2d36d-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="2d36d-116">ค้นหาผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="2d36d-116">Select a released product</span></span>
1. <span data-ttu-id="2d36d-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2d36d-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="2d36d-118">คลิกเวอร์ชันสูตร</span><span class="sxs-lookup"><span data-stu-id="2d36d-118">Click Formula versions.</span></span>
    * <span data-ttu-id="2d36d-119">ในหน้าต่างการดำเนินการด้านวิศวกร คลิกเวอร์ชันของสูตร</span><span class="sxs-lookup"><span data-stu-id="2d36d-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="2d36d-120">คัดลอกผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="2d36d-120">Copy co-products</span></span>
1. <span data-ttu-id="2d36d-121">ในบานหน้าต่างการดำเนินการ คลิกเวอร์ชั่นสูตร</span><span class="sxs-lookup"><span data-stu-id="2d36d-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="2d36d-122">คลิกผลิตภัณฑ์ร่วม</span><span class="sxs-lookup"><span data-stu-id="2d36d-122">Click Co-products.</span></span>
3. <span data-ttu-id="2d36d-123">คลิก คัดลอก</span><span class="sxs-lookup"><span data-stu-id="2d36d-123">Click Copy.</span></span>
4. <span data-ttu-id="2d36d-124">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2d36d-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="2d36d-125">ในฟิลด์เวอร์ชันสูตร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2d36d-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="2d36d-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2d36d-126">Click OK.</span></span>
7. <span data-ttu-id="2d36d-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2d36d-127">Close the page.</span></span>

