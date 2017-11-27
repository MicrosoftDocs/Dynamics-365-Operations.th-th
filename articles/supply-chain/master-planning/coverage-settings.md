---
title: "การตั้งค่าความครอบคลุม"
description: "การวางแผนหลักใช้การตั้งค่าความครอบคลุมเพื่อคำนวณความต้องการสินค้า"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd85f89917659ac9c94590bace765b2123d6e556
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="d2265-103">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="d2265-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2265-104">การวางแผนหลักใช้การตั้งค่าความครอบคลุมเพื่อคำนวณความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="d2265-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="d2265-105">คุณสามารถระบุการตั้งค่าความครอบคลุมได้หลายวิธีดังนี้</span><span class="sxs-lookup"><span data-stu-id="d2265-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="d2265-106">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="d2265-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="d2265-107">คุณสามารถสร้างกลุ่มความครอบคลุมที่มีการตั้งค่าสำหรับผลิตภัณฑ์ทั้งหมดที่เชื่อมโยงกับกลุ่มความคุ้มครองได้</span><span class="sxs-lookup"><span data-stu-id="d2265-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="d2265-108">คลิก **การวางแผนหลัก &gt; การตั้งค่า &gt; ความครอบคลุม &gt; กลุ่มความครอบคลุม** เพื่อสร้างกลุ่มความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="d2265-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="d2265-109">เลือกวันที่ ระบบจะใช้ระดับทักษะที่แท้จริงของบุคคลในวันที่คุณเลือกสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="d2265-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="d2265-110">หากการเชื่อมโยงไปเฉพาะไซต์ คลังสินค้า หรือมิติของผลิตภัณฑ์ ให้ใช้ฟิลด์ **กลุ่มความคุ้มครอง** ในหน้าการ **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d2265-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="d2265-111">ถ้าเป็นลิงค์ทั่วไป โดยไม่คำนึงถึงมิติของผลิตภัณฑ์ ให้ใช้ **กลุ่มความคุ้มครอง** บนแท็บด่วน **แผน** บนหน้า **รายละเอียดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="d2265-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="d2265-112">ถ้าคุณไม่เชื่อมโยงกลุ่มความคุ้มครองกับผลิตภัณฑ์ การวางแผนหลักใช้ **กลุ่มความคุ้มครองทั่วไป** ที่ระบุในหน้า **พารามิเตอร์การวางแผนหลัก** เป็นค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="d2265-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="d2265-113">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d2265-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="d2265-114">คุณสามารถสร้างการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="d2265-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="d2265-115">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="d2265-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="d2265-116">เลือกผลิตภัณฑ์ บน **บานหน้าต่างการดำเนินการ** บนแท็บ **แผน** ใน **กลุ่มความคุ้มครอง** คลิก **ความครอบคลุมสินค้า** เพื่อเปิดหน้า **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d2265-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="d2265-117">ถ้าผลิตภัณฑ์มีการเชื่อมโยงกับกลุ่มความครอบคลุมแล้ว คุณสามารถแทนที่การตั้งค่ากลุ่มความครอบคลุมได้โดยใช้ฟิลด์ **แทนที่**</span><span class="sxs-lookup"><span data-stu-id="d2265-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="d2265-118">การตั้งค่าความครอบคลุมบนหน้า**ความครอบคลุมสินค้า** จะมีความสำคัญเหนือการตั้งค่าบนหน้า **กลุ่มความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="d2265-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="d2265-119">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์โดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="d2265-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="d2265-120">วิซาร์ดเป็นคำแนะนำทีละขั้นตอนที่จะช่วยในการตั้งค่าพารามิเตอร์ความครอบคลุมสินค้าหลัก</span><span class="sxs-lookup"><span data-stu-id="d2265-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="d2265-121">บนหน้า **ความครอบคลุมสินค้า** ให้คลิก **วิซาร์ด** เพื่อเปิด **วิซาร์ดความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="d2265-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="d2265-122">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="d2265-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="d2265-123">คลิก **การจัดการข้อมูลผลิตภัณฑ์ &gt; ทั่วไป &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="d2265-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="d2265-124">ในหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** ในแท็บ **ทั่วไป** ในกลุ่ม **การจัดการ** คลิกลิงค์ **กลุ่มมิติการจัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="d2265-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="d2265-125">ในหน้า **กลุ่มมิติการจัดเก็บ** ให้เลือกฟิลด์ **แผนความครอบคลุมตามมิติ** เพื่อสร้างการตั้งค่าความครอบคลุมสำหรับมิติในกลุ่มมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d2265-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="d2265-126">มิติสินค้าทั้งหมด เช่น การตั้งค่าคอนฟิก สี ขนาด ลักษณะ ต้องมีการเลือกฟิลด์ **วางแผนความครอบคลุมโดยเรียงตามมิติ** ไว้</span><span class="sxs-lookup"><span data-stu-id="d2265-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="d2265-127">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d2265-127">See also</span></span>
--------

[<span data-ttu-id="d2265-128">แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="d2265-128">Master plans</span></span>](master-plans.md)




