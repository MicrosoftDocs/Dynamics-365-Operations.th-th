---
title: การสุ่มตัวอย่างสินค้าในการจัดการคุณภาพ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการสุ่มตัวอย่างสินค้า
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956842"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="dcb2a-103">การสุ่มตัวอย่างสินค้าในการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="dcb2a-103">Quality management item sampling</span></span>

<span data-ttu-id="dcb2a-104">การสุ่มตัวอย่างสินค้าใช้เป็นส่วนหนึ่งของการเชื่อมโยงคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="dcb2a-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="dcb2a-105">โดยจะกําหนดจํานวนของสินค้าคงคลังทางกายภาพในปัจจุบันที่ต้องตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="dcb2a-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="dcb2a-106">การสุ่มตัวอย่างอาจขึ้นอยู่กับปริมาณคงที่ เปอร์เซ็นต์ หรือป้ายทะเบียนแบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="dcb2a-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="dcb2a-107">ตั้งค่าการสุ่มตัวอย่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="dcb2a-107">Set up item sampling</span></span>

<span data-ttu-id="dcb2a-108">ให้ดำเนินการตามขั้นตอนต่อไปนี้เพื่อตั้งค่าการสุ่มตัวอย่างสินค้า</span><span class="sxs-lookup"><span data-stu-id="dcb2a-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="dcb2a-109">ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> การสุ่มตัวอย่างสินค้า**</span><span class="sxs-lookup"><span data-stu-id="dcb2a-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="dcb2a-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="dcb2a-110">Select **New**.</span></span>
1. <span data-ttu-id="dcb2a-111">ในฟิลด์ **การสุ่มตัวอย่างสินค้า** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="dcb2a-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="dcb2a-112">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="dcb2a-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="dcb2a-113">ในฟิลด์ **ค่า** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="dcb2a-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="dcb2a-114">ค่านี้เกี่ยวข้องกับข้อมูลจำเพาะเกี่ยวกับปริมาณที่ถูกเลือกในฟิลด์ที่อยู่ติดกัน</span><span class="sxs-lookup"><span data-stu-id="dcb2a-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="dcb2a-115">ในส่วน **กระบวนการ** ให้เลือกกล่องกาเครื่องหมาย **การบล็อคทั้งหมด** ถ้าปริมาณล็อตหรือปริมาณของรายการใบสั่งทั้งหมดควรถูกบล็อคถ้าการทดสอบล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="dcb2a-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="dcb2a-116">ถ้าไม่เลือกกล่องกาเครื่องหมายนี้ เฉพาะสินค้าในใบสั่งตรวจสอบคุณภาพเท่านั้นจะถูกบล็อคถ้าการทดสอบล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="dcb2a-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="dcb2a-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dcb2a-117">Select **Save**.</span></span>
1. <span data-ttu-id="dcb2a-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dcb2a-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="dcb2a-119">คุณลักษณะ *การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า* มีความสามารถในการสุ่มตัวอย่างสินค้าเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dcb2a-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="dcb2a-120">ซึ่งเพิ่มแนวคิดของ *ขอบเขตการสุ่มตัวอย่างสินค้า* และให้คุณกำหนดป้ายทะเบียนแบบเต็มเป็นข้อมูลจำเพาะของปริมาณได้</span><span class="sxs-lookup"><span data-stu-id="dcb2a-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="dcb2a-121">ถ้าคุณได้เปิดใช้งานคุณลักษณะนี้ ให้ดูที่ [การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า](quality-management-for-warehouses-processes.md)</span><span class="sxs-lookup"><span data-stu-id="dcb2a-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
