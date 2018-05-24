---
title: "การสร้างความต้องการสินค้าสำหรับใบสั่งบริการ"
description: "ถ้าคุณต้องการจองสินค้าเฉพาะสำหรับใบสั่งบริการ คุณสามารถสร้างความต้องการสินค้าคงคลังได้"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e76b0c636470a89ba2091363efe2f34eb3d58f88
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="22b66-103">การสร้างความต้องการสินค้าสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="22b66-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="22b66-104">คุณสามารถสร้างใบสั่งบริการเพื่อติดตาม และจัดการบริการซึ่งคุณนำเสนอให้แก่ลูกค้าของคุณได้</span><span class="sxs-lookup"><span data-stu-id="22b66-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="22b66-105">ถ้าคุณต้องการจองสินค้าเฉพาะสำหรับใบสั่งบริการ คุณสามารถสร้างความต้องการสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="22b66-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="22b66-106">ความต้องการสินค้าอาจถูกใช้ทันทีจากสินค้าคงคลัง หรือจะสามารถเริ่มต้นใบสั่งผลิตสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="22b66-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="22b66-107">โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต</span><span class="sxs-lookup"><span data-stu-id="22b66-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="22b66-108">ข้อกำหนดรายการสำหรับใบสั่งรายการมีการประมวลผลผ่านโครงการ </span><span class="sxs-lookup"><span data-stu-id="22b66-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="22b66-109">เมื่อต้องการสร้างความต้องการสินค้าในใบสั่งบริการ ใบสั่งบริการต้องกำหนดให้กับโครงการ </span><span class="sxs-lookup"><span data-stu-id="22b66-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="22b66-110">หลังจากที่คุณสร้างความต้องการสินค้าสำหรับใบสั่งบริการ คุณสามารถดูความต้องการสินค้าได้ในแบบฟอร์ม **โครงการ** สำหรับโครงการที่เลือก</span><span class="sxs-lookup"><span data-stu-id="22b66-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="22b66-111">สร้างความต้องการสินค้าสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="22b66-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="22b66-112">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="22b66-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="22b66-113">เลือกใบสั่งบริการที่คุณต้องการสร้างความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="22b66-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="22b66-114">ใน **บานหน้าต่างการดำเนินการ** บนแท็บ **การจัดส่ง** คลิก **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="22b66-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="22b66-115">ในแบบฟอร์ม **ความต้องการสินค้า** ป้อนข้อมูลสำหรับสินค้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="22b66-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="22b66-116">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟิลด์ที่ระบุ ดู [ความต้องการสินค้า (แบบฟอร์ม)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="22b66-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="22b66-117">สร้างความต้องการสินค้าสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="22b66-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="22b66-118">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="22b66-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="22b66-119">เปิดข้อตกลงการให้บริการที่คุณต้องการสร้างความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="22b66-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="22b66-120">บน FastTab **รายการ** คลิก **เพิ่ม** เพื่อสร้างรายการใหม่</span><span class="sxs-lookup"><span data-stu-id="22b66-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="22b66-121">ในฟิลด์ **ชนิดของธุรกรรม** เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="22b66-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="22b66-122">ในฟิลด์ **การตั้งค่าสินค้า** เลือก **ความต้องการสินค้า**</span><span class="sxs-lookup"><span data-stu-id="22b66-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="22b66-123">ในฟิลด์ **หมายเลขสินค้า** เลือกสินค้าที่จำเป็นสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="22b66-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="22b66-124">บน FastTab **รายละเอียดรายการ** บนแท็บ **มิติของผลิตภัณฑ์** ในฟิลด์ **ไซต์** เลือกไซต์สินค้าคงคลังสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="22b66-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="22b66-125">เมื่อต้องการสร้างใบสั่งบริการจากรายการข้อตกลง บน FastTab **รายการ** คลิก **สร้างใบสั่งบริการ** แล้วป้อนข้อมูลที่เกี่ยวข้องในแบบฟอร์ม **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="22b66-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="22b66-126">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="22b66-126">See also</span></span>

<span data-ttu-id="22b66-127">[สร้างใบสั่งบริการโดยอัตโนมัติ](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="22b66-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  



