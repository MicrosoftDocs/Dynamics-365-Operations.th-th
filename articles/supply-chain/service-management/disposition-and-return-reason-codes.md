---
title: "รหัสการโอนการครอบครองและรหัสเหตุผลการส่งคืน"
description: "สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e37bd328ebceacc8acf134c5fbb20e6d6a6428d5
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="disposition-codes-and-return-reason-codes"></a><span data-ttu-id="da544-103">รหัสการโอนการครอบครองและรหัสเหตุผลการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="da544-103">Disposition codes and return reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="da544-104">สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="da544-104">Create and use return reason codes and disposition codes to support the process for returning products.</span></span>

<span data-ttu-id="da544-105">ใช้รหัสเหตุผลการส่งคืนใช้เพื่ออธิบายเหตุผลที่ลูกค้าต้องการส่งคืนสินค้า </span><span class="sxs-lookup"><span data-stu-id="da544-105">Use a return reason code to describe the reason that the customer wants to return an item.</span></span> <span data-ttu-id="da544-106">คุณสามารถกำหนดรหัสเหตุผลในแบบฟอร์ม **สร้างใบสั่งส่งคืนสินค้า** ได้</span><span class="sxs-lookup"><span data-stu-id="da544-106">You can assign a reason code in the **Create return orders** form.</span></span>

<span data-ttu-id="da544-107">กำหนดรหัสการโอนการครอบครองเมื่อรับสินค้า หรือในระหว่างการตรวจสอบทางกายภาพของสินค้าที่ส่งคืน </span><span class="sxs-lookup"><span data-stu-id="da544-107">Assign a disposition code when an item is received or during the physical inspection of a returned item.</span></span> <span data-ttu-id="da544-108">คุณสามารถใช้รหัสการโอนการครอบครองเพื่ออธิบายเงื่อนไขของสินค้า </span><span class="sxs-lookup"><span data-stu-id="da544-108">You can use disposition codes to describe the condition of the item.</span></span> <span data-ttu-id="da544-109">คุณยังสามารถใช้รหัสการโอนการครอบครองเพื่อบ่งชี้ว่าการดำเนินการเพิ่มเติมจำเป็นสำหรับธุรกรรมหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="da544-109">You can also use disposition codes to indicate whether additional action is required for the transaction.</span></span> <span data-ttu-id="da544-110">ตัวอย่างเช่น สร้างรหัสการโอนการครอบครองสำหรับการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="da544-110">For example, create disposition codes for the following actions:</span></span>

  - <span data-ttu-id="da544-111">ทำสินค้าที่ส่งคืนเป็นของเสียและระบุสินค้าทดแทนให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="da544-111">Scrap the returned item and provide a replacement item to the customer.</span></span>

  - <span data-ttu-id="da544-112">ส่งคืนสินค้าไปยังสินค้าคงคลัง และเครดิตลูกค้าสำหรับต้นทุนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="da544-112">Return the item to inventory and credit the customer for the cost of the item.</span></span>

  - <span data-ttu-id="da544-113">ซ่อมสินค้าและส่งกลับให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="da544-113">Repair the item and return it to the customer.</span></span>

## <a name="see-also"></a><span data-ttu-id="da544-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="da544-114">See also</span></span>

[<span data-ttu-id="da544-115">การตั้งค่ารหัสเหตุผลการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="da544-115">Set up return reason codes</span></span>](set-up-return-reason-code.md)

[<span data-ttu-id="da544-116">ตั้งค่ารหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="da544-116">Set up disposition codes</span></span>](set-up-disposition-codes.md)




  



