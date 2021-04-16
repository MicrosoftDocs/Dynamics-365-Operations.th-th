---
title: ตั้งค่าคอนฟิกแสดงเฉพาะชุดงานภายในคลังสินค้าบนอุปกรณ์เคลื่อนที่
description: หัวข้อนี้อธิบายวิธีการตั้งค่าอุปกรณ์เคลื่อนที่เพื่อแสดงรายการของที่ตั้งที่มีชุดงานที่เก่ากว่าที่ตั้งปัจจุบันของรายการงาน
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5156b17b9eddc2c3127b6d91fd8cd7d519d240e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838309"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="8388a-103">ตั้งค่าคอนฟิกแสดงเฉพาะชุดงานภายในคลังสินค้าบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="8388a-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8388a-104">การตั้งค่าคอนฟิก **แสดงเฉพาะชุดงานภายในคลังสินค้า** ช่วยให้คุณสามารถแสดงรายการของที่ตั้งที่มีชุดงานที่เก่ากว่าที่ตั้งปัจจุบันของรายการงาน</span><span class="sxs-lookup"><span data-stu-id="8388a-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="8388a-105">รายการของสถานที่เก็บที่จะแสดงขึ้นรวมถึงข้อมูลเกี่ยวกับชุดงานที่เก่ากว่าในสถานที่เก็บนั้น ๆ ที่มีวันหมดอายุและสินค้าคงคลังทางกายภาพของแต่ละชุดงาน</span><span class="sxs-lookup"><span data-stu-id="8388a-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="8388a-106">คุณสามารถเลือกที่จะเบิกสินค้าจากสถานที่เก็บใหม่หรือเบิกสินค้าจากสถานที่เก็บปัจจุบันต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="8388a-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="8388a-107">เบิกสินค้าจากสถานที่เก็บใหม่ - ถ้าคุณเลือกที่จะเบิกสินค้าจากสถานที่เก็บใหม่ รายการงานปัจจุบันจะถูกอัพเดตเพื่อใช้สถานที่เก็บใหม่และงานจะดำเนินต่อไปตามปกติกับสถานที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="8388a-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="8388a-108">เพื่อให้สถานที่เก็บใหม่ใช้ได้ จะต้องมีปริมาณที่พร้อมใช้งานที่เพียงพอสำหรับรายการงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8388a-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="8388a-109">ถ้าไม่มีปริมาณที่กำหนด รายการงานจะไม่ถูกอัพเดตและรายการจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="8388a-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="8388a-110">ทำการเบิกสินค้าจากสถานที่เก็บปัจจุบัน - ถ้าคุณดำเนินการต่อกับสถานที่เก็บรายการงานปัจจุบัน ปริมาณสำหรับรายการงานจะดำเนินการเบิกสินค้าจากสถานที่เก็บเดิมต่อไป</span><span class="sxs-lookup"><span data-stu-id="8388a-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="8388a-111">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="8388a-111">Where it applies</span></span>
<span data-ttu-id="8388a-112">แสดงชุดงานที่เก่ากว่าภายในคลังสินค้า ถูกตั้งค่าคอนฟิกบนรายการเมนูของอุปกรณ์เคลื่อนที่ และส่งผลต่อการเลือกชุดงานด้านล่างรายการ</span><span class="sxs-lookup"><span data-stu-id="8388a-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="8388a-113">ตั้งค่า แสดงผลชุดงานที่เก่ากว่าภายในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="8388a-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="8388a-114">การตั้งค่าคอนฟิก **แสดงชุดงานที่เก่ากว่าภายในคลังสินค้า** จะพร้อมใช้งานบนรายการเมนูอุปกรณ์เคลื่อนที่เมื่อตัวเลือก **เลือกชุดงานที่เก่าที่สุด** ถูกตั้งค่าเป็น **เตือน**</span><span class="sxs-lookup"><span data-stu-id="8388a-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="8388a-115">ภายใต้ **การบริหารคลังสินค้า** > **การตั้งค่า** > **อุปกรณ์เคลื่อนที่** > **รายการเมนูบนอุปกรณ์เคลื่อนที่** ตั้งค่า **ใช้งานที่มีอยู่** เป็น **ใช่** สำหรับรายการเมนู และเลือก **เตือน** ในฟิลด์ **เลือกชุดงานที่เก่าที่สุด**</span><span class="sxs-lookup"><span data-stu-id="8388a-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]