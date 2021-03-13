---
title: สร้างสินทรัพย์ตามใบสั่งซื้อ
description: หัวข้อนี้อธิบายวิธีที่คุณสามารถสร้างรายการของรายการสินทรัพย์ที่สามารถใช้เป็นพื้นฐานสำหรับการสร้างสินทรัพย์สำหรับงานบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016995"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="ccf5b-103">สร้างสินทรัพย์ตามใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ccf5b-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถสร้างรายการของรายการสินทรัพย์ที่สามารถใช้เป็นพื้นฐานสำหรับการสร้างสินทรัพย์สำหรับงานบำรุงรักษาในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="ccf5b-105">โดยขึ้นอยู่กับรายการสินทรัพย์ คุณสามารถดูรายการของรายการใบสั่งซื้อที่ถูกสร้างขึ้นในรายการเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="ccf5b-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="ccf5b-106">วัตถุประสงค์ของฟังก์ชันการทำงานนี้คือ เพื่อให้สามารถสร้างสินทรัพย์ในการจัดการสินทรัพย์ตามใบสั่งซื้อได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="ccf5b-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="ccf5b-107">ขั้นแรก ให้คุณตั้งค่าสินค้าที่จะใช้สำหรับการสร้างสินทรัพย์จากใบสั่งซื้อใน **รายการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="ccf5b-108">หลังจากสร้างรายการใบสั่งซื้อแล้ว คุณจะสร้างสินทรัพย์ใน **สินทรัพย์ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="ccf5b-109">สามารถตัดสินใจได้ว่าขั้นตอนใดของใบสั่งซื้อที่ควรจะสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="ccf5b-110">เลือกรายการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-110">Select asset items</span></span>

1. <span data-ttu-id="ccf5b-111">คลิก **การจัดการสินทรัพย์** > **การตั้งค่า** > **สินทรัพย์** > **รายการ**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="ccf5b-112">คลิก **สร้าง** เพื่อสร้างรายการสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="ccf5b-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="ccf5b-113">เลือกสินค้าในฟิลด์ **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="ccf5b-114">เมื่อคุณออกจากฟิลด์นั้น ชื่อสินค้าจะถูกแทรกลงในฟิลด์ **ชื่อผลิตภัณฑ์** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="ccf5b-115">บน FastTab **ทั่วไป** ให้เลือกชนิดสินทรัพย์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccf5b-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="ccf5b-116">เลือกผู้ผลิตและรุ่นของสินทรัพย์สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccf5b-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="ccf5b-117">บันทึกรายการ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="ccf5b-118">สร้างสินทรัพย์จากสินทรัพย์ที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="ccf5b-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="ccf5b-119">คลิก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="ccf5b-120">คุณจะเห็นรายการที่ปรับปรุงแล้วของใบสั่งซื้อตามสินค้าที่เลือกใน **รายการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="ccf5b-121">คุณสามารถกรองสถานะของใบสั่งซื้อเพื่อเลือกสถานะของวงจรการใช้ที่ควรมีการสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="ccf5b-122">ตัวอย่างเช่น คุณอาจต้องการสร้างสินทรัพย์ เมื่อมีการลงรายการบัญชีใบรับสินค้าในใบสั่งซื้อเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ccf5b-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="ccf5b-123">เลือกลิงค์ **หมายเลขอ้างอิง** บนรายการใบสั่งซื้อ เพื่อดูข้อมูลโดยละเอียดเกี่ยวกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="ccf5b-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="ccf5b-124">ถ้าคุณต้องการแก้ไขมิติที่จะแสดงขึ้นบน FastTab **มิติสินค้าคงคลัง** ให้คลิกปุ่ม **แสดงมิติ** และทำการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="ccf5b-125">ถ้าคุณต้องการสร้างสินทรัพย์โดยยึดตามรายการใบสั่งซื้อ ให้เลือกกล่องกาเครื่องหมายในคอลัมน์ **ทำเครื่องหมาย** สำหรับรายการนั้นในหน้ารายการ แล้วคลิก **สร้างสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="ccf5b-126">ข้อความจะปรากฏขึ้นเพื่อแจ้งรหัสสินทรัพย์ให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="ccf5b-127">เลือกสินทรัพย์ในรายการ **สินทรัพย์ทั้งหมด** และคลิก **แก้ไข** เพื่อเพิ่มข้อมูลเพิ่มเติมให้กับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="ccf5b-128">ใน **สินทรัพย์ที่ค้างอยู่** ถ้าคุณต้องการลบรายการเนื่องจากคุณไม่ต้องการสร้างสินทรัพย์ ให้เลือกกล่องกาเครื่องหมายในคอลัมน์ **ทำเครื่องหมาย** สำหรับรายการนั้น และคลิก **ละทิ้งสินทรัพย์ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="ccf5b-129">ข้อความจะปรากฏขึ้นเพื่อแจ้งรหัสสินทรัพย์ให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="ccf5b-130">คุณไม่ได้ลบใบสั่งซื้อหรือใบสั่งขาย เพียงแค่เรกคอร์ดที่คุณสามารถสร้างสินทรัพย์ใน **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="ccf5b-131">มิติของผลิตภัณฑ์ทั้งหมด (ขนาด สี การตั้งค่าคอนฟิก ฯลฯ) จะถูกโอนย้ายไปยังแอททริบิวต์สินทรัพย์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="ccf5b-132">มิติการติดตาม (หมายเลขลำดับประจำสินค้า) จะถูกจัดเก็บไว้ในสินทรัพย์โดยตรง เมื่อมีการสร้างสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="ccf5b-133">ค้นหาสินทรัพย์ที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="ccf5b-133">Find pending assets</span></span>

<span data-ttu-id="ccf5b-134">คุณสามารถเรียกใช้ **การนับสินทรัพย์ที่ค้างอยู่** เพื่อตรวจสอบสินทรัพย์ที่ค้างอยู่</span><span class="sxs-lookup"><span data-stu-id="ccf5b-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="ccf5b-135">ตัวอย่างเช่น ฟังก์ชันนี้สามารถใช้สำหรับการรับการแจ้งเตือนในแต่ละครั้งที่สินทรัพย์ที่ค้างอยู่พร้อมที่จะสร้างเป็นสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="ccf5b-136">คลิก **การจัดการสินทรัพย์** > **ประจำงวด** > **สินทรัพย์** > **การนับสินทรัพย์ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="ccf5b-137">คลิก **ตกลง** เพื่อรันงานและปรับปรุงรายการใน **สินทรัพย์ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="ccf5b-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="ccf5b-138">คุณสามารถตั้งค่างานนี้ให้รันเป็นชุดงาน ตัวอย่างเช่น วันละหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="ccf5b-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="ccf5b-139">**ข้อควรระวัง:** ถ้าข้อมูลมีการเปลี่ยนแปลงในใบสั่งซื้อ *หลังจาก* คุณได้สร้างสินทรัพย์ตามสินค้าที่เกี่ยวข้องแล้ว การเปลี่ยนแปลงเหล่านั้นจะไม่มีผลในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="ccf5b-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
