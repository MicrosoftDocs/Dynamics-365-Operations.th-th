---
title: รหัสผู้จัดจำหน่ายไม่ได้รับอนุญาตให้ระบุผลิตภัณฑ์และวันที่
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง หรือเพิ่มรายการลงในใบสั่งซื้อ คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่ารหัสผู้จัดจำหน่ายไม่ได้รับอนุมัติสำหรับผลิตภัณฑ์และวันที่
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294194"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="900ac-103">รหัสผู้จัดจำหน่ายไม่ได้รับอนุญาตให้ระบุผลิตภัณฑ์และวันที่</span><span class="sxs-lookup"><span data-stu-id="900ac-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="900ac-104">รหัสข้อผิดพลาด: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="900ac-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="900ac-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="900ac-105">Symptoms</span></span>

<span data-ttu-id="900ac-106">เมื่อคุณพยายามยืนยันแผนการใบสั่งหรือเพิ่มรายการลงในใบสั่งซื้อ คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="900ac-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="900ac-107">รหัสผู้จัดจำหน่าย %1 ไม่ได้รับอนุมัติสำหรับ %2 ใน %3</span><span class="sxs-lookup"><span data-stu-id="900ac-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="900ac-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="900ac-108">Cause</span></span>

<span data-ttu-id="900ac-109">มีข้อผิดพลาดเกิดขึ้นเนื่องจากฟิลด์ **วิธีการตรวจสอบผู้จัดให้บริการที่ได้รับอนุมัติ** ได้รับการตั้งค่าเป็น *คําเตือนอย่างเดียว* หรือ *ไม่ได้รับอนุญาต* สำหรับผลิตภัณฑ์ที่ระบุ และไม่ได้รับอนุมัติให้จัดหาผลิตภัณฑ์นั้นในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="900ac-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="900ac-110">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="900ac-110">Resolution</span></span>

<span data-ttu-id="900ac-111">เมื่อต้องการแก้ไขปัญหานี้ ให้ปิดใช้งานการตรวจสอบผู้จัดจำหน่ายสำหรับผลิตภัณฑ์ที่เกี่ยวข้องหรืออนุมัติผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="900ac-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="900ac-112">หากต้องการปิดใช้งานการตรวจสอบผู้จัดจำหน่ายสำหรับผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="900ac-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="900ac-113">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="900ac-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="900ac-114">เปิดผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="900ac-114">Open the relevant product.</span></span>
1. <span data-ttu-id="900ac-115">บนแท็บด่วน **การซื้อ** ให้ตั้งค่าฟิลด์ **วิธีตรวจสอบผู้จัดจำหน่ายที่ได้รับอนุมัติ** เป็นค่าอื่นๆ ที่ไม่ใช่ *คําเตือนเท่านั้น* หรือ *ไม่อนุญาต*</span><span class="sxs-lookup"><span data-stu-id="900ac-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="900ac-116">หากต้องการอนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="900ac-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="900ac-117">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="900ac-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="900ac-118">เปิดสินค้าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="900ac-118">Open the relevant item.</span></span>
1. <span data-ttu-id="900ac-119">บน บานหน้าต่างการดำเนินการบนแท็บ **ซื้อ** ในกลุ่ม **ผู้จัดจำหน่ายอนุมัติแล้ว** ให้เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="900ac-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="900ac-120">ในหน้ารายการ **ผู้จัดจำหน่ายที่ได้รับอนุมัติ** เพิ่มแถวไปยังกริด และจากนั้นตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="900ac-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="900ac-121">**ผู้จัดจำหน่าย** – เลือกผู้จัดจำหน่ายที่จะอนุมัติสำหรับผลิตภัณฑ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="900ac-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="900ac-122">**วันที่มีผลบังคับใช้** – เลือกวันที่แรกที่อนุมัติผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="900ac-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="900ac-123">**วันหมดอายุ** – เลือกวันสุดท้ายที่อนุมัติผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="900ac-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="900ac-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [อนุมัติผู้จัดจำหน่ายสำหรับผลิตภัณฑ์เฉพาะ](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md)</span><span class="sxs-lookup"><span data-stu-id="900ac-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
