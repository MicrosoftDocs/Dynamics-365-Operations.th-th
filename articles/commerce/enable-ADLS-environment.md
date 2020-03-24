---
title: เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage (ADLS) สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553e1512ba72559923403eef741ce08222172a09
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127778"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="9fa95-103">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9fa95-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9fa95-104">หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage (ADLS) สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9fa95-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="9fa95-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9fa95-105">Overview</span></span>

<span data-ttu-id="9fa95-106">ในโซลูชัน Dynamics 365 Commerce ข้อมูลผลิตภัณฑ์และธุรกรรมทั้งหมดจะถูกติดตามในที่เก็บเอนทิตีของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9fa95-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="9fa95-107">เพื่อให้ข้อมูลนี้สามารถเข้าถึงได้จากบริการอื่น ๆ ของ Dynamics 365 เช่น การวิเคราะห์ข้อมูล ข่าวกรองทางธุรกิจ และคำแนะนำส่วนตัว โดยจำเป็นต้องเชื่อมต่อสภาพแวดล้อมกับโซลูชัน Azure Data Lake Storage Gen 2 (ADLS) ของลูกค้าเอง</span><span class="sxs-lookup"><span data-stu-id="9fa95-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="9fa95-108">เนื่องจาก ADLS ได้รับการกำหนดค่าในสภาพแวดล้อม ข้อมูลที่จำเป็นทั้งหมดจะถูกสะท้อนจากที่เก็บเอนทิตีในขณะที่ยังคงได้รับการป้องกันไว้อยู่และอยู่ภายใต้การควบคุมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9fa95-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="9fa95-109">หากเปิดใช้งานคำแนะนำผลิตภัณฑ์หรือคำแนะนำส่วนตัวในสภาพแวดล้อมด้วยแล้ว สแตกคำแนะนำผลิตภัณฑ์จะได้รับสิทธิ์การเข้าถึงโฟลเดอร์เฉพาะใน ADLS เพื่อดึงข้อมูลลูกค้าและคำนวณคำแนะนำตามข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="9fa95-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9fa95-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9fa95-110">Prerequisites</span></span>

<span data-ttu-id="9fa95-111">ลูกค้าจำเป็นต้องมีการกำหนดค่า ADLS ในการสมัครใช้งาน Azure ที่พวกเขาเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="9fa95-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="9fa95-112">หัวข้อนี้ไม่ครอบคลุมการซื้อการสมัครใช้งาน Azure หรือการตั้งค่าบัญชีที่เก็บข้อมูลที่เปิดใช้งาน ADLS</span><span class="sxs-lookup"><span data-stu-id="9fa95-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="9fa95-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ ADLS ดู [เอกสารอย่างเป็นทางการของ ADLS](https://azure.microsoft.com/pricing/details/storage/data-lake)</span><span class="sxs-lookup"><span data-stu-id="9fa95-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="9fa95-114">ขั้นตอนการกำหนดค่า </span><span class="sxs-lookup"><span data-stu-id="9fa95-114">Configuration steps</span></span>

<span data-ttu-id="9fa95-115">ส่วนนี้ครอบคลุมขั้นตอนการกำหนดค่าที่จำเป็นสำหรับการเปิดใช้งาน ADLS ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9fa95-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="9fa95-116">เปืดใช้งาน ADLS ในสภาพแวดล้อม </span><span class="sxs-lookup"><span data-stu-id="9fa95-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="9fa95-117">ล็อกอินเข้าสู่พอร์ทัลสนับสนุนของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9fa95-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="9fa95-118">ค้นหา **พารามิเตอร์ระบบ** และนำทางไปที่แท็บ **การเชื่อมโยงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9fa95-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="9fa95-119">ตั้งค่า **เปิดใช้งานการรวม Data Lake** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9fa95-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="9fa95-120">ตั้งค่า **เปิดใช้งานการปรับปรุงทริกเกิล Data Lake** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9fa95-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="9fa95-121">จากนั้นป้อนข้อมูลที่จำเป็นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9fa95-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="9fa95-122">**รหัสแอปพลิเคชัน** // **ข้อมูลลับของแอปพลิเคชัน** // **ชื่อ DNS** - จำเป็นต้องเชื่อมต่อกับ KeyVault ที่ซึ่งความลับ ADLS ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="9fa95-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="9fa95-123">**ชื่อลับ** - ชื่อลับที่เก็บไว้ใน KeyVault และใช้เพื่อรับรองความถูกต้องกับ ADLS</span><span class="sxs-lookup"><span data-stu-id="9fa95-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="9fa95-124">บันทึกการเปลี่ยนแปลงของคุณในหน้าที่อยู่มุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="9fa95-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="9fa95-125">ภาพต่อไปนี้แสดงตัวอย่างของการกำหนดค่า ADLS</span><span class="sxs-lookup"><span data-stu-id="9fa95-125">The following image shows an example ADLS configuration.</span></span>

![ตัวอย่างการกำหนดค่า ADLS](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="9fa95-127">ทดสอบการเชื่อมต่อกับ ADLS </span><span class="sxs-lookup"><span data-stu-id="9fa95-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="9fa95-128">ทดสอบการเชื่อมต่อกับ KeyVault โดยใช้ลิงก์ **ทดสอบ Azure Key Vault**</span><span class="sxs-lookup"><span data-stu-id="9fa95-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="9fa95-129">ทดสอบการเชื่อมต่อกับ ADLS โดยใช้ลิงก์ **ทดสอบที่เก็บข้อมูล Azure**</span><span class="sxs-lookup"><span data-stu-id="9fa95-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="9fa95-130">หากการทดสอบไม่ประสบผลสำเร็จ ตรวจสอบอีกครั้งว่าข้อมูล KeyVault ทั้งหมดที่เพิ่มข้างต้นถูกต้อง จากนั้นลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9fa95-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="9fa95-131">เมื่อการทดสอบการเชื่อมต่อสำเร็จ คุณต้องเปิดใช้งานการรีเฟรชอัตโนมัติสำหรับที่เก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9fa95-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="9fa95-132">เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9fa95-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="9fa95-133">ค้นหา **ที่เก็บเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="9fa95-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="9fa95-134">ในรายการด้านซ้าย นำทางไปยังรายการ **RetailSales** และเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9fa95-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="9fa95-135">ตรวจสอบให้แน่ใจว่า **ได้เปิดใช้งานการรีเฟรชอัตโนมัติ** ซึ่งถูกตั้งค่าเป็น **ใช่** เลือก **รีเฟรช** แล้วจึงเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9fa95-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="9fa95-136">เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้ รูปภาพต่อไปนี้แสดงตัวอย่างของที่เก็บเอนทิตีพร้อมกับการเปิดใช้งานการรีเฟรชอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9fa95-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![ตัวอย่างของที่เก็บเอนทิตีที่เปิดใช้งานการรีเฟรชอัตโนมัติ](./media/exampleADLSConfig2.png)

<span data-ttu-id="9fa95-138">ขณะนี้ ADLS ได้รับการกำหนดค่าสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9fa95-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="9fa95-139">หากยังไม่เสร็จสิ้น ให้ทำตามขั้นตอนสำหรับ [การเปิดใช้งานคำแนะนำผลิตภัณฑ์และการตั้งค่าส่วนบุคคล](enable-product-recommendations.md) สำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9fa95-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fa95-140">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9fa95-140">Additional resources</span></span>

[<span data-ttu-id="9fa95-141">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9fa95-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9fa95-142">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9fa95-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9fa95-143">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9fa95-143">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9fa95-144">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9fa95-144">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9fa95-145">เพิ่มรายการคำแนะนำลงในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="9fa95-145">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="9fa95-146">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="9fa95-146">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9fa95-147">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9fa95-147">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9fa95-148">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="9fa95-148">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9fa95-149">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9fa95-149">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9fa95-150">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="9fa95-150">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9fa95-151">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9fa95-151">Product recommendations FAQ</span></span>](faq-recommendations.md)


