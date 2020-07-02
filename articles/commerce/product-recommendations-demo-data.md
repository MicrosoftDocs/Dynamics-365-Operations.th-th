---
title: สร้างคำแนะนำที่มีข้อมูลสาธิต
description: หัวข้อนี้ให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตที่สามารถกำหนดเองได้ซึ่งถูกเติมข้อมูลไว้ล่วงหน้า
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 59b4dd7a29af739d92a20f6fe55eff9f201fcb6d
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454567"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="c0855-103">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="c0855-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0855-104">หัวข้อนี้ให้คำแนะนำเกี่ยวกับวิธีการใช้งานคำแนะนำเกี่ยวกับผลิตภัณฑ์ผ่านช่องทาง omni ในสภาพแวดล้อมของกล่องเดี่ยวระดับ-1 โดยใช้ข้อมูลสาธิตที่สามารถกำหนดเองได้ซึ่งถูกเติมข้อมูลไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="c0855-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="c0855-105">คำแนะนำผลิตภัณฑ์ผ่านช่องทาง Omni จัดชุดของรายการสั่งสินค้าที่สร้างขึ้นโดยทางโปรแกรมหรือดูแลเกี่ยวกับการแก้ไขของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0855-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="c0855-106">รายการเหล่านี้สามารถใช้ได้ในหลายสถานการณ์ ขึ้นอยู่กับความต้องการของธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c0855-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="c0855-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="c0855-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="c0855-108">สำหรับคำแนะนำผลิตภัณฑ์ของสภาพแวดล้อม Dynamics 365 ในระดับ 2 และที่สูงกว่า จะคำนวณโดยอัตโนมัติตามข้อมูลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c0855-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="c0855-109">การใช้ข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ไม่ได้ปิดใช้งานโซลูชันคำแนะนำผลิตภัณฑ์ใดๆที่เตรียมใช้งานในสภาพแวดล้อมและต้นทุนที่เกี่ยวข้องกับการใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="c0855-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="c0855-110">สำหรับคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อมระดับ 1 จะขึ้นอยู่กับข้อมูลสาธิตแบบคงที่ที่จัดเก็บอยู่ในไฟล์ .csv เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c0855-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="c0855-111">การเปิดใช้งานข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="c0855-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="c0855-112">ในการเปิดใช้งานวันที่สาธิตคำแนะนำผลิตภัณฑ์ ลูกค้าจำเป็นต้องปรับใช้การขยายของการสาธิตการแสดงตัวอย่าง Dynamics 365 Commerce ไปยังสภาพแวดล้อมที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c0855-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="c0855-113">การดำเนินการดังกล่าวจะเปิดใช้งานข้อมูลสาธิตของผลิตภัณฑ์ที่แนะนำโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c0855-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="c0855-114">ข้อมูลสาธิตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c0855-114">Default demo data</span></span>
<span data-ttu-id="c0855-115">สภาพแวดล้อมชนิด Onebox แต่ละรายการมาพร้อมกับชุดที่โหลดไว้แล้วของข้อมูลสาธิตคำแนะนำผลิตภัณฑ์ ซึ่งถูกจัดเก็บในไฟล์ 'reco_demo_data.csv' ที่แบ่งด้วยเครื่องหมายจุลภาคที่ตั้งอยู่บน Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="c0855-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="c0855-116">ข้อมูลนี้ได้จัดโครงสร้างตามคอลัมน์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c0855-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="c0855-117">ชื่อคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="c0855-117">Column name</span></span>         | <span data-ttu-id="c0855-118">ข้อบังคับ</span><span class="sxs-lookup"><span data-stu-id="c0855-118">Mandatory</span></span>          | <span data-ttu-id="c0855-119">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c0855-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="c0855-120">ค่าที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="c0855-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c0855-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="c0855-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="c0855-123">ชนิดรายการคำแนะนำผลิตภัณฑ์เฉพาะที่ใช้ในจุดข้อมูลสาธิตมีไว้เพื่อสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c0855-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="c0855-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="c0855-124">RecoBestSelling</span></span></li><li><span data-ttu-id="c0855-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="c0855-125">RecoNew</span></span></li><li><span data-ttu-id="c0855-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="c0855-126">RecoTrending</span></span></li><li><span data-ttu-id="c0855-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="c0855-127">RecoCart</span></span></li><li><span data-ttu-id="c0855-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="c0855-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="c0855-129">หมายเลขหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c0855-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="c0855-131">หมายเลขหน่วยปฏิบัติงานเฉพาะที่คาดว่าจะมีการแสดงคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0855-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="c0855-132">ประเภท</span><span class="sxs-lookup"><span data-stu-id="c0855-132">Category</span></span>            |                    |    <span data-ttu-id="c0855-133">ปรเภทรายการเฉพาะที่ควรส่งคืน</span><span class="sxs-lookup"><span data-stu-id="c0855-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="c0855-134">ถ้าไม่มีการระบุประเภทไว้ รายการจะอยู่ด้านบนของลำดับชั้นการนำทางเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c0855-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="c0855-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="c0855-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="c0855-136">สำหรับรายการที่จำเป็นต้องมีข้อมูลเริ่มต้น (RecoPeopleAlsoBuy และ RecoCart) ผลิตภัณฑ์ดังกล่าวควรแสดงผลิตภัณฑ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c0855-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="c0855-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="c0855-137">CustomerId</span></span>          |                    |    <span data-ttu-id="c0855-138">สำหรับรายการที่จำเป็นต้องมีตัวระบุลูกค้า (RecoPicks)</span><span class="sxs-lookup"><span data-stu-id="c0855-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="c0855-139">ค่าเริ่มต้น '0' นำไปใช้กับลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c0855-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="c0855-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="c0855-140">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="c0855-142">ผลิตภัณฑ์หนึ่งรายการขึ้นไปที่จะส่งคืนเป็นผลลัพธ์ ซึ่งคั่นด้วย ';'</span><span class="sxs-lookup"><span data-stu-id="c0855-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="c0855-143">เลือกกำหนดข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="c0855-143">Customize demo data</span></span>
<span data-ttu-id="c0855-144">คุณสามารถแก้ไขข้อมูลการสาธิตเริ่มต้นกับผลิตภัณฑ์และข้อมูลประเภทใดๆ ที่ตั้งค่าคอนฟิกใน HQ</span><span class="sxs-lookup"><span data-stu-id="c0855-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="c0855-145">หลังจากการอัปเดต .cvs คำแนะนำผลิตภัณฑ์ที่ส่งคืนไปยังลูกค้าจะสะท้อนถึงการเปลี่ยนแปลงในทันที</span><span class="sxs-lookup"><span data-stu-id="c0855-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="c0855-146">นามสกุลมีไฟล์ข้อมูลที่เรียกว่า 'RecoMockDataset.csv' ซึ่งช่วยให้คุณสามารถควบคุมชุดข้อมูลที่ใช้ขับเคลื่อนผลลัพธ์ของคำแนะนำจำลอง</span><span class="sxs-lookup"><span data-stu-id="c0855-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="c0855-147">ชื่อไฟล์สามารถควบคุมโดยการตั้งค่าคอนฟิกส่วนขยายโดยใช้การตั้งค่า **ext.Recommendations.DemoFilePath**</span><span class="sxs-lookup"><span data-stu-id="c0855-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="c0855-148">การทำเช่นนี้จะช่วยให้คุณมีชุดงานได้หลายชุด ซึ่งสามารถสลับไปมาได้ง่ายๆ ผ่านการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c0855-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="c0855-149">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c0855-149">Additional resources</span></span>

[<span data-ttu-id="c0855-150">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0855-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c0855-151">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c0855-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c0855-152">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0855-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c0855-153">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0855-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c0855-154">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="c0855-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="c0855-155">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="c0855-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="c0855-156">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c0855-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c0855-157">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="c0855-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c0855-158">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c0855-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c0855-159">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c0855-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
