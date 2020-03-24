---
title: ตั้งค่าช่องทางร้านค้าออนไลน์
description: บทความนี้แสดงข้อมูลเกี่ยวกับช่องทางร้านค้าออนไลน์และวิธีการตั้งค่าใน Dynamics 365 Commerce
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096905"
---
# <a name="set-up-an-online-store-channel"></a><span data-ttu-id="6437b-103">ตั้งค่าช่องทางร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-103">Set up an online store channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6437b-104">บทความนี้แสดงข้อมูลเกี่ยวกับช่องทางร้านค้าออนไลน์และวิธีการตั้งค่าใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6437b-104">This article provides information about online store channels and how to set them up in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6437b-105">การค้ารองรับช่องทางการค้าปลีกหลายช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6437b-105">Commerce supports multiple retail channels.</span></span> <span data-ttu-id="6437b-106">ช่องทางเหล่านี้รวมไปถึงร้านค้าออนไลน์ ศูนย์บริการ และร้านค้าปลีก (หรือที่รู้จักกันในนาม ร้านค้าแบบดั้งเดิม)</span><span class="sxs-lookup"><span data-stu-id="6437b-106">These channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="6437b-107">ร้านค้าออนไลน์ให้มีสถานะออนไลน์กับผู้ค้าปลีก เพื่อให้ลูกค้าสามารถซื้อผลิตภัณฑ์จากร้านค้าออนไลน์ของผู้ค้าปลีกได้ นอกเหนือจากร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="6437b-107">Online stores give an online presence to a retailer, so that customers can purchase products from the retailer's online store in addition to its retail stores.</span></span> <span data-ttu-id="6437b-108">หากลูกค้าซื้อผลิตภัณฑ์จากร้านค้าออนไลน์ ผลิตภัณฑ์เหล่านั้นสามารถจัดส่งไปยังพวกเขา หรือลูกค้าสามารถเลือกรับผลิตภัณฑ์ที่ร้านค้าในพื้นที่</span><span class="sxs-lookup"><span data-stu-id="6437b-108">If customers purchase products from the online store, those products can be shipped to them, or the customers can pick the products up at a local store.</span></span> 

<span data-ttu-id="6437b-109">คุณสร้างร้านค้าออนไลน์ในไคลเอนต์การค้า</span><span class="sxs-lookup"><span data-stu-id="6437b-109">You create an online store in the Commerce client.</span></span> <span data-ttu-id="6437b-110">ร้านค้าออนไลน์นี้จะถูกเผยแพร่ไปยังร้านค้าออนไลน์ของบุคคลภายนอกที่รวมเข้ากับการค้า</span><span class="sxs-lookup"><span data-stu-id="6437b-110">This online store is then published to a third-party online store that is integrated with Commerce.</span></span> <span data-ttu-id="6437b-111">ร้านค้าออนไลน์ของบุคคลที่สามทำหน้าที่เป็น storefront (UI) สำหรับร้านค้าออนไลน์ และแสดงตัวเลือกของระบบการจัดการลูกค้า (CMS) และความสามารถใน UI</span><span class="sxs-lookup"><span data-stu-id="6437b-111">The third-party online store serves as the storefront (UI) for the online store, and gives you a choice of customer management system (CMS) and UI capabilities.</span></span> <span data-ttu-id="6437b-112">การรวมที่หลากหลายของชนิดนี้พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6437b-112">Several integrations of this type are available.</span></span> 

<span data-ttu-id="6437b-113">คุณสมบัติที่คุณกำหนดสำหรับออนไลน์จัดเก็บควบคุมพฤติกรรมของร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-113">The properties that you define for the online store control the behavior of the online store.</span></span> <span data-ttu-id="6437b-114">ตัวอย่างเช่น คุณกำหนดลำดับชั้นประเภทการนำทางและมอบหมายให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-114">For example, you define the navigation category hierarchy and assign it to the online store.</span></span> <span data-ttu-id="6437b-115">เมื่อคุณเผยแพร่ร้านค้าออนไลน์ไปยังร้านค้าออนไลน์ของบุคคลที่สาม ลำดับชั้นประเภทการนำทางจะปรากฏในแบบออนไลน์ของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="6437b-115">When you publish the online store to the third-party online store, the navigation category hierarchy appears in the online version of the store.</span></span> <span data-ttu-id="6437b-116">ผู้ซื้อสินค้าใช้ลำดับชั้นประเภทการนำทางเพื่อเรียกดูร้านค้าออนไลน์และค้นหาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6437b-116">Shoppers then use the navigation category hierarchy to browse the online store and search for products.</span></span> 

<span data-ttu-id="6437b-117">การสร้างร้านค้าออนไลน์ คุณต้องตั้งค่าคอมโพเนนต์ที่เปิดใช้งานธุรกรรมที่จะประมวลผลสำหรับร้านค้า</span><span class="sxs-lookup"><span data-stu-id="6437b-117">To create an online store, you must set up the components that enable transactions to be processed for the store.</span></span> <span data-ttu-id="6437b-118">ตัวอย่างเช่น คุณต้องเพิ่มการจัดประเภท ใช้แอททริบิวต์ และตั้งค่าวิธีการชำระเงินและวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6437b-118">For example, you must add assortments, apply attributes, and set up payment methods and shipping methods.</span></span> <span data-ttu-id="6437b-119">คุณยังสามารถกำหนดราคา การส่งเสริมการขาย ส่วนลด ข้อตกลงทางการค้า และเงื่อนไขการจัดส่งที่เฉพาะเจาะจงในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-119">You can also define prices, promotions, discounts, trade agreements, and shipping terms that are specific to the online store.</span></span> 

<span data-ttu-id="6437b-120">หลังจากที่คุณเผยแพร่ร้านค้าออนไลน์ไปยังร้านค้าออนไลน์ของบุคคลภายนอก คุณสามารถสร้างแคตตาล็อกผลิตภัณฑ์สำหรับร้านค้าออนไลน์ได้</span><span class="sxs-lookup"><span data-stu-id="6437b-120">After you publish the online store to the third-party online store, you can create product catalogs for the online store.</span></span> <span data-ttu-id="6437b-121">ผลิตภัณฑ์ในแค็ตตาล็อกจะแสดงรายการผลิตภัณฑ์ในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-121">The products in the catalog become product listings in the online store.</span></span> <span data-ttu-id="6437b-122">เมื่อผู้ซื้อซื้อผลิตภัณฑ์จากร้านค้าออนไลน์ สินค้าคงคลังที่มีอยู่จะถูกอัพเดต และซิงโครไนส์ในไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="6437b-122">When a shopper purchases products from the online store, the available inventory is updated and synchronized in the client.</span></span> <span data-ttu-id="6437b-123">นอกจากนี้ ใบสั่งขายจะถูกสร้างขึ้นสำหรับการซื้อ และจะถูกส่งไปยังไคลเอนต์สำหรับการเติมสินค้าของใบสั่งและการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="6437b-123">Additionally, sales orders are generated for the purchases, and are sent to the client for order fulfillment and processing.</span></span>

## <a name="set-up-an-online-store"></a><span data-ttu-id="6437b-124">ตั้งค่าร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-124">Set up an online store</span></span>

<span data-ttu-id="6437b-125">เพื่อตั้งค่าร้านค้าออนไลน์ คุณต้องดำเนินการต่อไปนี้ให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="6437b-125">To set up an online store, you must complete the following tasks.</span></span>

1. <span data-ttu-id="6437b-126">สร้างร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-126">Create the online store.</span></span>
2. <span data-ttu-id="6437b-127">เพิ่มร้านค้าออนไลน์กับลำดับชั้นขององค์กรที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="6437b-127">Add the online store to the appropriate organization hierarchies.</span></span>
3. <span data-ttu-id="6437b-128">เพิ่มการจัดประเภทที่รวมผลิตภัณฑ์พร้อมใช้งานในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-128">Add assortments that include the products that are available in the online store.</span></span>
4. <span data-ttu-id="6437b-129">กำหนดหรือสร้างกลุ่มราคาสำหรับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-129">Assign or create price groups for the online store.</span></span>
5. <span data-ttu-id="6437b-130">ตั้งค่าวิธีการจัดส่งที่พร้อมใช้งานสำหรับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-130">Set up the modes of delivery that are available for the online store.</span></span>
6. <span data-ttu-id="6437b-131">กำหนดวิธีการชำระเงินที่ยอมรับโดยร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-131">Assign the payment methods that are accepted by the online store.</span></span>
7. <span data-ttu-id="6437b-132">ถ้าคุณอนุญาตผู้ซื้อสินค้าสั่งผลิตภัณฑ์ทางออนไลน์ และจากนั้น เบิกสินค้าเหล่านั้นที่ร้านค้าท้องถิ่น กำหนดกลุ่มรหัสที่ตั้งร้านค้าให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-132">If you allow shoppers to order products online and then pick them up at a local store, assign store locator groups to the online store.</span></span>
8. <span data-ttu-id="6437b-133">กำหนดแอททริบิวต์สำหรับช่องทาง ผลิตภัณฑ์ และใบสั่งขายไปยังร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-133">Assign attributes for channels, products, and sales orders to the online store.</span></span> <span data-ttu-id="6437b-134">แอททริบิวต์ช่องทางที่ใช้กับร้านค้าออนไลน์ทั้งหมด คุณลักษณะของผลิตภัณฑ์ที่นำไปใช้กับผลิตภัณฑ์ที่นำเสนอในร้านค้าออนไลน์ และแอททริบิวต์ใบสั่งขายใช้กับใบสั่งขายที่สร้างขึ้นจากร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-134">Channel attributes apply to the whole online store, product attributes apply to the products that are offered in the online store, and sales order attributes apply to the sales orders that are generated from the online store.</span></span>
9. <span data-ttu-id="6437b-135">แม็ปแอททริบิวต์เพื่อตั้งค่าคุณสมบัติที่กำหนดวิธีทำแอททริบิวต์ร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-135">Map attributes to define the properties that determine how those attributes behave in the online store.</span></span> <span data-ttu-id="6437b-136">ตัวอย่างเช่น แอททริบิวต์ที่สามารถกำหนดว่าจำเป็น หรือสามารถค้นหาได้</span><span class="sxs-lookup"><span data-stu-id="6437b-136">For example, attributes can be defined as required or searchable.</span></span>
10. <span data-ttu-id="6437b-137">เผยแพร่ร้านค้าออนไลน์เพื่อสร้างโครงสร้างร้านค้าในตัวเลือกของร้านค้าออนไลน์ของบุคคลที่สามของคุณ</span><span class="sxs-lookup"><span data-stu-id="6437b-137">Publish the online store to generate the store structure on your choice of third-party online store.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6437b-138">ก่อนที่คุณจะเผยแพร่ร้านค้าออนไลน์ คุณต้องตั้งค่าที่ตั้งการกระจายสินค้านั้น</span><span class="sxs-lookup"><span data-stu-id="6437b-138">Before you publish the online store, you must set up a distribution location for it.</span></span>

## <a name="commerce-channel-navigation-hierarchies"></a><span data-ttu-id="6437b-139">ลำดับชั้นการนำทางของช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="6437b-139">Commerce channel navigation hierarchies</span></span>

<span data-ttu-id="6437b-140">ก่อนที่คุณจะสร้างร้านค้าออนไลน์ คุณต้องกำหนดลำดับชั้นการนำทางของช่องทางการค้าที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="6437b-140">Before you create an online store, you must define the commerce channel navigation hierarchy that you want to use for it.</span></span> <span data-ttu-id="6437b-141">ลำดับชั้นการนำทางของช่องทาง แสดงลำดับชั้นของประเภทที่แสดงในร้านค้าออนไลน์หลังจากที่ร้านค้าได้รับการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="6437b-141">The channel navigation hierarchy represents the category hierarchy that is displayed in the online store after the store is published.</span></span> <span data-ttu-id="6437b-142">เมื่อคุณเผยแพร่แค็ตตาล็อกผลิตภัณฑ์ไปยังร้านค้าออนไลน์ ผลิตภัณฑ์ในแค็ตตาล็อกจะถูกแมปกับประเภทในลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6437b-142">When you publish product catalogs to the online store, the products in the catalog are mapped to the categories in the channel navigation hierarchy.</span></span> <span data-ttu-id="6437b-143">ผู้ซื้อสินค้าใช้ลำดับชั้นการนำทางในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-143">Shoppers then use the hierarchy to navigate in the online store.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="6437b-144">ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6437b-144">Organization hierarchies</span></span>

<span data-ttu-id="6437b-145">ลำดับชั้นขององค์กรใช้เพื่อจัดโครงสร้างช่องทางการค้าและเพื่อแสดงความสัมพันธ์ระหว่างองค์กรที่ประกอบธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="6437b-145">Organization hierarchies are used to structure commerce channels and to represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="6437b-146">เมื่อคุณตั้งค่าร้านค้าออนไลน์ คุณสามารถเพิ่มเข้าไปในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="6437b-146">When you set up online stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="6437b-147">ร้านค้าแบ่งปันข้อมูลที่ใช้สำหรับการจัดประเภท การเพิ่มเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6437b-147">The stores then share the data that is used for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="6437b-148">เมื่อคุณสร้างลำดับชั้นขององค์กร คุณกำหนดวัตถุประสงค์นั้น</span><span class="sxs-lookup"><span data-stu-id="6437b-148">When you create an organization hierarchy, you assign a purpose to it.</span></span> <span data-ttu-id="6437b-149">วัตถุประสงค์บ่งชี้วิธีใช้ลำดับชั้นในโครงสร้างธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="6437b-149">The purpose indicates how the hierarchy is used in the business structure.</span></span> <span data-ttu-id="6437b-150">คุณสามารถสร้างลำดับชั้นขององค์กรหนึ่งสำหรับการดำเนินงานร้านค้า และใช้ลำดับชั้นนั้นสำหรับการจัดประเภท การเพิ่มเติมสินค้า และการรายงาน</span><span class="sxs-lookup"><span data-stu-id="6437b-150">You can create one organization hierarchy for your store operations, and use that hierarchy for assortments, replenishment, and reporting.</span></span> 

<span data-ttu-id="6437b-151">อีกทางหนึ่งคือ คุณสามารถสร้างลำดับชั้นขององค์กรแยกต่างหากสำหรับแต่ละวัตถุประสงค์</span><span class="sxs-lookup"><span data-stu-id="6437b-151">Alternatively, you can create a separate organization hierarchy for each purpose.</span></span> <span data-ttu-id="6437b-152">คุณสามารถสร้างหลายลำดับชั้นที่มีวัตถุประสงค์เดียวกัน และกำหนดช่องสัญญาณแยกต่างหากแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="6437b-152">You can also create multiple hierarchies that have the same purpose, and assign a separate channel to each one.</span></span> <span data-ttu-id="6437b-153">หากคุณวางแผนที่จะเผยแพร่แคตตาล็อกผลิตภัณฑ์ไปยังร้านค้าออนไลน์ คุณควรเพิ่มร้านค้าออนไลน์ลงในลำดับชั้นขององค์กรเพื่อจัดประเภทเป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="6437b-153">If you plan to publish product catalogs to the online store, you should, at a minimum, add the online store to an organization hierarchy for assortments.</span></span> <span data-ttu-id="6437b-154">มีเลือกผลิตภัณฑ์ในแค็ตตาล็อกจากการจัดประเภทที่กำหนดให้กับร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-154">The products in a catalog are selected from the assortments that are assigned to the online store.</span></span> <span data-ttu-id="6437b-155">เมื่อมีการเผยแพร่แค็ตตาล็อก กระบวนการเผยแพร่เปรียบเทียบวันที่มีผลบังคับใช้สำหรับการจัดประเภทที่กำหนดให้กับร้านค้าออนไลน์ที่มีผลิตภัณฑ์ที่รวมอยู่ในแค็ตตาล็อกเพื่อตรวจสอบว่าผลิตภัณฑ์ใดที่จะพร้อมใช้งานในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6437b-155">When the catalog is published, the publishing process compares the effective dates for the assortment that is assigned to the online store with the products that are included in the catalog to determine which products to make available in the online store.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6437b-156">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6437b-156">Additional resources</span></span>

[<span data-ttu-id="6437b-157">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="6437b-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6437b-158">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="6437b-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6437b-159">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="6437b-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6437b-160">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="6437b-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6437b-161">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="6437b-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6437b-162">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="6437b-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6437b-163">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="6437b-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6437b-164">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6437b-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6437b-165">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="6437b-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6437b-166">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="6437b-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6437b-167">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="6437b-167">Enable location-based store detection</span></span>](enable-store-detection.md)
