---
title: "รายงานบัตรสินค้าคงคลัง"
description: "หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายงานบัตรสินค้าคงคลังสำหรับนิติบุคคลในประเทศไทย รายงานบัตรสินค้าคงคลังประกอบด้วยรายละเอียดเกี่ยวกับความเคลื่อนไหวของสินค้าคงคลัง ปริมาณ และต้นทุนสำหรับแต่ละสินค้าและคลังสินค้า และจะต้องถูกสร้างขึ้นเมื่อรัฐบาลร้องขอ รายงานบัตรสินค้าคงคลังจะถูกสร้างขึ้นก่อนหรือหลังกระบวนการปิดบัญชีสินค้าคงคลัง"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265184
ms.assetid: 1ce8c70b-c6af-4171-98d2-2aa8e9563c5b
ms.search.region: Thailand
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5aee3a39c83d6a35237efc6fe2ba487299cab361
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="stock-card-reports"></a><span data-ttu-id="ef474-105">รายงานบัตรสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ef474-105">Stock card reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef474-106">หัวข้อนี้ให้ข้อมูลเกี่ยวกับรายงานบัตรสินค้าคงคลังสำหรับนิติบุคคลในประเทศไทย</span><span class="sxs-lookup"><span data-stu-id="ef474-106">This topic provides information about stock card reports for legal entities in Thailand.</span></span> <span data-ttu-id="ef474-107">รายงานบัตรสินค้าคงคลังประกอบด้วยรายละเอียดเกี่ยวกับความเคลื่อนไหวของสินค้าคงคลัง ปริมาณ และต้นทุนสำหรับแต่ละสินค้าและคลังสินค้า และจะต้องถูกสร้างขึ้นเมื่อรัฐบาลร้องขอ</span><span class="sxs-lookup"><span data-stu-id="ef474-107">A stock card report contains information about inventory movement, quantity, and cost for each item and warehouse, and must be generated when the government requests it.</span></span> <span data-ttu-id="ef474-108">รายงานบัตรสินค้าคงคลังจะถูกสร้างขึ้นก่อนหรือหลังกระบวนการปิดบัญชีสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ef474-108">The stock card report is generated either before or after the inventory close process.</span></span> 

<span data-ttu-id="ef474-109">คุณสามารถสร้างรายงานบัตรสินค้าคงคลังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ef474-109">You can generate the following stock card reports:</span></span>

-   <span data-ttu-id="ef474-110">**บัตรสินค้าคงคลังตามจริง** – ดูข้อมูลที่เกี่ยวข้องกับไซต์เดียวหรือไซต์ทั้งหมดต่อสถานที่เก็บและคลังสินค้า หลังจากมีการลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="ef474-110">**Physical stock card** – View information that is related to one site or all sites, per location and warehouse, after packing slips are posted.</span></span>
-   <span data-ttu-id="ef474-111">**บัตรสินค้าคงคลังทางการเงิน** – ดูข้อมูลที่เกี่ยวข้องกับไซต์เดียวหรือไซต์ทั้งหมดต่อสถานที่เก็บและคลังสินค้า หลังจากมีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ef474-111">**Financial stock card** – View information that is related to one site or all sites, per location and warehouse, after invoices are posted.</span></span>
-   <span data-ttu-id="ef474-112">**สรุปบัตรสินค้าคงคลัง** – ดูรายละเอียดสินค้าหรือคลังสินค้าตามกลุ่มสินค้า ไซต์ คลังสินค้า และต้นทุน</span><span class="sxs-lookup"><span data-stu-id="ef474-112">**Stock card summary** – View item or warehouse details by item group, site, warehouse, and cost.</span></span>

## <a name="set-up-the-generation-of-stock-card-reports"></a><span data-ttu-id="ef474-113">ตั้งค่าการสร้างรายงานบัตรสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ef474-113">Set up the generation of stock card reports</span></span>
<span data-ttu-id="ef474-114">ทำงานต่อไปนี้ให้เสร็จสมบูรณ์ก่อนที่คุณจะสร้างรายงานบัตรสินค้าคงคลัง:</span><span class="sxs-lookup"><span data-stu-id="ef474-114">Complete the following tasks before you generate a stock card report:</span></span>

-   <span data-ttu-id="ef474-115">สร้างรายการที่มีข้อมูลที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="ef474-115">Create an item that has the required information.</span></span> <span data-ttu-id="ef474-116">**หมายเหตุ:** กำหนดสำนักงานสาขาย่อยที่ยื่นให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="ef474-116">**Note:** Assign a tax branch to a site.</span></span>
-   <span data-ttu-id="ef474-117">สร้างสำนักงานสาขาย่อยที่ยื่น</span><span class="sxs-lookup"><span data-stu-id="ef474-117">Create a tax branch.</span></span>
-   <span data-ttu-id="ef474-118">ตั้งค่าสำนักงานสาขาย่อยที่ยื่นสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="ef474-118">Set up a tax branch for a legal entity.</span></span>
-   <span data-ttu-id="ef474-119">ตั้งค่าสำนักงานสาขาย่อยที่ยื่นสำหรับผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ef474-119">Set up a tax branch for a vendor or a customer.</span></span>
-   <span data-ttu-id="ef474-120">กำหนดสำนักงานสาขาย่อยที่ยื่นให้กับไซต์</span><span class="sxs-lookup"><span data-stu-id="ef474-120">Assign a tax branch to a site.</span></span>
-   <span data-ttu-id="ef474-121">สร้างและลงรายการบัญชีธุรกรรมการซื้อ การขาย และการโอนย้ายสินค้าคงคลังที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="ef474-121">Create and post required purchase, sale, and inventory transfer transactions.</span></span>

## <a name="recalculate-inventory-and-generate-the-financial-stock-card-report"></a><span data-ttu-id="ef474-122">คำนวณสินค้าคงคลังอีกครั้ง และสร้างรายงานบัตรสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ef474-122">Recalculate inventory and generate the financial stock card report</span></span>
<span data-ttu-id="ef474-123">ใช้หน้า **การปิดและการปรับปรุง** ในการคำนวณสินค้าคงคลังอีกครั้งหลังจากมีการรันกระบวนการปิดบัญชีสินค้าคงคลัง และสร้างรายงานบัตรสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ef474-123">Use the **Closing and adjustment** page to recalculate inventory after the inventory close process is run, and generate the financial stock card report.</span></span>

## <a name="generate-the-stock-card-report"></a><span data-ttu-id="ef474-124">สร้างรายงานบัตรสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ef474-124">Generate the stock card report</span></span>
<span data-ttu-id="ef474-125">คุณสามารถจัดกลุ่มสินค้าต่างๆ ตามไซต์ คลังสินค้า สถานที่เก็บ หมายเลขสินค้า หรือกลุ่มสินค้า และสร้างรายงานบัตรสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="ef474-125">You can group items by site, warehouse, location, item number, or item group, and then generate the stock card reports.</span></span> <span data-ttu-id="ef474-126">ใช้รายงาน **บัตรสินค้าคงคลัง – ตามจริง** ในการสร้างรายงานบัตรสินค้าคงคลังตามจริง</span><span class="sxs-lookup"><span data-stu-id="ef474-126">Use the **Stock card – Physical** report to generate the physical stock card report.</span></span> <span data-ttu-id="ef474-127">ใช้รายงาน **บัตรสินค้าคงคลัง – ทางการเงิน** ในการสร้างรายงานบัตรสินค้าคงคลังทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="ef474-127">Use the **Stock card – Financial** report to generate the financial stock card report.</span></span> <span data-ttu-id="ef474-128">คุณสามารถสร้างรายงานบัตรสินค้าคงคลังโดยละเอียดหรือโดยสรุป</span><span class="sxs-lookup"><span data-stu-id="ef474-128">You can generate a detailed or summarized stock card report.</span></span>




