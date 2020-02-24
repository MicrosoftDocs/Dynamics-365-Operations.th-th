---
title: รับคำแนะนำเกี่ยวกับผลิตภัณฑ์โดยใช้ข้อมูลสาธิต
description: เอกสารนี้มีวัตถุประสงค์เพื่อให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตแบบกำหนดเองที่กำหนดไว้ล่วงหน้า
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6abac72b7530dc7b82c8e95faebdce791cf7dbd1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003245"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="091b8-103">รับคำแนะนำเกี่ยวกับผลิตภัณฑ์โดยใช้ข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="091b8-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="091b8-104">เอกสารนี้มีวัตถุประสงค์เพื่อให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตแบบกำหนดเองที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="091b8-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="091b8-105">คำแนะนำผลิตภัณฑ์ผ่านช่องทาง Omni จัดชุดของรายการสั่งสินค้าที่สร้างขึ้นโดยทางโปรแกรมหรือดูแลเกี่ยวกับการแก้ไขของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="091b8-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="091b8-106">รายการเหล่านี้สามารถใช้ได้ในหลายสถานการณ์ ขึ้นอยู่กับความต้องการของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="091b8-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="091b8-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="091b8-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="091b8-108">สำหรับคำแนะนำผลิตภัณฑ์ของสภาพแวดล้อม Dynamics 365 ในระดับ 2 และที่สูงกว่า จะคำนวณโดยอัตโนมัติตามข้อมูลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="091b8-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="091b8-109">การใช้ข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ไม่ได้ปิดใช้งานโซลูชันคำแนะนำผลิตภัณฑ์ใดๆที่เตรียมใช้งานในสภาพแวดล้อมและต้นทุนที่เกี่ยวข้องกับการใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="091b8-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="091b8-110">สำหรับคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อมระดับ 1 จะขึ้นอยู่กับข้อมูลสาธิตแบบคงที่ที่จัดเก็บอยู่ในไฟล์ .csv เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="091b8-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="091b8-111">การเปิดใช้งานข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="091b8-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="091b8-112">ในการจะจะเปิดใช้งานวันที่สาธิตคำแนะนำผลิตภัณฑ์ ลูกค้าจำเป็นต้องจัดวางการขยายของการสาธิตการแสดงตัวอย่าง Dynamics 365 Commerce ไปยังสภาพแวดล้อมที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="091b8-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="091b8-113">การดำเนินการดังกล่าวจะเปิดใช้งานข้อมูลสาธิตของผลิตภัณฑ์ที่แนะนำโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="091b8-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="091b8-114">ข้อมูลสาธิตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="091b8-114">Default demo data</span></span>
<span data-ttu-id="091b8-115">สภาพแวดล้อมของ Onebox แต่ละชนิดพร้อมกับชุดที่โหลดไว้แล้วของข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ถูกจัดเก็บในไฟล์ reco_demo_data.csv ที่แบ่งด้วยเครื่องหมายจุลภาค ซึ่งจัดเก็บอยู่บน Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="091b8-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="091b8-116">ข้อมูลนี้ได้จัดโครงสร้างตามคอลัมน์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="091b8-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="091b8-117">ชื่อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="091b8-117">Column name</span></span>         | <span data-ttu-id="091b8-118">ข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="091b8-118">Mandatory</span></span>          | <span data-ttu-id="091b8-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="091b8-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="091b8-120">ค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="091b8-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="091b8-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="091b8-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="091b8-123">ชนิดรายการคำแนะนำผลิตภัณฑ์เฉพาะที่ใช้ในจุดข้อมูลสาธิตมีไว้เพื่อสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="091b8-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="091b8-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="091b8-124">RecoBestSelling</span></span></li><li><span data-ttu-id="091b8-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="091b8-125">RecoNew</span></span></li><li><span data-ttu-id="091b8-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="091b8-126">RecoTrending</span></span></li><li><span data-ttu-id="091b8-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="091b8-127">RecoCart</span></span></li><li><span data-ttu-id="091b8-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="091b8-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="091b8-129">หมายเลขหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="091b8-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="091b8-131">หมายเลขหน่วยปฏิบัติงานเฉพาะที่คาดว่าจะมีการแสดงคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="091b8-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="091b8-132">ประเภท</span><span class="sxs-lookup"><span data-stu-id="091b8-132">Category</span></span>            |                    |    <span data-ttu-id="091b8-133">ปรเภทรายการเฉพาะที่ควรส่งคืน</span><span class="sxs-lookup"><span data-stu-id="091b8-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="091b8-134">ถ้าไม่มีการระบุประเภทไว้ รายการจะอยู่ด้านบนของลำดับชั้นการนำทางเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="091b8-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="091b8-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="091b8-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="091b8-136">สำหรับรายการที่จำเป็นต้องมีข้อมูลเริ่มต้น (RecoPeopleAlsoBuy และ RecoCart) ผลิตภัณฑ์ดังกล่าวควรแสดงผลิตภัณฑ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="091b8-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="091b8-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="091b8-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="091b8-139">ผลิตภัณฑ์หนึ่งรายการขึ้นไปที่จะส่งคืนเป็นผลลัพธ์ ซึ่งคั่นด้วย ';'</span><span class="sxs-lookup"><span data-stu-id="091b8-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="091b8-140">เลือกกำหนดข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="091b8-140">Customize demo data</span></span>
<span data-ttu-id="091b8-141">คุณสามารถแก้ไขข้อมูลการสาธิตเริ่มต้นกับผลิตภัณฑ์และข้อมูลประเภทใดๆ ที่ตั้งค่าคอนฟิกใน HQ</span><span class="sxs-lookup"><span data-stu-id="091b8-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="091b8-142">เมื่อมีการอัพเดต .cvs คำแนะนำผลิตภัณฑ์ที่ส่งคืนไปยังลูกค้าจะสะท้อนถึงการเปลี่ยนแปลงในทันที</span><span class="sxs-lookup"><span data-stu-id="091b8-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="091b8-143">นามสกุลมีไฟล์ข้อมูลที่เรียกว่า 'RecoMockDataset' ซึ่งช่วยให้ลูกค้าสามารถควบคุมชุดข้อมูลที่ใช้ขับเคลื่อนผลลัพธ์ของคำแนะนำจำลอง</span><span class="sxs-lookup"><span data-stu-id="091b8-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="091b8-144">ชื่อไฟล์สามารถควบคุมโดยการตั้งค่าคอนฟิกส่วนขยายโดยใช้การตั้งค่า **ext.Recommendations.DemoFilePath**</span><span class="sxs-lookup"><span data-stu-id="091b8-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="091b8-145">การทำเช่นนี้จะช่วยให้คุณมีชุดงานได้หลายชุด ซึ่งสามารถสลับไปมาได้ง่ายๆ ผ่านการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="091b8-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="091b8-146">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="091b8-146">Additional Resources</span></span>

[<span data-ttu-id="091b8-147">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="091b8-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="091b8-148">การวางแผนสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="091b8-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
