---
title: การสร้างคลาสการผลิต
description: 'ขั้นตอนนี้แสดงวิธีการตั้งค่าคลาสงาน '
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a965906bfbf6411986594ddd5c67beb426268367
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217114"
---
# <a name="create-a-work-class"></a><span data-ttu-id="838d3-103">การสร้างคลาสการผลิต</span><span class="sxs-lookup"><span data-stu-id="838d3-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="838d3-104">ขั้นตอนนี้แสดงวิธีการตั้งค่าคลาสงาน </span><span class="sxs-lookup"><span data-stu-id="838d3-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="838d3-105">คลาสงานถูกใช้เพื่อกำหนดและ/หรือจำกัดชนิดของรายการใบสั่งงานที่ผู้ปฏิบัติงานคลังสินค้าสามารถประมวลผลบนอุปกรณ์เคลื่อนที่ </span><span class="sxs-lookup"><span data-stu-id="838d3-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="838d3-106">รายการที่ผู้ปฏิบัติงานสามารถประมวลผลจะถูกกำหนดจากคลาสงานบนรายการเมนูอุปกรณ์เคลื่อนที่ที่ผู้ปฏิบัติงานคลังสินค้ามีการเข้าถึงและคลาสงานที่ระบุไว้ในรายการงาน</span><span class="sxs-lookup"><span data-stu-id="838d3-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="838d3-107">คลาสงานสามารถใช้เพื่อตรวจสอบสถานที่ส่งสินค้าสำหรับรายการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="838d3-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="838d3-108">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="838d3-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="838d3-109">ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="838d3-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="838d3-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > งาน > คลาสงาน</span><span class="sxs-lookup"><span data-stu-id="838d3-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="838d3-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="838d3-111">Click New.</span></span>
3. <span data-ttu-id="838d3-112">ในฟิลด์รหัสคลาสงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="838d3-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="838d3-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="838d3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="838d3-114">ในฟิลด์ชนิดใบสั่งงาน ให้เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="838d3-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="838d3-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="838d3-115">Click New.</span></span>
7. <span data-ttu-id="838d3-116">ในฟิลด์ชนิดสถานที่ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="838d3-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="838d3-117">ถ้าคุณเลือกชนิดสถานที่ นี่จะตั้งค่าข้อจำกัดสำหรับสถานที่ที่สามารถจัดเก็บสินค้าหลังจากที่ได้เบิกสินค้าไป</span><span class="sxs-lookup"><span data-stu-id="838d3-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="838d3-118">การตั้งค่านี้จะใช้เมื่อคำสั่งสถานที่พยายามแก้ไขที่ตั้ง หรือถ้าผู้ปฏิบัติงานคลังสินค้าระบุสถานที่จัดเก็บสินค้าในอุปกรณ์เคลื่อนที่ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="838d3-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="838d3-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="838d3-119">Close the page.</span></span>

