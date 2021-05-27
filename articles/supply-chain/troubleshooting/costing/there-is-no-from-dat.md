---
title: ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า
description: ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026964"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="7caf5-103">ไม่มีค่าวันที่เริ่มต้นบนแท็บราคาที่ใช้งานอยู่ของหน้าราคาสินค้า</span><span class="sxs-lookup"><span data-stu-id="7caf5-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="7caf5-104">หมายเลข KB: 4613548</span><span class="sxs-lookup"><span data-stu-id="7caf5-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="7caf5-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="7caf5-105">Symptoms</span></span>

<span data-ttu-id="7caf5-106">ไม่มีค่า **วันที่เริ่มต้น** บนแท็บ **ราคาที่ใช้งานอยู่** ของหน้า **ราคาสินค้า**</span><span class="sxs-lookup"><span data-stu-id="7caf5-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="7caf5-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="7caf5-107">Resolution</span></span>

<span data-ttu-id="7caf5-108">ค่า **วันที่เริ่มต้น** (วันที่มีผลบังคับใช้) ที่ตั้งค่าบนราคาที่ค้างอยู่จะไม่โอนย้ายไปที่ราคาที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="7caf5-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="7caf5-109">เมื่อเรกคอร์ดต้นทุนสินค้าถูกป้อนเป็นครั้งแรก จะมีสถานะและวันที่มีผลบังคับใช้ *รอดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="7caf5-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="7caf5-110">เมื่อคุณเรียกใช้งานเรกคอร์ดต้นทุนสินค้า จะมีการอัพเดตสถานะเป็น *ที่ใช้งานอยู่* และวันที่มีผลบังคับถูกอัพเดตเป็นวันที่เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="7caf5-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="7caf5-111">วันที่เรียกใช้ของราคาที่ใช้งานอยู่จะเป็นวันที่จริงของการเรียกใช้งานเสมอ</span><span class="sxs-lookup"><span data-stu-id="7caf5-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="7caf5-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของรุ่นการคิดต้นทุน](../../cost-management/costing-versions.md)</span><span class="sxs-lookup"><span data-stu-id="7caf5-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
