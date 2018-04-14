--- 
title: "สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน"
description: "กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน "
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4d7e1115d8a53a6667768dd5da1dc0cffded61cd
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="da3fb-103">สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="da3fb-103">Create a mobile device menu item for license plate consolidation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da3fb-104">กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน </span><span class="sxs-lookup"><span data-stu-id="da3fb-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="da3fb-105">ซึ่งช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถรวมรายการต่างๆ ได้ในป้ายทะเบียนเดียว โดยมีรายการต่างๆ ในป้ายทะเบียนอื่นที่อยู่ในสถานที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="da3fb-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="da3fb-106">ตัวอย่างเช่น พวกเขาอาจใช้สิ่งนี้ถ้าขั้นตอนการแบ่งระยะถัดไปในใบสั่งงานทั้งสองเหมือนกัน เพื่อให้จำเป็นต้องดำเนินงานเพียงหนึ่งครั้งสำหรับสินค้าผสม</span><span class="sxs-lookup"><span data-stu-id="da3fb-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="da3fb-107">คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="da3fb-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="da3fb-108">โดยทั่วไปงานเหล่านี้จะถูกดำเนินการโดยผู้จัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="da3fb-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="da3fb-109">ขั้นตอนนี้ใช้สำหรับคุณลักษณะที่ถูกเพิ่มเข้ามาใน Dynamics 365 for Operations version 1611</span><span class="sxs-lookup"><span data-stu-id="da3fb-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="da3fb-110">ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="da3fb-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="da3fb-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="da3fb-111">Click New.</span></span>
3. <span data-ttu-id="da3fb-112">ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="da3fb-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="da3fb-113">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="da3fb-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="da3fb-114">ในฟิลด์โหมด เลือก 'ทางอ้อม'</span><span class="sxs-lookup"><span data-stu-id="da3fb-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="da3fb-115">ในฟิลด์รหัสกิจกรรม เลือก 'รวมป้ายทะเบียน'</span><span class="sxs-lookup"><span data-stu-id="da3fb-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


