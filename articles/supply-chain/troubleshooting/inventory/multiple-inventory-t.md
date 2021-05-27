---
title: รายการความเคลื่อนไหวของสินค้าคงคลังหลายรายการของหมายเลขชุดงานเมื่อปิดใช้งานการอัปเดตจริง
description: มีการสร้างรายการความเคลื่อนไหวของสินค้าคงคลังหลายรายการหลังจากที่คุณปรับปรุงบรรทัดใบสั่งซื้อให้กับสินค้าที่มีการตั้งค่าตัวเลือกในการอัปเดตจริง ของกลุ่มหมายเลขชุดงานเป็น ไม่
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026963"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="ab8f3-103">รายการความเคลื่อนไหวของสินค้าคงคลังหลายรายการของหมายเลขชุดงานเมื่อปิดใช้งานการอัปเดตจริง</span><span class="sxs-lookup"><span data-stu-id="ab8f3-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="ab8f3-104">หมายเลข KB: 4613390</span><span class="sxs-lookup"><span data-stu-id="ab8f3-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="ab8f3-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="ab8f3-105">Symptoms</span></span>

<span data-ttu-id="ab8f3-106">มีการสร้างรายการความเคลื่อนไหวของสินค้าคงคลังหลายรายการหลังจากที่คุณปรับปรุงบรรทัดใบสั่งซื้อให้กับสินค้าที่มีการตั้งค่าตัวเลือก **ในการอัปเดตจริง** ของกลุ่มหมายเลขชุดงานเป็น *ไม่*</span><span class="sxs-lookup"><span data-stu-id="ab8f3-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="ab8f3-107">เมื่อคุณสร้างสินค้าที่มีการตั้งค่าตัวเลือก **ในการอัปเดตจริง** ของกลุ่มหมายเลขชุดงานเป็น *ไม่* ระบบจะสร้างหมายเลขชุดงานใหม่โดยอัตโนมัติ ถ้าคุณแก้ไขปริมาณการสั่งซื้อและบันทึกหน้าใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="ab8f3-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ab8f3-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="ab8f3-108">Resolution</span></span>

<span data-ttu-id="ab8f3-109">การตั้งค่า **ในการอัปเดตจริง** ของกลุ่มหมายเลขชุดงานจะใช้ได้กับวิธีต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ab8f3-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="ab8f3-110">เมื่อตั้งค่าตัวเลือกเป็น *ใช่* หมายเลขชุดงานใหม่จะถูกสร้างขึ้นหลังจากการอัปเดตจริงเท่านั้น (ตัวอย่างเช่น เมื่อจัดส่งสินค้าหรือได้รับ)</span><span class="sxs-lookup"><span data-stu-id="ab8f3-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="ab8f3-111">เมื่อตั้งค่าตัวเลือกเป็น *ไม่* จะมีการสร้างหมายเลขชุดงานใหม่ทุกครั้งที่มีการอัปเดตที่เกี่ยวข้องเกิดขึ้น (ตัวอย่างเช่น เมื่อมีการเพิ่มปริมาณใหม่ที่ใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="ab8f3-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
