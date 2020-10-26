---
title: ตั้งค่ารหัสการโอนการครอบครอง
description: 'ขั้นตอนนี้มุ่งเน้นการตั้งค่ารหัสการโอนการครอบครองที่สามารถใช้บนอุปกรณ์เคลื่อนที่สำหรับกระบวนการการได้รับสินค้าส่งคืนที่ '
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9962b92b4e9ef5500d1cd3d2db6e2448b708b97
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983756"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="a992e-103">ตั้งค่ารหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="a992e-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a992e-104">ขั้นตอนนี้มุ่งเน้นการตั้งค่ารหัสการโอนการครอบครองที่สามารถใช้บนอุปกรณ์เคลื่อนที่สำหรับกระบวนการการได้รับสินค้าส่งคืนที่ </span><span class="sxs-lookup"><span data-stu-id="a992e-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="a992e-105">รหัสการโอนการครอบครองคือชุดของกฎที่สามารถใช้เมื่อได้รับสินค้า</span><span class="sxs-lookup"><span data-stu-id="a992e-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="a992e-106">ตัวอย่างเช่น เมื่อผู้ใช้งานใช้อุปกรณ์เคลื่อนที่ในการรับสินค้าที่ได้รับความเสียหาย ผู้ใช้ต้องสแกนรหัสการโอนการครอบครองสำหรับสินค้าที่เสียหาย</span><span class="sxs-lookup"><span data-stu-id="a992e-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="a992e-107">สถานะสินค้าคงคลังของสินค้าที่ได้รับ เท็มเพลตงาน และคำสั่งสถานที่สามารถกำหนดได้จากรหัสการโอนการครอบครองที่สแกน</span><span class="sxs-lookup"><span data-stu-id="a992e-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="a992e-108">สำหรับกระบวนการรับใบสั่งซื้อและใบสั่งผลิตรายงานเป็นกระบวนการที่เสร็จสิ้นแล้ว การใช้รหัสการโอนการครอบครองเป็นเพียงตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="a992e-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="a992e-109">สำหรับกระบวนการรับการส่งคืนใบสั่งขาย ถ้าสินค้ามีการลงทะเบียนโดยใช้อุปกรณ์เคลื่อนที่ การใช้รหัสการโอนการครอบครองจะเป็นข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="a992e-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="a992e-110">คำแนะนำนี้ถูกสร้างโดยใช้ข้อมูลสาธิตของบริษัท USMF </span><span class="sxs-lookup"><span data-stu-id="a992e-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="a992e-111">ขั้นตอนนี้มีไว้สำหรับผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="a992e-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="a992e-112">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="a992e-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="a992e-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a992e-113">Click New.</span></span>
    * <span data-ttu-id="a992e-114">สร้างรหัสการโอนการครอบครองใหม่เพื่อใช้สำหรับการส่งคืนของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a992e-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="a992e-115">ในฟิลด์รหัสการโอนการครอบครอง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a992e-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="a992e-116">ในฟิลด์สถานะสินค้าคงคลัง เลือกสถานะสินค้าคงคลังที่มีการบล็อคสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="a992e-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="a992e-117">ถ้าคุณกำลังใช้ USMF เลือก 'การบล็อค'</span><span class="sxs-lookup"><span data-stu-id="a992e-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="a992e-118">คุณสามารถเพิ่มสถานะสินค้าคงคลังไปยังรหัสการโอนการครอบครองเพื่อแทนที่สถานะเริ่มต้นที่อยู่บนรายการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a992e-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="a992e-119">ในฟิลด์เท็มเพลตงาน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a992e-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="a992e-120">ไม่จำเป็นต้องระบุ: เลือกรหัสเท็มเพลงานที่เชื่อมโยงกับใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="a992e-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="a992e-121">ถ้าไม่ระบุค่า เท็มเพลตงานจะถูกแก้ไขตามกฎมาตรฐานที่กำหนดค่าไว้ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="a992e-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="a992e-122">การเลือกเท็มเพลตงานจะจำกัดรหัสการโอนการครอบครองที่สามารถใช้ได้</span><span class="sxs-lookup"><span data-stu-id="a992e-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="a992e-123">ตัวอย่างเช่น ถ้ารหัสการโอนการครอบครองมีเท็มเพลตงานที่มีใบสั่งงานเป็นชนิดใบสั่งซื้อ จะไม่สามารถใช้เพื่อลงทะเบียนสินค้าที่ถูกส่งคืนโดยลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a992e-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="a992e-124">ในฟิลด์รหัสการโอนการครอบครองสินค้ารับคืน ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a992e-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="a992e-125">รหัสการโอนการครอบครองการส่งคืนกำหนดส่วนที่เหลือของกระบวนการใบสั่งส่งคืนสำหรับสินค้าลงทะเบียน </span><span class="sxs-lookup"><span data-stu-id="a992e-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="a992e-126">ในตัวอย่างนี้ ลูกค้าควรได้รับใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="a992e-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="a992e-127">เพิ่มรหัสการจัดการส่งคืนสินค้าที่ประกอบด้วยเครดิตการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="a992e-127">Add a returns disposition code that contains an action Credit.</span></span>  

