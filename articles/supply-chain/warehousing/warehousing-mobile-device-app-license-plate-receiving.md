---
title: ป้ายทะเบียนที่ได้รับผ่านทางแอปคลังสินค้า
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าแอปคลังสินค้า เพื่อสนับสนุนการใช้กระบวนการรับป้ายทะเบียนเพื่อรับสินค้าคงคลังที่มีอยู่จริง
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346387"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="26e8c-103">ป้ายทะเบียนที่ได้รับผ่านทางแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="26e8c-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="26e8c-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าแอปคลังสินค้า เพื่อให้สนับสนุนการใช้กระบวนการรับป้ายทะเบียนเพื่อรับสินค้าคงคลังที่มีอยู่จริง</span><span class="sxs-lookup"><span data-stu-id="26e8c-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="26e8c-105">คุณสามารถใช้ฟังก์ชันนี้เพื่อบันทึกการรับสินค้าคงคลังขาเข้าที่เกี่ยวข้องกับใบแจ้งเตือนการจัดส่งล่วงหน้า (ASN) อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="26e8c-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="26e8c-106">ระบบจะสร้าง ASN โดยอัตโนมัติ เมื่อมีการใช้กระบวนการจัดการคลังสินค้าเพื่อจัดส่งใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="26e8c-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="26e8c-107">สำหรับกระบวนการใบสั่งซื้อ ASN สามารถถูกบันทึกด้วยตนเอง หรือสามารถถูกนำเข้าได้โดยอัตโนมัติโดยใช้กระบวนการเอนทิตี้ข้อมูล ASN ขาเข้า</span><span class="sxs-lookup"><span data-stu-id="26e8c-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="26e8c-108">ข้อมูล ASN ถูกเชื่อมโยงกับการโหลดและการจัดส่งผ่านทาง *โครงสร้างการบรรจุ* ที่ซึ่งแท่นวางสินค้า (ป้ายทะเบียนหลัก) สามารถมีกรอบได้ (แผ่นป้ายทะเบียนที่ซ้อนกัน)</span><span class="sxs-lookup"><span data-stu-id="26e8c-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="26e8c-109">เมื่อต้องการลดจำนวนของรายการความเคลื่อนไหวของสินค้าคงคลัง เมื่อมีการใช้โครงสร้างการจัดส่งที่มีการใช้ป้ายทะเบียนที่ซ้อนกัน ระบบจะบันทึกปริมาณคงคลังคงเหลือที่มีอยู่จริงบนป้ายทะเบียนหลัก</span><span class="sxs-lookup"><span data-stu-id="26e8c-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="26e8c-110">เมื่อต้องการทริกเกอร์การเคลื่อนไหวของปริมาณคงคลังคงเหลือที่มีอยู่จริงจากป้ายทะเบียนหลักไปยังป้ายทะเบียนที่ซ้อนกัน โดยยึดตามข้อมูลโครงสร้างการบรรจุ อุปกรณ์เคลื่อนที่ต้องมีรายการเมนูที่ยึดตามกระบวนการสร้างงาน *บรรจุไปยังป้ายทะเบียนที่ซ้อนกัน*</span><span class="sxs-lookup"><span data-stu-id="26e8c-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="26e8c-111">แสดงหรือข้ามหน้าสรุปการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="26e8c-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="26e8c-112">คุณสามารถใช้คุณลักษณะ *ควบคุมว่าจะแสดงหน้าสรุปการรับสินค้าบนอุปกรณ์เคลื่อนที่* เพื่อใช้ประโยชน์จากขั้นตอนของแอปคลังสินค้าโดยละเอียดเพิ่มเติม โดยเป็นส่วนหนึ่งของกระบวนการรับป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="26e8c-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="26e8c-113">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="26e8c-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="26e8c-114">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26e8c-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="26e8c-115">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26e8c-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="26e8c-116">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="26e8c-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="26e8c-117">**ชื่อคุณลักษณะ:** *ควบคุมว่าจะแสดงหน้าสรุปการรับสินค้าบนอุปกรณ์เคลื่อนที่หรือไม่*</span><span class="sxs-lookup"><span data-stu-id="26e8c-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="26e8c-118">เมื่อเปิดใช้งานคุณลักษณะนี้ รายการเมนูบนอุปกรณ์เคลื่อนที่สำหรับการรับป้ายทะเบียน หรือการรับป้ายทะเบียนการรับสินค้าและการย้ายเก็บจะให้การตั้งค่า **หน้าแสดงการสรุปการรับสินค้า**</span><span class="sxs-lookup"><span data-stu-id="26e8c-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="26e8c-119">การตั้งค่านี้มีตัวเลือกดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26e8c-119">This setting has the following options:</span></span>

- <span data-ttu-id="26e8c-120">**แสดงสรุปโดยละเอียด** – ในระหว่างการรับป้ายทะเบียน ผู้ปฏิบัติงานจะเห็นหน้าพิเศษที่แสดงข้อมูล ASN แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="26e8c-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="26e8c-121">**ข้ามสรุป** – ผู้ปฏิบัติงานจะไม่เห็นข้อมูล ASN แบบเต็ม</span><span class="sxs-lookup"><span data-stu-id="26e8c-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="26e8c-122">นอกจากนี้ ผู้ปฏิบัติงานคลังสินค้าจะยังไม่สามารถตั้งค่ารหัสการโอนการครอบครอง หรือเพิ่มข้อยกเว้น ในระหว่างกระบวนการรับสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="26e8c-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="26e8c-123">ป้องกันใบสั่งโอนย้าย ป้ายทะเบียนที่ส่ง ไม่ให้ถูกใช้ที่คลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="26e8c-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="26e8c-124">ไม่สามารถใช้กระบวนการรับป้ายทะเบียนได้ ถ้า ASN มีรหัสป้ายทะเบียนอยู่แล้ว และมีข้อมูลปริมาณคงเหลือที่มีอยู่จริงที่สถานที่คลังสินค้าอื่นที่ไม่ใช่สถานที่คลังสินค้าที่มีการลงทะเบียนป้ายทะเบียนเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="26e8c-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="26e8c-125">สำหรับสถานการณ์ใบสั่งโอนย้ายที่ซึ่งคลังสินค้าส่งต่อไม่ได้ติดตามป้ายทะเบียน (และดังนั้น จึงไม่สามารถติดตามปริมาณคงคลังคงเหลือที่มีอยู่จริงสำหรับป้ายทะเบียนแต่ละแผ่น) คุณสามารถใช้คุณลักษณะ *ป้องกันใบสั่งโอนย้ายที่จัดส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นๆ นอกเหนือจากคลังสินค้าปลายทาง* เพื่อป้องกันการอัปเดตปริมาณคงคลังคงเหลือของป้ายทะเบียนที่อยู่ระหว่างการส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="26e8c-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="26e8c-126">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="26e8c-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="26e8c-127">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26e8c-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="26e8c-128">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะนี้ในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26e8c-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="26e8c-129">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="26e8c-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="26e8c-130">**ชื่อคุณลักษณะ:** *ป้องกันใบสั่งโอนย้ายที่ส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง*</span><span class="sxs-lookup"><span data-stu-id="26e8c-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="26e8c-131">เมื่อต้องการจัดการฟังก์ชันเมื่อคุณลักษณะนี้พร้อมใช้งาน ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="26e8c-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="26e8c-132">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="26e8c-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="26e8c-133">บนแท็บ **ทั่วไป** บน FastTab **ป้ายทะเบียน** ให้ตั้งค่าฟิลด์ **นโยบายส่งต่อป้ายทะเบียนของคลังสินค้า** เป็นค่าใดค่าหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="26e8c-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="26e8c-134">**อนุญาตให้ใช้ป้ายทะเบียนที่ไม่มีการติดตามอีกครั้ง** – ระบบทำงานในลักษณะเดียวกันกับทำงานเมื่อคุณลักษณะ *ป้องกันใบสั่งโอนย้ายที่จัดส่งป้ายทะเบียนไม่ให้ถูกใช้ในคลังสินค้าอื่นที่ไม่ใช่คลังสินค้าปลายทาง* ไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="26e8c-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="26e8c-135">ค่านี้เป็นการตั้งค่าเริ่มต้น เมื่อคุณเรียกใช้งานคุณลักษณะเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="26e8c-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="26e8c-136">**ป้องกันไม่ให้มีการนำป้ายทะเบียนที่ไม่มีการติดตามไปใช้ซ้ำ** – เฉพาะการอัปเดตปริมาณคงเหลือที่เกี่ยวข้องกับป้ายทะเบียนที่จัดส่งเท่านั้นที่จะได้รับอนุญาตที่คลังสินค้าปลายทาง จนกว่าจะได้รับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="26e8c-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="26e8c-137">ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="26e8c-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="26e8c-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายการเมนูบนอุปกรณ์เคลื่อนที่ ให้ดูที่ [ตั้งค่าอุปกรณ์เคลื่อนที่สำหรับงานของคลังสินค้า](configure-mobile-devices-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="26e8c-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
