---
title: การตั้งค่าความครอบคลุม
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าความครอบคลุมซึ่งการจัดกำหนดการหลักจะใช้ในการคำนวณความต้องการสินค้า
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538905"
---
# <a name="coverage-settings"></a><span data-ttu-id="bda88-103">การตั้งค่าความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="bda88-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bda88-104">การวางแผนหลักใช้การตั้งค่าความครอบคลุมเพื่อคำนวณความต้องการสินค้า</span><span class="sxs-lookup"><span data-stu-id="bda88-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="bda88-105">คุณสามารถระบุการตั้งค่าความครอบคลุมได้หลายวิธีดังนี้</span><span class="sxs-lookup"><span data-stu-id="bda88-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="bda88-106">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="bda88-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="bda88-107">คุณสามารถสร้างกลุ่มความครอบคลุมที่มีการตั้งค่าสำหรับผลิตภัณฑ์ทั้งหมดที่เชื่อมโยงกับกลุ่มความคุ้มครองได้</span><span class="sxs-lookup"><span data-stu-id="bda88-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="bda88-108">ในการสร้างกลุ่มความครอบคลุม ไปยัง **การวางแผนหลัก &gt; การตั้งค่า &gt; ความครอบคลุม &gt; กลุ่มความครอบคลุม**</span><span class="sxs-lookup"><span data-stu-id="bda88-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="bda88-109">เลือกวันที่ ระบบจะใช้ระดับทักษะที่แท้จริงของบุคคลในวันที่คุณเลือกสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="bda88-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="bda88-110">หากการเชื่อมโยงไปเฉพาะไซต์ คลังสินค้า หรือมิติของผลิตภัณฑ์ ให้ใช้ฟิลด์ **กลุ่มความคุ้มครอง** ในหน้าการ **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bda88-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="bda88-111">ถ้าลิงค์เป็นแบบทั่วไป โดยไม่คำนึงถึงมิติของผลิตภัณฑ์ ให้ใช้ฟิลด์ **กลุ่มความครอบคลุม** บน FastTab **แผน** ของหน้า **รายละเอียดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="bda88-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="bda88-112">โดยค่าเริ่มต้น ถ้าคุณไม่เชื่อมโยงกลุ่มความครอบคลุมกับผลิตภัณฑ์ การวางแผนหลักจะใช้กลุ่มความครอบคลุมทั่วไปที่ระบุในหน้า **พารามิเตอร์การวางแผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="bda88-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="bda88-113">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bda88-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="bda88-114">คุณสามารถสร้างการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์เฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="bda88-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="bda88-115">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="bda88-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="bda88-116">เลือกผลิตภัณฑ์ และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **แผน** ในกลุ่ม **ความครอบคลุม** เลือก **ความครอบคลุมสินค้า** เพื่อเปิดหน้า **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bda88-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="bda88-117">ถ้าผลิตภัณฑ์มีการเชื่อมโยงกับกลุ่มความครอบคลุมแล้ว คุณสามารถแทนที่การตั้งค่ากลุ่มความครอบคลุมได้โดยใช้ฟิลด์ **แทนที่**</span><span class="sxs-lookup"><span data-stu-id="bda88-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="bda88-118">การตั้งค่าความครอบคลุมบนหน้า**ความครอบคลุมสินค้า** จะมีความสำคัญเหนือการตั้งค่าบนหน้า **กลุ่มความคุ้มครอง**</span><span class="sxs-lookup"><span data-stu-id="bda88-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="bda88-119">ระบุการตั้งค่าความครอบคลุมสำหรับผลิตภัณฑ์โดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="bda88-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="bda88-120">วิซาร์ดแนะนำคุณทีละขั้นตอนเกี่ยวกับกระบวนการของการตั้งค่าพารามิเตอร์ความครอบคลุมสินค้าหลัก</span><span class="sxs-lookup"><span data-stu-id="bda88-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="bda88-121">บนหน้า **ความครอบคลุมสินค้า** บนบานหน้าต่างการดำเนินการ ให้เลือก **วิซาร์ด** เพื่อเปิด **วิซาร์ดความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="bda88-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="bda88-122">ระบุการตั้งค่าความครอบคลุมสำหรับกลุ่มมิติ</span><span class="sxs-lookup"><span data-stu-id="bda88-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="bda88-123">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ &gt; ผลิตภัณฑ์ &gt; ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="bda88-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="bda88-124">บนหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** บน FastTab **ทั่วไป** ในส่วน **การจัดการ** เลือกลิงค์ในฟิลด์ **กลุ่มมิติการจัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="bda88-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="bda88-125">บนหน้า **กลุ่มมิติการจัดเก็บ** ให้เลือกกล่องกาเครื่องหมาย **แผนความครอบคลุมตามมิติ** เพื่อสร้างการตั้งค่าความครอบคลุมสำหรับมิติในกลุ่มมิติการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="bda88-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="bda88-126">ฟิลด์ **แผนความครอบคลุมตามมิติ** ต้องถูกเลือกสำหรับมิติของผลิตภัณฑ์ทั้งหมด เช่น การตั้งค่าคอนฟิก สี และลักษณะ</span><span class="sxs-lookup"><span data-stu-id="bda88-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bda88-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bda88-127">Additional resources</span></span>

[<span data-ttu-id="bda88-128">แผนหลัก</span><span class="sxs-lookup"><span data-stu-id="bda88-128">Master plans</span></span>](master-plans.md)
