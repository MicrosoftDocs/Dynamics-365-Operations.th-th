---
title: สร้างผลิตภัณฑ์ใหม่ใน Commerce
description: หัวข้อนี้จะอธิบายวิธีการสร้างผลิตภัณฑ์ใหม่ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965334"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="21536-103">สร้างผลิตภัณฑ์ใหม่ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="21536-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="21536-104">หัวข้อนี้จะอธิบายวิธีการสร้างผลิตภัณฑ์ใหม่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="21536-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="21536-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="21536-105">Overview</span></span>

<span data-ttu-id="21536-106">ส่วนใหญ่แล้ว จะมีการกำหนดผลิตภัณฑ์โดยเรียงตามหมายเลขสินค้า ชื่อ และคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="21536-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="21536-107">อย่างไรก็ตาม ข้อมูลอื่น ๆ ยังจำเป็นเพื่อที่จะอธิบายผลิตภัณฑ์หรือการบริการอีกด้วย:</span><span class="sxs-lookup"><span data-stu-id="21536-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="21536-108">สร้างผลิตภัณฑ์ใหม่</span><span class="sxs-lookup"><span data-stu-id="21536-108">Create a new product</span></span>

1. <span data-ttu-id="21536-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retai และการค้า \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์ตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="21536-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="21536-110">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="21536-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="21536-111">ในรายการแบบหล่นลง **ชนิดผลิตภัณฑ์** เลือก **สินค้า** หรือ **บริการ**</span><span class="sxs-lookup"><span data-stu-id="21536-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="21536-112">ในรายการแบบหล่นลง **ชนิดย่อยของผลิตภัณฑ์** เลือก **ผลิตภัณฑ์** (ถ้าผลิตภัณฑ์จะไม่มีตัวแปร) หรือ **ผลิตภัณฑ์หลัก** (ถ้าผลิตภัณฑ์จะมีตัวแปร)</span><span class="sxs-lookup"><span data-stu-id="21536-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="21536-113">ในกล่อง **หมายเลขผลิตภัณฑ์** ให้ป้อนหมายเลขผลิตภัณฑ์ ถ้ายังไม่มีการเติมข้อมูลไว้ล่วงหน้าไว้</span><span class="sxs-lookup"><span data-stu-id="21536-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="21536-114">ในกล่อง **ชื่อผลิตภัณฑ์** ให้ป้อนชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21536-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="21536-115">ในกล่อง **ชื่อสำหรับค้นหา** ให้ป้อนชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="21536-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="21536-116">ในรายการแบบหล่นลง **ประเภท Retail** ให้เลือกประเภทที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="21536-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="21536-117">ถ้าผลิตภัณฑ์เป็นชุด ให้เลือก **ใช่** สำหรับ **ชุดผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="21536-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="21536-118">ถ้าชนิดย่อยของผลิตภัณฑ์เป็นผลิตภัณฑ์หลัก ให้กำหนด **กลุ่มมิติของผลิตภัณฑ์** เพื่อรวมตัวแปรที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="21536-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="21536-119">ตัวเลือก ได้แก่ **สี** **ขนาด** **ลักษณะ** และ **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="21536-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="21536-120">คุณอาจต้องสร้างกลุ่มมิติของผลิตภัณฑ์เพิ่มเติม ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="21536-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="21536-121">ในรายการแบบหล่นลง **เทคโนโลยีการตั้งค่าคอนฟิก** ให้เลือกตัวเลือกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="21536-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="21536-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="21536-122">Select **OK**.</span></span>

<span data-ttu-id="21536-123">รูปภาพต่อไปนี้แสดงผลิตภัณฑ์ตัวอย่างที่มีการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="21536-123">The following image shows an example product being added.</span></span>

![สร้างผลิตภัณฑ์](media/create-new-product.png)

<span data-ttu-id="21536-125">เมื่อมีการเพิ่มผลิตภัณฑ์แล้ว คุณสามารถตั้งค่าข้อมูลเพิ่มเติมได้ เช่น **คำอธิบายผลิตภัณฑ์** **กลุ่มตัวแปร** **กลุ่มมิติ** **คุณลักษณะของผลิตภัณฑ์** และ **ผลิตภัณฑ์ที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="21536-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="21536-126">รูปภาพต่อไปนี้แสดงรายละเอียดเพิ่มเติมของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21536-126">The following image shows a product's additional details.</span></span>

![รายละเอียดผลิตภัณฑ์](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="21536-128">สร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="21536-128">Create product variants</span></span>

<span data-ttu-id="21536-129">ถ้าชนิดย่อยของผลิตภัณฑ์เป็น **ผลิตภัณฑ์หลัก** จะต้องมีการสร้างตัวแปรเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="21536-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="21536-130">เมื่อต้องการสร้างตัวแปรผลิตภัณฑ์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="21536-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="21536-131">ในบานหน้าต่างการดำเนินการ เลือก **ตัวแปรผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="21536-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="21536-132">ถ้ามีการเลือกกลุ่มตัวแปรในบานหน้าต่างการดำเนินการ ให้เลือก \**คำแนะนำตัวแปร*</span><span class="sxs-lookup"><span data-stu-id="21536-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="21536-133">เลือกตัวแปรที่คุณต้องการสนับสนุนสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21536-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="21536-134">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="21536-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="21536-135">นำผลิตภัณฑ์ออกใช้</span><span class="sxs-lookup"><span data-stu-id="21536-135">Release a product</span></span>

<span data-ttu-id="21536-136">เมื่อต้องการขายผลิตภัณฑ์ จะต้องนำออกใช้ในนิติบุคคลก่อน</span><span class="sxs-lookup"><span data-stu-id="21536-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="21536-137">จากหน้าผลิตภัณฑ์ ให้เลือก **นำผลิตภัณฑ์ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="21536-137">From the product page, select **Release products**.</span></span>

    ![นำผลิตภัณฑ์ออกใช้](media/create-new-product-3.png)

1. <span data-ttu-id="21536-139">เลือกผลิตภัณฑ์ที่จะนำออกใช้ แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="21536-139">Select the product to release, and then select **Next**.</span></span>

    ![เลือกผลิตภัณฑ์ที่จะนำออกใช้](media/create-new-product-4.png)

1. <span data-ttu-id="21536-141">เลือกชุดของตัวแปรผลิตภัณฑ์ที่จะนำออกใช้ แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="21536-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![เลือกตัวแปรที่จะนำออกใช้](media/create-new-product-5.png)

1. <span data-ttu-id="21536-143">เลือกนิติบุคคล แล้วเลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="21536-143">Select the legal entity, and then select **Next**.</span></span>

    ![เลือกนิติบุคคล](media/create-new-product-6.png)

1. <span data-ttu-id="21536-145">เลือก **เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="21536-145">Select **Finish**.</span></span>

    ![ทำให้การนำผลิตภัณฑ์ออกใช้เสร็จสิ้น](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="21536-147">ตั้งค่าคอนฟิกผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="21536-147">Configure a released product</span></span>

<span data-ttu-id="21536-148">หลังจากที่มีการนำผลิตภัณฑ์ออกใช้แล้ว จะต้องมีการตั้งค่าคอนฟิกเพิ่มเติมซึ่งรวมถึงการเพิ่มราคาให้กับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21536-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="21536-149">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> Retail และการค้า \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์ที่นำออกใช้ตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="21536-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="21536-150">เลือกโหนดประเภทของผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่นำออกใช้ แล้วเลือกผลิตภัณฑ์จากรายการผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21536-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="21536-151">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="21536-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="21536-152">ในส่วน **ซื้อ** ตั้งค่าคอนฟิกคุณสมบัติที่จำเป็นใดๆ ซึ่งรวมถึง **หน่วย** **ราคา** และ **ปริมาณ**</span><span class="sxs-lookup"><span data-stu-id="21536-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="21536-153">ในบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้อง** เพื่อตรวจสอบให้แน่ใจว่าไม่มีการรายงานข้อผิดพลาดสำหรับฟิลด์ที่ขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="21536-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="21536-154">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="21536-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="21536-155">รูปภาพต่อไปนี้แสดงตัวอย่างของการตั้งค่าคอนฟิกสำหรับผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="21536-155">The following image shows an example configuration for a released product.</span></span>

![ตั้งค่าคอนฟิกผลิตภัณฑ์ที่นำออกใช้](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="21536-157">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="21536-157">Additional resources</span></span>

[<span data-ttu-id="21536-158">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="21536-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="21536-159">สร้างกลุ่มตัวแปร</span><span class="sxs-lookup"><span data-stu-id="21536-159">Create a variant group</span></span>](create-variant-group.md) 
