---
title: ผลิตภัณฑ์ถูกระงับสำหรับธุรกรรม
description: หลังจากที่คุณยืนยันใบสั่งการวางแผนแล้ว คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าสินค้าถูกระงับไว้สำหรับธุรกรรม
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301290"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="9e9db-103">ผลิตภัณฑ์ถูกระงับสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9e9db-103">Product is on hold for transactions</span></span>

<span data-ttu-id="9e9db-104">รหัสข้อผิดพลาด: SYS13295</span><span class="sxs-lookup"><span data-stu-id="9e9db-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="9e9db-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="9e9db-105">Symptoms</span></span>

<span data-ttu-id="9e9db-106">หลังจากคุณยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9e9db-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="9e9db-107">สินค้า %1 คงค้างอยู่สำหรับธุรกรรมใน %2</span><span class="sxs-lookup"><span data-stu-id="9e9db-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="9e9db-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="9e9db-108">Cause</span></span>

<span data-ttu-id="9e9db-109">เมื่ออธิบายสินค้าที่ถูกบล็อค ระบบจะใช้เงื่อนไข *ที่ถูกบล็อค* *หยุด* และ *ระงับ* แบบเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="9e9db-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="9e9db-110">ข้อผิดพลาดนี้หมายความว่าสินค้ามีการตั้งค่าเป็น **หยุด** ในการตั้งค่าใบสั่งเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9e9db-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="9e9db-111">ถ้าสินค้าถูกบล็อค คุณเพิ่มสินค้าที่ใบสั่งซื้อหรือรายการใบสั่งขาย คุณจะได้รับข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="9e9db-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="9e9db-112">เมื่อสินค้าถูกบล็อก คุณจะไม่สามารถปรับเปลี่ยนรายการความเคลื่อนไหวของสินค้าคงคลังที่เกี่ยวข้องกับใบสั่งซื้อหรือรายการใบสั่งขายได้ (ตัวอย่างเช่น เมื่อคุณลงรายการบัญชีบันทึกการจัดส่งหรือใบแจ้งหนี้)</span><span class="sxs-lookup"><span data-stu-id="9e9db-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="9e9db-113">คุณสามารถบล็อกสินค้าที่ซื้อและขายสินค้าในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="9e9db-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="9e9db-114">ในกรณีนี้ เลือกกล่องกาเครื่องหมาย **หยุด** ในใบสั่งซื้อ แต่สินค้าไม่มีการบล็อกในสินค้าคงคลังหรือใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="9e9db-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="9e9db-115">ต่อไปนี้เป็นเงื่อนไขบางอย่างที่อาจทําให้หมายเลขสินค้าถูกบล็อคไม่ให้ขาย</span><span class="sxs-lookup"><span data-stu-id="9e9db-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="9e9db-116">สินค้ายังคงอยู่ระหว่างการพัฒนาหรือการผลิต</span><span class="sxs-lookup"><span data-stu-id="9e9db-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="9e9db-117">ดังนั้นคุณจึงไม่ต้องการให้มีการขายหรือจองไว้</span><span class="sxs-lookup"><span data-stu-id="9e9db-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="9e9db-118">คุณได้รับสินค้าที่บกพร่องจำนวนมาก และต้องมีการแก้ไขข้อบกพร่องก่อนที่จะขายสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="9e9db-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="9e9db-119">ในกรณีชนิดนี้ คุณสามารถบล็อกสินค้าจนกว่าจะแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="9e9db-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="9e9db-120">หากสินค้าถูกบล็อก และคุณสร้างบรรทัดใบสั่งส่งคืนสินค้า คุณจะได้รับข้อความ</span><span class="sxs-lookup"><span data-stu-id="9e9db-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="9e9db-121">คุณไม่สามารถบล็อคชุดสินค้าหรือล็อตสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="9e9db-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="9e9db-122">ถ้าจะต้องบล็อคสินค้าบางส่วน คุณสามารถบล็อคได้ด้วยการย้ายสินค้าคงคลัง หรือบล็อคสินค้าคงคลังทั้งหมดของสินค้านั้นสำหรับรอบระยะเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="9e9db-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="9e9db-123">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="9e9db-123">Resolution</span></span>

- <span data-ttu-id="9e9db-124">เปิดหน้า **การตั้งค่าใบสั่งเริ่มต้น** ของสินค้า และล้างกล่องกาเครื่องหมาย **หยุด**</span><span class="sxs-lookup"><span data-stu-id="9e9db-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
