--- 
title: "รักษาประเภทของบาร์โค้ด"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า "
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="maintain-barcode-types"></a><span data-ttu-id="c3716-103">รักษาประเภทของบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="c3716-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3716-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="c3716-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="c3716-105">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="c3716-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="c3716-106">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ตัวอย่างมูลค่าที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="c3716-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="c3716-107">งานเหล่านี้อาจจะเกิดขึ้นทั่วไปโดยผู้จัดการคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="c3716-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="c3716-108">ไปที่ บาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="c3716-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="c3716-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c3716-109">Click New.</span></span>
3. <span data-ttu-id="c3716-110">ในฟิลด์การตั้งค่าบาร์โค้ด ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c3716-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="c3716-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c3716-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c3716-112">ในฟิลด์ชนิดของบาร์โค้ด ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c3716-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="c3716-113">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'รหัส 39' ได้</span><span class="sxs-lookup"><span data-stu-id="c3716-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="c3716-114">ในฟิลด์ขนาด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c3716-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="c3716-115">ในฟิลด์ความยาวสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c3716-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="c3716-116">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="c3716-116">Click Save.</span></span>
9. <span data-ttu-id="c3716-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c3716-117">Close the page.</span></span>
10. <span data-ttu-id="c3716-118">ไปที่ สินค้าคงคลังและพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="c3716-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="c3716-119">ในฟิลด์การตั้งค่าบาร์โค้ด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c3716-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="c3716-120">เลือกการตั้งค่าบาร์โค้ดที่คุณสร้างขึ้นก่อนหน้า แต่ให้ระวังว่าบาร์โค้ดต้องตรงกับรูปแบบของตัวระบุเฉพาะสำหรับชนิดของเรกคอร์ดที่ใช้ในกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="c3716-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="c3716-121">ตัวอย่างเช่น สำหรับเส้นทางการเบิกสินค้า รูปแบบบาร์โค้ดควรตรงกับรูปแบบของการอ้างอิงเส้นทางการเบิกสินค้า ซึ่งโดยปกติจะเป็นลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="c3716-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="c3716-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="c3716-122">Click Save.</span></span>
13. <span data-ttu-id="c3716-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c3716-123">Close the page.</span></span>


