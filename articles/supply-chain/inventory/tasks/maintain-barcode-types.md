---
title: รักษาประเภทของบาร์โค้ด
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า '
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 979726a1d094146b546bbc6d31963367de2c59f5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204090"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="f8c67-103">รักษาประเภทของบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="f8c67-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8c67-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อกำหนดบาร์โค้ดใหม่ ซึ่งสามารถนำไปใช้เป็นส่วนหนึ่งของรายงานรายการเบิกสินค้า </span><span class="sxs-lookup"><span data-stu-id="f8c67-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="f8c67-105">คุณสามารถศึกษากระบวนงานนี้ได้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="f8c67-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f8c67-106">ถ้าคุณกำลังใช้ USMF คุณสามารถใช้ตัวอย่างมูลค่าที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="f8c67-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="f8c67-107">งานเหล่านี้อาจจะเกิดขึ้นทั่วไปโดยผู้จัดการคลังสินค้า </span><span class="sxs-lookup"><span data-stu-id="f8c67-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="f8c67-108">ไปที่ บาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="f8c67-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="f8c67-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f8c67-109">Click New.</span></span>
3. <span data-ttu-id="f8c67-110">ในฟิลด์การตั้งค่าบาร์โค้ด ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8c67-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="f8c67-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f8c67-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8c67-112">ในฟิลด์ชนิดของบาร์โค้ด ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f8c67-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="f8c67-113">ถ้าคุณกำลังใช้ USMF คุณสามารถเลือก 'รหัส 39' ได้</span><span class="sxs-lookup"><span data-stu-id="f8c67-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="f8c67-114">ในฟิลด์ขนาด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f8c67-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="f8c67-115">ในฟิลด์ความยาวสูงสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f8c67-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="f8c67-116">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="f8c67-116">Click Save.</span></span>
9. <span data-ttu-id="f8c67-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f8c67-117">Close the page.</span></span>
10. <span data-ttu-id="f8c67-118">ไปที่ สินค้าคงคลังและพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="f8c67-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="f8c67-119">ในฟิลด์การตั้งค่าบาร์โค้ด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8c67-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="f8c67-120">เลือกการตั้งค่าบาร์โค้ดที่คุณสร้างขึ้นก่อนหน้า แต่ให้ระวังว่าบาร์โค้ดต้องตรงกับรูปแบบของตัวระบุเฉพาะสำหรับชนิดของเรกคอร์ดที่ใช้ในกระบวนการ </span><span class="sxs-lookup"><span data-stu-id="f8c67-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="f8c67-121">ตัวอย่างเช่น สำหรับเส้นทางการเบิกสินค้า รูปแบบบาร์โค้ดควรตรงกับรูปแบบของการอ้างอิงเส้นทางการเบิกสินค้า ซึ่งโดยปกติจะเป็นลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="f8c67-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="f8c67-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f8c67-122">Click Save.</span></span>
13. <span data-ttu-id="f8c67-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f8c67-123">Close the page.</span></span>

