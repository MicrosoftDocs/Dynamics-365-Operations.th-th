---
title: "ใบสั่งซื้อสำหรับโครงการ"
description: "บทความนี้อธิบายวิธีที่หลากหลายที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการได้  วิธีการที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อ และถูกคิดค่าธรรมเนียมไปยังโครงการ"
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1797bc49877f1c8c06797083d1c7b76934675ba3
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="940f0-104">ใบสั่งซื้อสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="940f0-105">บทความนี้อธิบายวิธีที่หลากหลายที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการได้ </span><span class="sxs-lookup"><span data-stu-id="940f0-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="940f0-106">วิธีการที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อ และถูกคิดค่าธรรมเนียมไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="940f0-107">ใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition คุณสามารถใช้วิธีการต่างๆเพื่อสร้างใบสั่งซื้อสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="940f0-108">วิธีการที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ เมื่อมีการใช้สินค้าที่ซื้อ และเมื่อสินค้าที่ซื้อถูกคิดค่าธรรมเนียมไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="940f0-109">วิธีการสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="940f0-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="940f0-110">คุณสามารถใช้หนึ่งในวิธีต่อไปนี้ เพื่อสร้างใบสั่งซื้อในการจัดการโครงการและการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="940f0-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="940f0-111">วัตถุประสงค์ของใบสั่งซื้อจะเป็นตัวกำหนดว่าจะมีการใช้ใบสั่งซื้อเมื่อใดและคิดค่าใช้จ่ายสำหรับสินค้าในโครงการเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="940f0-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="940f0-112">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="940f0-112">Method</span></span></th>
<th><span data-ttu-id="940f0-113">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="940f0-113">Purpose</span></span></th>
<th><span data-ttu-id="940f0-114">ปริมาณการใช้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="940f0-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="940f0-115">สร้างใบสั่งซื้อโดยตรงจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="940f0-116">ใช้วิธีการนี้เพื่อซื้อสินค้าจากผู้จัดจำหน่ายภายนอก สำหรับการใช้วัสดุในโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="940f0-117">คุณสามารถสร้างใบสั่งซื้อได้ในสองลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="940f0-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="940f0-118">จากตัวโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="940f0-118">From the project itself.</span></span> <span data-ttu-id="940f0-119">ในกรณีนี้ จะมีการกำหนดโครงการไว้แล้วสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="940f0-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="940f0-120">โดยการนำทางไปยังโครงการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="940f0-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="940f0-121">คุณต้องเลือกทั้งผู้จัดจำหน่ายและโครงการที่จะสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="940f0-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="940f0-122">สินค้ามีการใช้เมื่อมีการอัพเดตใบแจ้งหนี้จากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="940f0-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="940f0-123">สร้างใบสั่งซื้อจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="940f0-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="940f0-124">ใช้วิธีนี้เพื่อซื้อสินค้า เมื่อคุณสร้างใบสั่งขายจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="940f0-125">สินค้าจะถูกใช้เมื่อมีการออกอินวอยซ์ใบสั่งขายให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="940f0-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="940f0-126">สร้างใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="940f0-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="940f0-127">ใช้วิธีนี้เพื่อซื้อสินค้า เมื่อคุณสร้างความต้องการสินค้าจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="940f0-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="940f0-128">สินค้ามีการใช้เมื่อมีการอัพเดตบันทึกการจัดส่งตามความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="940f0-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="940f0-129">เมื่อคุณอัพเดตใบแจ้งหนี้ของผู้จัดจำหน่ายหรือบันทึกการจัดส่ง คุณจะได้รับข้อความเตือนให้อัพเดตบันทึกการจัดส่งสำหรับความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="940f0-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="940f0-130">สำหรับข้อมูลเพิ่มเติม โปรดดู [รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า](tasks/receive-items-purchase-order-item-requirement.md)</span><span class="sxs-lookup"><span data-stu-id="940f0-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


