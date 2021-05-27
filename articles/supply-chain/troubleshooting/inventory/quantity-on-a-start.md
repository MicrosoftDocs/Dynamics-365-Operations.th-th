---
title: ปริมาณในใบสั่งตรวจสอบสินค้าที่เริ่มต้นไม่มีการอัปเดตเมื่อแบ่งใบสั่ง
description: เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าและพยายามแบ่ง ใบสั่งไม่มีการอัปเดตเป็นปริมาณคงเหลือที่แบ่ง
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026962"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="9f93e-103">ปริมาณในใบสั่งตรวจสอบสินค้าที่เริ่มต้นไม่มีการอัปเดตเมื่อแบ่งใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="9f93e-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="9f93e-104">หมายเลข KB: 4613113</span><span class="sxs-lookup"><span data-stu-id="9f93e-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="9f93e-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="9f93e-105">Symptoms</span></span>

<span data-ttu-id="9f93e-106">เมื่อคุณสร้างใบสั่งตรวจสอบสินค้าและพยายามแบ่ง ใบสั่งไม่มีการอัปเดตเป็นปริมาณคงเหลือหลังการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="9f93e-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="9f93e-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="9f93e-107">Resolution</span></span>

<span data-ttu-id="9f93e-108">ระบบจะไม่เปลี่ยนปริมาณเดิมจากใบสั่งตรวจสอบสินค้า เพื่อให้แน่ใจว่าคุณสามารถติดตามปริมาณเดิมที่สร้างไว้ให้กับใบสั่งตรวจสอบสินค้านั้น</span><span class="sxs-lookup"><span data-stu-id="9f93e-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="9f93e-109">อย่างไรก็ตาม ระบบจะติดตามปริมาณที่แบ่งจากใบสั่งตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="9f93e-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="9f93e-110">เมื่อต้องการติดตามนี้ จะใช้ฟิลด์ฐานข้อมูลที่ชื่อ `QuantityThatHasSplitIntoOtherQuarantineOrders`</span><span class="sxs-lookup"><span data-stu-id="9f93e-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="9f93e-111">อย่างไรก็ตาม ฟิลด์นี้ไม่ปรากฏในอินเทอร์เฟสผู้ใช้ (UI)</span><span class="sxs-lookup"><span data-stu-id="9f93e-111">However, this field isn't visible in the user interface (UI).</span></span>
