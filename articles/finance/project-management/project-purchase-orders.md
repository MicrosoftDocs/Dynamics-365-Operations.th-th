---
title: ใบสั่งซื้อสำหรับโครงการ
description: บทความนี้อธิบายวิธีที่หลากหลายที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการได้  วิธีการที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อ และถูกคิดค่าธรรมเนียมไปยังโครงการ
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174569"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="8eb28-104">ใบสั่งซื้อสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eb28-105">บทความนี้อธิบายวิธีที่หลากหลายที่คุณสามารถใช้เพื่อสร้างใบสั่งซื้อสำหรับโครงการได้ </span><span class="sxs-lookup"><span data-stu-id="8eb28-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="8eb28-106">วิธีการที่คุณใช้ขึ้นอยู่กับวัตถุประสงค์ของใบสั่งซื้อ และเมื่อมีการใช้สินค้าที่ซื้อ และถูกคิดค่าธรรมเนียมไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="8eb28-107">วิธีการสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8eb28-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="8eb28-108">คุณสามารถใช้หนึ่งในวิธีต่อไปนี้ เพื่อสร้างใบสั่งซื้อในการจัดการโครงการและการบัญชีได้</span><span class="sxs-lookup"><span data-stu-id="8eb28-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="8eb28-109">วัตถุประสงค์ของใบสั่งซื้อจะเป็นตัวกำหนดว่าจะมีการใช้ใบสั่งซื้อเมื่อใดและคิดค่าใช้จ่ายสำหรับสินค้าในโครงการเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="8eb28-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8eb28-110">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-110">Method</span></span></th>
<th><span data-ttu-id="8eb28-111">วัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="8eb28-111">Purpose</span></span></th>
<th><span data-ttu-id="8eb28-112">ปริมาณการใช้ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8eb28-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8eb28-113">สร้างใบสั่งซื้อโดยตรงจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="8eb28-114">ใช้วิธีการนี้เพื่อซื้อสินค้าจากผู้จัดจำหน่ายภายนอก สำหรับการใช้วัสดุในโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="8eb28-115">คุณสามารถสร้างใบสั่งซื้อได้ในสองลักษณะ:</span><span class="sxs-lookup"><span data-stu-id="8eb28-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="8eb28-116">จากตัวโครงการเอง</span><span class="sxs-lookup"><span data-stu-id="8eb28-116">From the project itself.</span></span> <span data-ttu-id="8eb28-117">ในกรณีนี้ จะมีการกำหนดโครงการไว้แล้วสำหรับใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8eb28-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="8eb28-118">โดยการนำทางไปยังโครงการใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8eb28-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="8eb28-119">คุณต้องเลือกทั้งผู้จัดจำหน่ายและโครงการที่จะสร้างใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8eb28-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="8eb28-120">สินค้ามีการใช้เมื่อมีการอัพเดตใบแจ้งหนี้จากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8eb28-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eb28-121">สร้างใบสั่งซื้อจากใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="8eb28-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="8eb28-122">ใช้วิธีนี้เพื่อซื้อสินค้า เมื่อคุณสร้างใบสั่งขายจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="8eb28-123">สินค้าจะถูกใช้เมื่อมีการออกอินวอยซ์ใบสั่งขายให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8eb28-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eb28-124">สร้างใบสั่งซื้อจากความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="8eb28-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="8eb28-125">ใช้วิธีนี้เพื่อซื้อสินค้า เมื่อคุณสร้างความต้องการสินค้าจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="8eb28-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="8eb28-126">สินค้ามีการใช้เมื่อมีการอัพเดตบันทึกการจัดส่งตามความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="8eb28-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="8eb28-127">เมื่อคุณอัพเดตใบแจ้งหนี้ของผู้จัดจำหน่ายหรือบันทึกการจัดส่ง คุณจะได้รับข้อความเตือนให้อัพเดตบันทึกการจัดส่งสำหรับความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="8eb28-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="8eb28-128">สำหรับข้อมูลเพิ่มเติม โปรดดู [รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า](tasks/receive-items-purchase-order-item-requirement.md)</span><span class="sxs-lookup"><span data-stu-id="8eb28-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

