---
title: การค้นหาสินค้าคงคลังในการขายหน้าร้าน (POS)
description: หัวข้อนี้อธิบายถึงตัวเลือกที่พร้อมใช้งานสำหรับการดูข้อมูลสินค้าคงคลังในการขายหน้าร้าน (POS)
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 609f5f13f3af4a7621fe7ee152800dac4d68a9fc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025160"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="3c103-103">การค้นหาสินค้าคงคลังในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="3c103-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c103-104">การค้นหาสินค้าคงคลังในการขายหน้าร้าน (POS) ช่วยให้ผู้ค้าปลีกบรรลุความรู้ความสามารถในการดำเนินงานในเวลาจริง และได้รับความเข้าใจด้วยการเชื่อมต่อร้านค้า POS และฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="3c103-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="3c103-105">ฟังก์ชันนี้แสดงมุมมองในเวลาจริงอย่างถูกต้องของสินค้าคงคลังของผลิตภัณฑ์ระหว่างศูนย์กระจายสินค้าและร้านค้า</span><span class="sxs-lookup"><span data-stu-id="3c103-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="3c103-106">นอกจากนี้ ยังช่วยให้ผู้ค้าปลีกไดรฟ์ประสิทธิภาพเพิ่มเติม และการประหยัดต้นทุนโดยการปรับปรุงการวางแผนสินค้าคงคลังในเวลาจริง</span><span class="sxs-lookup"><span data-stu-id="3c103-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="3c103-107">มุมมองในเวลาจริงอย่างถูกต้องของสินค้าคงคลังทั่วทั้งองค์กร ช่วยให้สมาคมร้านค้าสามารถให้บริการลูกค้าที่ยอดเยี่ยมได้อย่างทันเวลา</span><span class="sxs-lookup"><span data-stu-id="3c103-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="3c103-108">เวลาที่มีผลมากที่สุดคือ เวลาที่ลูกค้าพร้อมที่จะทำการตัดสินใจซื้อ</span><span class="sxs-lookup"><span data-stu-id="3c103-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="3c103-109">สิ่งสำคัญคือว่า พนักงานเก็บเงินในร้านค้ามีข้อมูลสินค้าคงคลังแบบเรียลไทม์ที่เพียงปลายนิ้วสัมผัสของพวกเขา เพื่อให้พวกเขาสามารถสัญญาการจัดส่งผลิตภัณฑ์และการเบิกสินค้าได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3c103-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="3c103-110">คุณสามารถเปิดหน้า **การค้นหาสินค้าคงคลัง** ได้จากพื้นที่ทำงาน **Retail Modern POS** หรือพื้นที่ทำงาน **Retail Cloud POS**</span><span class="sxs-lookup"><span data-stu-id="3c103-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![ไทล์การค้นหาสินค้าคงคลังบนโฮมเพจ POS](media/POSHomepage.png)

<span data-ttu-id="3c103-112">ในหน้า **การค้นหาสินค้าคงคลัง** คุณสามารถใช้แป้นพิมพ์ตัวเลขเพื่อป้อนหมายเลขผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="3c103-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="3c103-113">จากนั้น คุณสามารถดูปริมาณคงเหลือสำหรับร้านค้าและคลังสินค้าที่หลากหลายได้</span><span class="sxs-lookup"><span data-stu-id="3c103-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![หน้าการค้นหาสินค้าคงคลังมาตรฐาน](media/InventoryLookUp.png)

<span data-ttu-id="3c103-115">ปริมาณ **จองไว้แล้ว** และ **สั่งแล้ว** ยังถูกแสดงสำหรับที่ตั้งแต่ละแห่งอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3c103-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="3c103-116">**จองไว้แล้ว** – ปริมาณนี้อ้างอิงถึงค่า **ที่จองจริง** จากฝ่ายสนับสนุนสำหรับหมายเลขผลิตภัณฑ์ที่ระบุในที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="3c103-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="3c103-117">**สั่งแล้ว** – ปริมาณนี้อ้างอิงถึงค่า **ผลรวมที่สั่ง** จากฝ่ายสนับสนุนสำหรับหมายเลขผลิตภัณฑ์ที่ระบุในที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="3c103-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="3c103-118">สถานที่ที่มีการแสดงข้อมูลความพร้อมใช้งานสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="3c103-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="3c103-119">รายการของสถานที่มีชนิดของเอนทิตี้สองชนิด:</span><span class="sxs-lookup"><span data-stu-id="3c103-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="3c103-120">**ร้านค้าปลีก** – รายการแสดงร้านค้าที่ถูกตั้งค่าคอนฟิก โดยใช้กลุ่มรหัสที่ตั้งร้านค้าสำหรับร้านค้าปัจจุบันในศูนย์ควบคุมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3c103-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span>
- <span data-ttu-id="3c103-121">**ศูนย์การกระจาย** – ชนิดต่างๆ ของศูนย์การกระจาย (เช่น คลังสินค้า) สามารถถูกตั้งค่าคอนฟิกได้ใน Retail</span><span class="sxs-lookup"><span data-stu-id="3c103-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Retail.</span></span> <span data-ttu-id="3c103-122">อย่างไรก็ตาม รายการจะแสดงข้อมูลความพร้อมใช้งานสินค้าคงคลังเท่านั้น สำหรับศูนย์กระจายสินค้าของชนิดเริ่มต้น **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="3c103-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3c103-123">ไม่มีการแสดงข้อมูลความพร้อมใช้งานสินค้าคงคลังสำหรับคลังสินค้าของชนิด **ส่งต่อ** **ตรวจสอบ** และ **สินค้าที่อยู่ระหว่างกระบวนการผลิต** สำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="3c103-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="3c103-124">ในหน้า **การค้นหาสินค้าคงคลัง** คุณสามารถดูปริมาณของปริมาณที่ให้สัญญาได้ (ATP) สำหรับแต่ละร้านค้า นอกเหนือจากปริมาณการคงเหลือปัจจุบัน ปริมาณที่จอง และปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="3c103-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="3c103-125">เลือกร้านค้าที่จะดูข้อมูล ATP สำหรับ และจากนั้น เลือก **แสดงความพร้อมใช้งานของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="3c103-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ปริมาณ ATP](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="3c103-127">การเปิดมิติที่ใช้มุมมองเมทริกซ์เพื่อแสดงผลิตภัณฑ์ย่อยทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3c103-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="3c103-128">ในหน้า **รายละเอียดผลิตภัณฑ์** ของผลิตภัณฑ์หลัก หรือในหน้า **การค้นหาสินค้าคงคลัง** เลือก **ดูผลิตภัณฑ์ย่อยทั้งหมด** จากแถบแอปที่ด้านล่างของหน้า</span><span class="sxs-lookup"><span data-stu-id="3c103-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="3c103-129">มุมมอง **เมทริกซ์ตามมิติ** สำหรับการเปิดใช้งานเริ่มต้นจากหน้าเหล่านี้ แสดงข้อมูลความพร้อมใช้งานสินค้าคงคลังสำหรับผลิตภัณฑ์ย่อยทั้งหมดของผลิตภัณฑ์สำหรับร้านค้าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3c103-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="3c103-130">ปุ่ม **ดูผลิตภัณฑ์ย่อยทั้งหมด** จะพร้อมใช้งานสำหรับสินค้าผลิตภัณฑ์หลักของสินค้าที่มีผลิตภัณฑ์ย่อยเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3c103-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="3c103-131">ไม่พร้อมใช้งานสำหรับผลิตภัณฑ์แบบสแตนด์อโลนหรือชุด</span><span class="sxs-lookup"><span data-stu-id="3c103-131">It isn't available for standalone products or kits.</span></span>

![ปุ่มดูผลิตภัณฑ์ย่อยทั้งหมดบนหน้าการค้นหาสินค้าคงคลัง](media/StandardToMatrix.png)

<span data-ttu-id="3c103-133">เลือก **ดูผลิตภัณฑ์ย่อยทั้งหมด** ในหน้า **รายละเอียดผลิตภัณฑ์** ของผลิตภัณฑ์หลัก หรือในหน้า **การค้นหาสินค้าคงคลัง** โดยไม่ต้องเลือกตำแหน่งที่ตั้ง เพื่อไปยังมุมมอง **เมทริกซ์ตามมิติ** เพื่อดูข้อมูลความพร้อมใช้งานของสินค้าคงคลังสำหรับผลิตภัณฑ์ย่อยทั้งหมดของผลิตภัณฑ์สำหรับร้านค้าปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3c103-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![มุมมองเมทริกซ์ตามมิติสำหรับหน้าการค้นหาสินค้าคงคลัง](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="3c103-135">ในภาพอธิบายก่อนหน้านี้ ลำดับการแสดงของมิติเป็นตัวอักษร เนื่องจากไม่ได้รับการตั้งค่าคอนฟิกลำดับการแสดงผลของมิติสำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c103-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="3c103-136">ในมุมมอง **เมทริกซ์ตามมิติ** เซลล์สำหรับผลิตภัณฑ์ย่อยรวมค่าคงเหลือในมุมขวาล่าง</span><span class="sxs-lookup"><span data-stu-id="3c103-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="3c103-137">ตารางต่อไปนี้อธิบายความหมายของค่าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="3c103-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="3c103-138">มูลค่าคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="3c103-138">On-hand value</span></span>                            | <span data-ttu-id="3c103-139">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3c103-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="3c103-140">ค่าตัวเลขที่มากกว่า 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="3c103-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="3c103-141">ตัวแปรได้ถูกนำออกใช้ไปยังที่ตั้งที่เลือก และคุณสามารถทำการดำเนินการเพิ่มเติมในเซลล์ได้</span><span class="sxs-lookup"><span data-stu-id="3c103-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="3c103-142">(การดำเนินการเหล่านี้จะถูกแจกแจงรายละเอียดในหัวข้อนี้ในภายหลัง)</span><span class="sxs-lookup"><span data-stu-id="3c103-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="3c103-143">**0** (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="3c103-143">**0** (zero)</span></span>                             | <span data-ttu-id="3c103-144">ตัวแปรได้ถูกนำออกใช้ไปยังที่ตั้งที่เลือก แต่รายการไม่พร้อมใช้งานในตำแหน่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c103-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="3c103-145">อย่างไรก็ตาม คุณสามารถทำการดำเนินการเพิ่มเติมในเซลล์ได้</span><span class="sxs-lookup"><span data-stu-id="3c103-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="3c103-146">(การดำเนินการเหล่านี้จะถูกแจกแจงรายละเอียดในหัวข้อนี้ในภายหลัง)</span><span class="sxs-lookup"><span data-stu-id="3c103-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="3c103-147">**n/a** หรือเซลล์ที่ไม่ได้ใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3c103-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="3c103-148">ตัวแปรไม่มีการออกใช้ไปยังที่ตั้งที่เลือก และคุณไม่สามารถทำการดำเนินการเพิ่มเติมในเซลล์ได้</span><span class="sxs-lookup"><span data-stu-id="3c103-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="3c103-149">คุณยังสามารถเปลี่ยนไพว็อทสำหรับมิติได้ โดยการเลือกมิติใหม่ที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="3c103-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![การเปลี่ยนแปลงไพว็อท](media/ChangePivot.png)

![ไพว็อทที่เปลี่ยน](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="3c103-152">ในภาพประกอบก่อนหน้านี้ ลำดับการแสดงผลของมิติสำหรับผลิตภัณฑ์ที่เลือกเป็นแบบกำหนดเอง (ไม่ใช่แบบอักษร)</span><span class="sxs-lookup"><span data-stu-id="3c103-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="3c103-153">ซึ่งยึดตามลำดับการแสดงมิติที่กำหนดไว้ในฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="3c103-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="3c103-154">นอกจากนี้ ในมุมมอง **เมทริกซ์ตามมิติ** สามารถทำการดำเนินการเพิ่มเติมเพื่อช่วยเพิ่มประสิทธิภาพการทำงานของการเชื่อมโยงของร้านค้าได้</span><span class="sxs-lookup"><span data-stu-id="3c103-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="3c103-155">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="3c103-155">Here are some examples:</span></span>

- <span data-ttu-id="3c103-156">เปลี่ยนที่ตั้งร้านค้าเพื่อค้นหาความพร้อมใช้งานสินค้าคงคลังของผลิตภัณฑ์ย่อยทั้งหมดที่สถานที่อื่น</span><span class="sxs-lookup"><span data-stu-id="3c103-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="3c103-157">ตำแหน่งที่ตั้งเหล่านี้ประกอบด้วยร้านค้าอื่นๆ ในกลุ่มรหัสที่ตั้งร้านค้าและศูนย์การกระจายสินค้าของชนิดเริ่มต้น **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="3c103-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="3c103-158">ขายผลิตภัณฑ์ย่อยแต่ละรายการให้แก่ลูกค้า โดยใช้เงินสดและการขนส่ง การเบิกสินค้าในร้านค้า หรือการจัดส่งไปยังที่อยู่</span><span class="sxs-lookup"><span data-stu-id="3c103-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="3c103-159">ให้ข้อมูล ATP แก่ลูกค้าสำหรับผลิตภัณฑ์ย่อยแต่ละรายการที่ที่ตั้งเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3c103-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![การดำเนินการเพิ่มเติมในไทล์ตัวแปร](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="3c103-161">ในภาพอธิบายก่อนหน้านี้ ลำดับการแสดงของมิติเป็นตัวอักษร เนื่องจากไม่ได้รับการตั้งค่าคอนฟิกลำดับการแสดงผลของมิติสำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c103-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="3c103-162">ตารางต่อไปนี้แสดงข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการเพิ่มเติมที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3c103-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="3c103-163">การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="3c103-163">Action</span></span>               | <span data-ttu-id="3c103-164">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3c103-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="3c103-165">ขายตอนนี้</span><span class="sxs-lookup"><span data-stu-id="3c103-165">Sell now</span></span>             | <span data-ttu-id="3c103-166">เพิ่มตัวแปรสินค้าที่เลือกในธุรกรรม และเปลี่ยนเส้นทางผู้ใช้ไปยังหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3c103-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="3c103-167">(การดำเนินการนี้ไม่พร้อมใช้งาน เมื่อที่ตั้งที่เลือกเป็นศูนย์กระจายสินค้า)</span><span class="sxs-lookup"><span data-stu-id="3c103-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="3c103-168">เบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="3c103-168">Pick up in store</span></span>     | <span data-ttu-id="3c103-169">สร้างใบสั่งของลูกค้าสำหรับผลิตภัณฑ์ย่อยที่จะเลือกค่าจากที่ตั้งที่เลือก และเปลี่ยนเส้นทางผู้ใช้ไปยังหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3c103-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="3c103-170">(การดำเนินการนี้ไม่พร้อมใช้งาน เมื่อที่ตั้งที่เลือกเป็นศูนย์กระจายสินค้า)</span><span class="sxs-lookup"><span data-stu-id="3c103-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="3c103-171">จัดส่งผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3c103-171">Ship product</span></span>         | <span data-ttu-id="3c103-172">สร้างใบสั่งของลูกค้าสำหรับผลิตภัณฑ์ย่อยที่จะถูกจัดส่งค่าจากที่ตั้งที่เลือก และเปลี่ยนเส้นทางผู้ใช้ไปยังหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3c103-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="3c103-173">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3c103-173">Availability</span></span>         | <span data-ttu-id="3c103-174">แสดงข้อมูล ATP สำหรับชุดข้อมูลตัวแปรที่เลือกสำหรับที่ตั้งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3c103-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="3c103-175">แสดงทุกที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="3c103-175">Show all locations</span></span>   | <span data-ttu-id="3c103-176">สลับไปยังมุมมองการค้นหาสินค้าคงคลังมาตรฐาน และเน้นข้อมูลความพร้อมใช้งานสินค้าคงคลังสำหรับตัวแปรสินค้าสำหรับร้านค้าทั้งหมดในกลุ่มรหัสที่ตั้งร้านค้า และในศูนย์กระจายสินค้าของชนิด **มาตรฐาน/เริ่มต้น** ด้วย</span><span class="sxs-lookup"><span data-stu-id="3c103-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="3c103-177">ดูรายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3c103-177">View product details</span></span> | <span data-ttu-id="3c103-178">เปลี่ยนเส้นทางผู้ใช้ไปยังหน้า **รายละเอียดผลิตภัณฑ์** ของข้อมูลหลักของผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3c103-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
