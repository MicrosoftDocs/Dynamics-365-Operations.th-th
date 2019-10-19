---
title: ข้อมูลสาธิตคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง Omni
description: เอกสารนี้มีวัตถุประสงค์เพื่อให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตแบบกำหนดเองที่กำหนดไว้ล่วงหน้า
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226507"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="bddf0-103">ข้อมูลสาธิตคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="bddf0-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="bddf0-104">เอกสารนี้มีวัตถุประสงค์เพื่อให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตแบบกำหนดเองที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="bddf0-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="bddf0-105">คำแนะนำผลิตภัณฑ์ผ่านช่องทาง Omni จัดชุดของรายการสั่งสินค้าที่สร้างขึ้นโดยทางโปรแกรมหรือดูแลเกี่ยวกับการแก้ไขของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bddf0-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="bddf0-106">รายการเหล่านี้สามารถใช้ได้ในหลายสถานการณ์ ขึ้นอยู่กับความต้องการของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="bddf0-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="bddf0-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendaitons-overview.md)</span><span class="sxs-lookup"><span data-stu-id="bddf0-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="bddf0-108">สำหรับคำแนะนำผลิตภัณฑ์ของสภาพแวดล้อม Dynamics แบบเทียร์ 2 และสูงกว่าจะคำนวณโดยอัตโนมัติตามข้อมูลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="bddf0-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="bddf0-109">การใช้ข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ไม่ได้ปิดใช้งานโซลูชันคำแนะนำผลิตภัณฑ์ใดๆที่เตรียมใช้งานในสภาพแวดล้อมและต้นทุนที่เกี่ยวข้องกับการใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="bddf0-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="bddf0-110">สำหรับคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อมระดับชั้น1จะขึ้นอยู่กับข้อมูลสาธิตแบบคงที่ที่จัดเก็บอยู่ในไฟล์ csv เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bddf0-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="bddf0-111">การเปิดใช้งานข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="bddf0-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="bddf0-112">ลูกค้าจำเป็นต้องจัดวาง **Dynamics 365 Commerce การขยายของการสาธิตการแสดงตัวอย่าง** ไปยังสภาพแวดล้อมที่เกี่ยวข้อง ซึ่งจะเปิดใช้งานข้อมูลสาธิตคำแนะนำผลิตภัณฑ์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bddf0-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="bddf0-113">ข้อมูลสาธิตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bddf0-113">Default demo data</span></span>
<span data-ttu-id="bddf0-114">สภาพแวดล้อมของ Onebox แต่ละชนิดพร้อมกับชุดที่โหลดไว้แล้วของข้อมูลสาธิตคำแนะนำผลิตภัณฑ์จัดเก็บในไฟล์ที่แบ่งด้วยเครื่องหมายจุลภาค **reco_demo_data.csv** ซึ่งจัดเก็บอยู่ในโฟลเดอร์เดียวกันกับเอกสารนี้บนเซิร์ฟเวอร์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="bddf0-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="bddf0-115">ข้อมูลนี้ได้จัดโครงสร้างตามคอลัมน์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bddf0-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="bddf0-116">ชื่อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="bddf0-116">Column name</span></span>         | <span data-ttu-id="bddf0-117">ข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="bddf0-117">Mandatory</span></span>          | <span data-ttu-id="bddf0-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bddf0-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="bddf0-119">ค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="bddf0-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bddf0-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="bddf0-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="bddf0-122">ชนิดรายการคำแนะนำผลิตภัณฑ์เฉพาะที่ใช้ในจุดข้อมูลสาธิตจะได้สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="bddf0-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="bddf0-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="bddf0-123">RecoBestSelling</span></span></li><li><span data-ttu-id="bddf0-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="bddf0-124">RecoNew</span></span></li><li><span data-ttu-id="bddf0-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="bddf0-125">RecoTrending</span></span></li><li><span data-ttu-id="bddf0-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="bddf0-126">RecoCart</span></span></li><li><span data-ttu-id="bddf0-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="bddf0-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="bddf0-128">หมายเลขหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="bddf0-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="bddf0-130">หมายเลขหน่วยปฏิบัติงานเฉพาะที่คาดว่าจะมีการแสดงคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bddf0-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="bddf0-131">ประเภท</span><span class="sxs-lookup"><span data-stu-id="bddf0-131">Category</span></span>            |                    |    <span data-ttu-id="bddf0-132">ปรเภทรายการเฉพาะที่ควรส่งคืน</span><span class="sxs-lookup"><span data-stu-id="bddf0-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="bddf0-133">ถ้าไม่มีการระบุประเภทไว้ รายการจะอยู่ด้านบนของลำดับชั้นการนำทางเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="bddf0-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="bddf0-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="bddf0-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="bddf0-135">สำหรับรายการที่จำเป็นต้องมีข้อมูลเริ่มต้น (RecoPeopleAlsoBuy และ RecoCart) ผลิตภัณฑ์ดังกล่าวควรแสดงผลิตภัณฑ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bddf0-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="bddf0-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="bddf0-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="bddf0-138">ผลิตภัณฑ์หนึ่งรายการขึ้นไปที่จะส่งคืนเป็นผลลัพธ์ ซึ่งคั่นด้วย **';'**</span><span class="sxs-lookup"><span data-stu-id="bddf0-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="bddf0-139">เลือกกำหนดข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="bddf0-139">Customize demo data</span></span>
<span data-ttu-id="bddf0-140">ลูกค้าสามารถแก้ไขข้อมูลสาธิตเริ่มต้นกับผลิตภัณฑ์และข้อมูลประเภทใดๆที่ตั้งค่าคอนฟิกใน HQ</span><span class="sxs-lookup"><span data-stu-id="bddf0-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="bddf0-141">เมื่อมีการอัพเดต CSV คำแนะนำผลิตภัณฑ์ที่ส่งคืนไปยังลูกค้าจะสะท้อนถึงการเปลี่ยนแปลงในทันที</span><span class="sxs-lookup"><span data-stu-id="bddf0-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="bddf0-142">นามสกุลมีไฟล์ข้อมูลที่เรียกว่า RecoMockDataset ซึ่งช่วยให้ลูกค้าสามารถควบคุมชุดข้อมูลที่ใช้ขับเคลื่อนผลลัพธ์ของคำแนะนำจำลอง</span><span class="sxs-lookup"><span data-stu-id="bddf0-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="bddf0-143">ชื่อไฟล์สามารถควบคุมโดยการตั้งค่าคอนฟิกส่วนขยายโดยใช้การตั้งค่า **ext.Recommendations.DemoFilePath**</span><span class="sxs-lookup"><span data-stu-id="bddf0-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="bddf0-144">การทำเช่นนี้จะช่วยให้ลูกค้าสามารถมีชุดงานได้หลายชุดซึ่งสามารถสลับไปมาได้ง่ายผ่านการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="bddf0-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="bddf0-145">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bddf0-145">Additional resources</span></span>

[<span data-ttu-id="bddf0-146">ภาพรวมคำแนะนำของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bddf0-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="bddf0-147">การวางแผนสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="bddf0-147">Environment planning</span></span>](environment-planning.md)
