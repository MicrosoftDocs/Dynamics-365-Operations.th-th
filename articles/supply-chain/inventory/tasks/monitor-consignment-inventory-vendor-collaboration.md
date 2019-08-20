---
title: ตรวจสอบสินค้าคงคลังที่มีการส่งมอบโดยใช้การทำงานร่วมกันกับผู้จัดจำหน่าย
description: 'กระบวนงานนี้แสดงวิธีการใช้การทำงานร่วมกันกับผู้จัดจำหน่ายเพื่อดูรายละเอียดเกี่ยวกับระดับสินค้าคงคลังของผลิตภัณฑ์ที่คุณได้ทำในการส่งมอบให้กับลูกค้า '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfbe5e9de7b700d991e0826fb4387de416ce242a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845415"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="2aa4e-103">ตรวจสอบสินค้าคงคลังที่มีการส่งมอบโดยใช้การทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="2aa4e-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2aa4e-104">กระบวนงานนี้แสดงวิธีการใช้การทำงานร่วมกันกับผู้จัดจำหน่ายเพื่อดูรายละเอียดเกี่ยวกับระดับสินค้าคงคลังของผลิตภัณฑ์ที่คุณได้ทำในการส่งมอบให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="2aa4e-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="2aa4e-105">คุณยังสามารถตรวจสอบปริมาณการใช้สินค้าคงคลังเมื่อลูกค้ากลายเป็นเจ้าของสินค้าคงคลังได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2aa4e-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="2aa4e-106">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2aa4e-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="2aa4e-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="2aa4e-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="2aa4e-108">ดูสินค้าคงคลังที่ใช้</span><span class="sxs-lookup"><span data-stu-id="2aa4e-108">View consumed inventory</span></span>
1. <span data-ttu-id="2aa4e-109">ไปที่ การทำงานร่วมกันกับผู้จัดจำหน่าย > สินค้าคงคลังที่มีการส่งมอบ > ผลิตภัณฑ์ที่ได้รับจากสินค้าคงคลังที่มีการส่งมอบ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="2aa4e-110">รายการจะแสดงรายการใบรับสินค้าที่สร้างขึ้นเมื่อความเป็นเจ้าของสินค้าคงคลังที่มีการส่งมอบเปลี่ยนจากผู้จัดจำหน่ายเป็นลูกค้า </span><span class="sxs-lookup"><span data-stu-id="2aa4e-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="2aa4e-111">คุณอาจต้องเลื่อนไปทางขวาเพื่อดูปริมาณและข้อมูลอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="2aa4e-112">คุณสามารถใช้ข้อมูลในรายการนี้ในการสร้างใบแจ้งหนี้สำหรับลูกค้าของคุณ </span><span class="sxs-lookup"><span data-stu-id="2aa4e-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="2aa4e-113">นอกจากนี้ คุณยังสามารถส่งออกข้อมูลไปยัง Microsoft Excel ได้</span><span class="sxs-lookup"><span data-stu-id="2aa4e-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="2aa4e-114">คลิก ดูรายการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-114">Click View purchase order.</span></span>
3. <span data-ttu-id="2aa4e-115">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="2aa4e-116">รายการถูกทำเครื่องหมายเป็นการส่งมอบ และส่วนหัวแสดงให้เห็นว่าใบสั่งซื้อมีสถานะเป็นได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="2aa4e-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="2aa4e-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2aa4e-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="2aa4e-118">ดูสินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-118">View on-hand inventory</span></span>
1. <span data-ttu-id="2aa4e-119">ไปที่ การทำงานร่วมกันกับผู้จัดจำหน่าย > สินค้าคงคลังที่มีการส่งมอบ > ปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="2aa4e-120">หน้าสินค้าคงคลังที่มีการส่งมอบคงเหลือแสดงสินค้าคงคลังที่คุณเป็นเจ้าของที่คลังสินค้าของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="2aa4e-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="2aa4e-121">คุณสามารถแสดงมิติเพิ่มเติม เช่น ไซต์และคลังสินค้าได้โดยการคลิกแท็บแสดงมิติ</span><span class="sxs-lookup"><span data-stu-id="2aa4e-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

