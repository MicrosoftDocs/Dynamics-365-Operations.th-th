---
title: ตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่เพื่อแสดงภาพรวมของบรรทัดการเบิกสินค้า
description: หัวข้อนี้จะอธิบายถึงวิธีการกำหนดเวลาที่รายการของบรรทัดงานทั้งหมดจะแสดงให้เห็นถึงผู้ปฏิบัติงานในคลังสินค้าที่กำลังประมวลผลการทำงานของคลังสินค้าบนอุปกรณ์เคลื่อนที่ ความสามารถนี้อาจเป็นประโยชน์สำหรับผู้ปฏิบัติงานคลังสินค้า ซึ่งมักจะต้องมีภาพรวมของบรรทัดการเบิกสินค้าในใบสั่งงานเพื่อให้สามารถเพิ่มประสิทธิภาพของลำดับการเบิกสินค้าได้
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818883"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="96b68-104">ตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่เพื่อแสดงภาพรวมของบรรทัดการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96b68-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96b68-105">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกตัวเลือกที่เกี่ยวข้องกับภาพรวมของบรรทัดการเบิกสินค้าสำหรับรายการเมนูของอุปกรณ์เคลื่อนที่ที่ใช้ในการประมวลผลงานการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96b68-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="96b68-106">ภาพรวมของบรรทัดการเบิกสินค้าให้ดูรายละเอียดของผู้ปฏิบัติงานคลังสินค้าและเลือกจากรายการของบรรทัดงานทั้งหมดที่เกี่ยวข้องกับงานปัจจุบันของตน</span><span class="sxs-lookup"><span data-stu-id="96b68-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="96b68-107">ความสามารถนี้สามารถช่วยให้ผู้ปฏิบัติงานสามารถเพิ่มประสิทธิภาพของลำดับการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96b68-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="96b68-108">ลักษณะการทำงานนี้จะมีตัวเลือกที่แทนที่ปุ่ม **ข้าม** มาตรฐานที่จะให้ผู้ปฏิบัติงานวนรอบไปยังบรรทัดทีละบรรทัดในใบสั่งแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="96b68-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="96b68-109">(อย่างไรก็ตามตัวเลือกที่จะใช้ปุ่มดังกล่าวยังคงมีอยู่)</span><span class="sxs-lookup"><span data-stu-id="96b68-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="96b68-110">ผู้ดูแลระบบสามารถตั้งค่าคอนฟิกแต่ละรายการเมนูทีละรายการเพื่อควบคุมวิธีการ เวลา และที่ที่แอปการจัดการคลังสินค้าบนมือถือจะแสดงภาพรวมของบรรทัดการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96b68-110">Admins can configure each menu item individually to control how, when, and where the Warehouse Management mobile app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="96b68-111">เปิดคุณลักษณะภาพรวมรายการเลือกงาน</span><span class="sxs-lookup"><span data-stu-id="96b68-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="96b68-112">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="96b68-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="96b68-113">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="96b68-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="96b68-114">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="96b68-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="96b68-115">**โมดูล:** _การจัดการคลังสินค้า_</span><span class="sxs-lookup"><span data-stu-id="96b68-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="96b68-116">**ชื่อคุณลักษณะ:** _ภาพรวมรายการเลือกงาน_</span><span class="sxs-lookup"><span data-stu-id="96b68-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="96b68-117">ตั้งค่าคอนฟิกรายการเมนูเพื่อแสดงรายการของรายการงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="96b68-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="96b68-118">หากต้องการตั้งค่ารายการเมนูของอุปกรณ์เคลื่อนที่เพื่อแสดงภาพรวมของบรรทัดการเบิกสินค้า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="96b68-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="96b68-119">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="96b68-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="96b68-120">เลือกหรือสร้างรายการเมนูที่เกี่ยวข้องกับงานการเบิกสินค้าและตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="96b68-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="96b68-121">**โหมด:** *งาน*</span><span class="sxs-lookup"><span data-stu-id="96b68-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="96b68-122">**ใช้งานที่มีอยู่:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="96b68-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="96b68-123">**กำกับโดย:** *สั่งการโดยผู้ใช้* หรือ *สั่งการโดยระบบ*</span><span class="sxs-lookup"><span data-stu-id="96b68-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="96b68-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างรายการเมนูและใช้การตั้งค่าต่างๆ ที่มีอยู่ในหน้า **รายการเมนูของอุปกรณ์เคลื่อนที่** ให้ดูที่ [การตั้งค่าอุปกรณ์เคลื่อนที่สำหรับการทำงานของคลังสินค้า](configure-mobile-devices-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="96b68-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="96b68-125">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าคอนฟิกลักษณะการทำงานโดยการตั้งค่าฟิลด์ **แสดงรายการรายการงาน** ให้เป็นค่าใดค่าหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="96b68-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="96b68-126">**แสดงเฉพาะเมื่อมีการร้องขอ** – ผู้ปฏิบัติงานเท่านั้นที่สามารถเลือกที่จะดูรายการบรรทัดการเบิกสินค้าได้โดยการเลือกปุ่ม **ข้ามไปยัง** ในแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="96b68-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="96b68-127">**แสดงที่จุดเริ่มต้นของการเบิกสินค้าทั้งหมด** – ผู้ปฏิบัติงานดูรายการทุกครั้งที่เริ่มต้นหรือสิ้นสุดบรรทัดการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="96b68-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="96b68-128">นอกจากนี้ยังสามารถดูรายการอีกครั้งได้ด้วยการเลือกปุ่ม **ข้ามไปยัง** ในแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="96b68-128">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="96b68-129">**แสดงที่จุดเริ่มต้นของการเบิกสินค้าครั้งแรกเท่านั้น** – ผู้ปฏิบัติงานดูรายการทุกครั้งที่เริ่มต้นงานการเบิกสินค้าใหม่ แต่ไม่ใช่หลังจากแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="96b68-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="96b68-130">นอกจากนี้ยังสามารถดูรายการอีกครั้งได้ด้วยการเลือกปุ่ม **ข้ามไปยัง** ในแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="96b68-130">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="96b68-131">**ไม่ต้องแสดง** – ปุ่ม **ข้าม** มาตรฐาน จะปรากฏขึ้นในแอปการจัดการคลังสินค้าบนมือถือและการแสดงรายการของรายการงานจะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="96b68-131">**Never show** – The standard **Skip** button appears in the Warehouse Management mobile app, and display of the work line list is turned off.</span></span> <span data-ttu-id="96b68-132">ปุ่ม **ข้าม** ช่วยให้ผู้ปฏิบัติงานมีวงจรผ่านบรรทัดทีละบรรทัดในใบสั่งแบบคงที่</span><span class="sxs-lookup"><span data-stu-id="96b68-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="96b68-133">นอกจากนี้ยังสามารถวนผ่านรายการได้หลายครั้งตามต้องการจนกว่าจะมีการประมวลผลรายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="96b68-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="96b68-134">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="96b68-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="96b68-135">ถ้าคุณตั้งค่าฟิลด์ **แสดงรายการของรายการงาน** ให้เป็นค่าใดๆ ยกเว้น *ไม่แสดง* ปุ่ม **รายการของฟิลด์** บนบานหน้าต่างการดำเนินการจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="96b68-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="96b68-136">ในบานหน้าต่างการดำเนินการ เลือก **รายการฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="96b68-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="96b68-137">บนหน้า **รายการฟิลด์** ให้ตั้งค่าคอนฟิกข้อมูลที่แอปการจัดการคลังสินค้าบนมือถือแสดงสำหรับแต่ละบรรทัดในรายการ</span><span class="sxs-lookup"><span data-stu-id="96b68-137">On the **Field list** page, configure the information that the Warehouse Management mobile app shows for each line in the list.</span></span>

    - <span data-ttu-id="96b68-138">ฟิลด์ **ตัวควบคุมหลัก** จะถูกตั้งค่าเป็น *LineNum* เสมอ</span><span class="sxs-lookup"><span data-stu-id="96b68-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="96b68-139">ดังนั้นแต่ละแถวในรายการจะเริ่มต้นด้วยหมายเลขบรรทัด</span><span class="sxs-lookup"><span data-stu-id="96b68-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="96b68-140">ใช้ฟิลด์ **ฟิลด์แสดงผล** ที่มีอยู่เพื่อเพิ่มฟิลด์แสดงผลเพิ่มเติมเจ็ดฟิลด์ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="96b68-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="96b68-141">ในฟิลด์แต่ละ **ฟิลด์แสดง** ให้เลือกชื่อของฟิลด์บรรทัดงาน</span><span class="sxs-lookup"><span data-stu-id="96b68-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="96b68-142">แต่ละบรรทัดจะแสดงค่าสำหรับฟิลด์นั้น</span><span class="sxs-lookup"><span data-stu-id="96b68-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="96b68-143">ค่านี้จะแสดงตามลำดับที่คุณเลือกไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="96b68-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="96b68-144">คุณสามารถปล่อยฟิลด์ **ฟิลด์แสดง** บางฟิลด์ให้ว่างเปล่าได้ถ้าคุณไม่ต้องการค่าทั้งหมดเจ็ดค่า</span><span class="sxs-lookup"><span data-stu-id="96b68-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="96b68-145">ในบานหน้าต่างการดำเนินการให้เลือก **บันทึก** จากนั้นปิดหน้า **รายการฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="96b68-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]