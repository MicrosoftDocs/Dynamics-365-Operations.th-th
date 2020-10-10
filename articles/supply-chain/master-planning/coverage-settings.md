---
title: การตั้งค่าความครอบคลุม
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าความครอบคลุมซึ่งการจัดกำหนดการหลักจะใช้ในการคำนวณความต้องการสินค้า
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9a170ee07da27977fd65ef8f01f3bb87b7ef8b4
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887125"
---
# <a name="coverage-settings"></a><span data-ttu-id="297fc-103">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="297fc-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="297fc-104">การวางแผนหลักใช้การตั้งค่าความครอบคลุมเพื่อคำนวณความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="297fc-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="297fc-105">คุณสามารถระบุการตั้งค่าความครอบคลุมได้หลายวิธีดังนี้</span><span class="sxs-lookup"><span data-stu-id="297fc-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="297fc-106">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="297fc-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="297fc-107">คุณสามารถสร้างกลุ่มความครอบคลุมที่มีการตั้งค่าสำหรับผลิตภัณฑ์ทั้งหมดที่เชื่อมโยงกับกลุ่มความคุ้มครองได้</span><span class="sxs-lookup"><span data-stu-id="297fc-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="297fc-108">ในการสร้างกลุ่มความครอบคลุม ไปยัง **การวางแผนหลัก &gt; การตั้งค่า &gt; ความครอบคลุม &gt; กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="297fc-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="297fc-109">เลือกวันที่ ระบบจะใช้ระดับทักษะที่แท้จริงของบุคคลในวันที่คุณเลือกสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="297fc-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="297fc-110">หากการเชื่อมโยงไปเฉพาะไซต์ คลังสินค้า หรือมิติของผลิตภัณฑ์ ให้ใช้ฟิลด์ **กลุ่มความคุ้มครอง** ในหน้าการ **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="297fc-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="297fc-111">ถ้าลิงค์เป็นแบบทั่วไป โดยไม่คำนึงถึงมิติของผลิตภัณฑ์ ให้ใช้ฟิลด์ **กลุ่มความครอบคลุม** บน FastTab **แผน** ของหน้า **รายละเอียดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="297fc-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="297fc-112">โดยค่าเริ่มต้น ถ้าคุณไม่เชื่อมโยงกลุ่มความครอบคลุมกับผลิตภัณฑ์ การวางแผนหลักจะใช้กลุ่มความครอบคลุมทั่วไปที่ระบุในหน้า **พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="297fc-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="297fc-113">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="297fc-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="297fc-114">คุณสามารถสร้างการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="297fc-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="297fc-115">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="297fc-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="297fc-116">เลือกผลิตภัณฑ์ และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **แผน** ในกลุ่ม **ความครอบคลุม** เลือก **ความครอบคลุมสินค้า** เพื่อเปิดหน้า **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="297fc-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="297fc-117">ถ้าผลิตภัณฑ์มีการเชื่อมโยงกับกลุ่มความครอบคลุมแล้ว คุณสามารถแทนที่การตั้งค่ากลุ่มความครอบคลุมได้โดยใช้ฟิลด์ **แทนที่**</span><span class="sxs-lookup"><span data-stu-id="297fc-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="297fc-118">การตั้งค่าความครอบคลุมบนหน้า**ความครอบคลุมสินค้า** จะมีความสำคัญเหนือการตั้งค่าบนหน้า **กลุ่มความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="297fc-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="297fc-119">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์โดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="297fc-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="297fc-120">วิซาร์ดแนะนำคุณทีละขั้นตอนเกี่ยวกับกระบวนการของการตั้งค่าพารามิเตอร์ความครอบคลุมสินค้าหลัก</span><span class="sxs-lookup"><span data-stu-id="297fc-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="297fc-121">บนหน้า **ความครอบคลุมสินค้า** บนบานหน้าต่างการดำเนินการ ให้เลือก **วิซาร์ด** เพื่อเปิด **วิซาร์ดความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="297fc-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="297fc-122">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="297fc-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="297fc-123">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="297fc-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="297fc-124">บนหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** บน FastTab **ทั่วไป** ในส่วน **การจัดการ** เลือกลิงค์ในฟิลด์ **กลุ่มมิติการจัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="297fc-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="297fc-125">บนหน้า **กลุ่มมิติการจัดเก็บ** ให้เลือกกล่องกาเครื่องหมาย **แผนความครอบคลุมตามมิติ** เพื่อสร้างการตั้งค่าความครอบคลุมสำหรับมิติในกลุ่มมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="297fc-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="297fc-126">ฟิลด์ **แผนความครอบคลุมตามมิติ** ต้องถูกเลือกสำหรับมิติของผลิตภัณฑ์ทั้งหมด เช่น การตั้งค่าคอนฟิก สี และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="297fc-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="297fc-127">รหัสความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="297fc-127">Coverage codes</span></span>

<span data-ttu-id="297fc-128">คุณสามารถตั้งค่าคอนฟิกการวางแผนหลักเพื่อใช้วิธีการเติมสินค้าที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="297fc-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="297fc-129">วิธีการเติมสินค้าหรือวิธีการปรับขนาดล็อตเป็นเทคนิคที่ใช้โดยระบบเพื่อกำหนดขนาดชุดงานสำหรับสินค้าที่ซื้อหรือผลิต</span><span class="sxs-lookup"><span data-stu-id="297fc-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="297fc-130">วิธีการเติมสินค้าที่มีการกำหนดรหัสความครอบคลุมอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="297fc-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="297fc-131">**ด้วยตนเอง** - วิธีการปรับขนาดล็อตซึ่งระบบจะไม่แนะนำใบสั่งซื้อโอนย้ายหรือใบสั่งผลิตสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="297fc-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="297fc-132">ผู้วางแผนของสินค้าจะเป็นผู้รับผิดชอบการสร้างใบสั่งที่จำเป็นสำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="297fc-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="297fc-133">**ต่อความต้องการ** - การปรับขนาดล็อตซึ่งระบบจะสร้างการสั่งซื้อ การโอนย้าย หรือใบสั่งผลิตที่วางแผนไว้แล้ว ต่อความต้องการของแต่ละรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="297fc-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="297fc-134">โดยทั่วไปจะถูกใช้กับสิ้นค้าที่มีราคาแพงที่มีความต้องการไม่สม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="297fc-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="297fc-135">**แต่ละรอบระยะเวลา** - วิธีการปรับขนาดล็อตซึ่งรวมความต้องการทั้งหมดในรอบระยะเวลาหนึ่งสำหรับสินค้าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="297fc-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="297fc-136">ใบสั่งจะถูกวางแผนสำหรับวันแรกของรอบระยะเวลา และปริมาณของสินค้าจะเป็นไปตามข้อกำหนดสุทธิในรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="297fc-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="297fc-137">รอบระยะเวลาจะเริ่มต้นด้วยความต้องการสินค้าชิ้นแรกและครอบคลุมระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="297fc-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="297fc-138">รอบระยะเวลาถัดไปจะเริ่มต้นจากความต้องการของสินค้าชิ้นถัดไป</span><span class="sxs-lookup"><span data-stu-id="297fc-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="297fc-139">**ต่ำสุด/สูงสุด** - วิธีการปรับขนาดล็อตที่มีการเติมสินค้าคงคลังจนถึงระดับหนึ่ง เมื่อปริมาณคงคลังคงที่เหลืออยู่ต่ำกว่าขีดจำกัดที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="297fc-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="297fc-140">ปริมาณการเติมสินค้าจะแตกต่างกันกันไประหว่างระดับสูงสุดและระดับปริมาณคงคลังที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="297fc-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="297fc-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="297fc-141">Additional resources</span></span>

[<span data-ttu-id="297fc-142">ภาพรวมของแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="297fc-142">Master plans overview</span></span>](master-plans.md)
