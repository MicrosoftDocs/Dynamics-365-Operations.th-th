---
title: ความต้องการสินค้าในใบสั่งบริการ
description: ถ้าคุณต้องการจองสินค้าเฉพาะสำหรับใบสั่งบริการ คุณสามารถสร้างความต้องการสินค้าคงคลังได้
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8866d8a4d6ad879f2c43b470af98457cb7c75721
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985751"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="ea7ee-103">ความต้องการสินค้าในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ea7ee-104">คุณสามารถสร้างใบสั่งบริการเพื่อติดตาม และจัดการบริการซึ่งคุณนำเสนอให้แก่ลูกค้าของคุณได้</span><span class="sxs-lookup"><span data-stu-id="ea7ee-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="ea7ee-105">ถ้าคุณต้องการจองสินค้าเฉพาะสำหรับใบสั่งบริการ คุณสามารถสร้างความต้องการสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="ea7ee-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="ea7ee-106">ความต้องการสินค้าอาจถูกใช้ทันทีจากสินค้าคงคลัง หรือจะสามารถเริ่มต้นใบสั่งผลิตสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="ea7ee-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="ea7ee-107">โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="ea7ee-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="ea7ee-108">ข้อกำหนดรายการสำหรับใบสั่งรายการมีการประมวลผลผ่านโครงการ </span><span class="sxs-lookup"><span data-stu-id="ea7ee-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="ea7ee-109">ในการสร้างข้อกำหนดรายการบนใบสั่งบริการ ใบสั่งบริการจะต้องแนบกับโครงการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="ea7ee-110">ทันทีที่ข้อกำหนดรายการถูกสร้างขึ้นสำหรับใบสั่งบริการ จะสามารถดูได้จาก **โครงการ** ในใบสั่งบริการแต่ละรายการ หรือผ่านฟอร์ม **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="ea7ee-111">การดูข้อกำหนดรายการจากใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="ea7ee-112">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ea7ee-113">คลิก **ส่ง** แล้วคลิก **ความต้องการสินค้า** เพื่อเปิดแบบฟอร์ม **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="ea7ee-114">คลิกแท็บ **โครงการ** และตรวจสอบฟิลด์ **ใบสั่งบริการ** เพื่อดูใบสั่งบริการของความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="ea7ee-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="ea7ee-115">การลบใบสั่งบริการที่มีข้อกำหนดรายการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="ea7ee-116">ถ้าข้อกำหนดรายการสร้างขึ้นบนใบสั่งบริการ คุณไม่สามารถลบใบสั่งบริการได้ </span><span class="sxs-lookup"><span data-stu-id="ea7ee-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="ea7ee-117">คุณต้องลบความต้องการสินค้าก่อนที่คุณจะสามารถลบใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="ea7ee-118">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ea7ee-119">คลิก **ส่ง** แล้วคลิก **ความต้องการสินค้า** เพื่อเปิดแบบฟอร์ม **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="ea7ee-120">แบบฟอร์มนี้แสดงความต้องการสินค้าที่สร้างขึ้นในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="ea7ee-121">เลือกความต้องการสินค้าที่จะลบ แล้วคลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="ea7ee-122">หรือ</span><span class="sxs-lookup"><span data-stu-id="ea7ee-122">–or–</span></span>

1.  <span data-ttu-id="ea7ee-123">คลิก **การจัดการโครงการและการบัญชี** \> **ทั่วไป** \> **โครงการ** \> **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="ea7ee-124">เปิดโครงการที่มีใบสั่งบริการที่สร้างความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="ea7ee-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="ea7ee-125">ในแบบฟอร์ม **โครงการ** ในบานหน้าต่างด้านขวา คลิก **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="ea7ee-126">ฟอร์ม **ความต้องการสินค้า** แสดงรายการความต้องการสินค้าที่มีความสัมพันธ์กับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ea7ee-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="ea7ee-127">เลือกความต้องการสินค้าที่จะลบ แล้วคลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="ea7ee-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea7ee-128">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="ea7ee-128">See also</span></span>

<span data-ttu-id="ea7ee-129">[ความต้องการสินค้า (แบบฟอร์ม)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="ea7ee-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

