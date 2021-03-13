---
title: เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c10802d66ba9e241a042cc1a0bba01457da20126
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010110"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="9c6c5-103">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9c6c5-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c6c5-104">หัวข้อนี้อธิบายวิธีเปิดใช้งานและทดสอบ Azure Data Lake Storage สำหรับสภาพแวดล้อม Dynamics 365 Commerce ซึ่งเป็นข้อกำหนดเบื้องต้นสำหรับการเปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c6c5-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="9c6c5-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-105">Overview</span></span>

<span data-ttu-id="9c6c5-106">ในโซลูชัน Dynamics 365 Commerce ข้อมูลผลิตภัณฑ์และธุรกรรมทั้งหมดจะถูกติดตามในที่เก็บเอนทิตีของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="9c6c5-107">เพื่อทำให้ข้อมูลนี้สามารถเข้าถึงได้จากบริการอื่นๆ ของ Dynamics 365 เช่น การวิเคราะห์ข้อมูล ข่าวกรองทางธุรกิจ และคำแนะนำแบบส่วนตัว จึงจำเป็นต้องเชื่อมต่อสภาพแวดล้อมกับโซลูชัน Azure Data Lake Storage Gen 2 ที่เป็นของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c6c5-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="9c6c5-108">เนื่องจาก Azure Data Lake Storage ถูกตั้งค่าคอนฟิกในสภาพแวดล้อม ข้อมูลที่จำเป็นทั้งหมดจะถูกสะท้อนจากที่เก็บเอนทิตี ในขณะที่ยังคงได้รับการป้องกันและอยู่ภายใต้การควบคุมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c6c5-108">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="9c6c5-109">นอกจากนี้ หากมีการเปิดใช้งานคำแนะนำผลิตภัณฑ์หรือคำแนะนำแบบส่วนตัวในสภาพแวดล้อมด้วยแล้ว สแต็คคำแนะนำผลิตภัณฑ์จะได้รับสิทธิ์การเข้าถึงโฟลเดอร์เฉพาะใน Azure Data Lake Storage เพื่อดึงข้อมูลของลูกค้าและคำนวณคำแนะนำตามข้อมูลนั้น</span><span class="sxs-lookup"><span data-stu-id="9c6c5-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9c6c5-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9c6c5-110">Prerequisites</span></span>

<span data-ttu-id="9c6c5-111">ลูกค้าจำเป็นต้องตั้งค่าคอนฟิก Azure Data Lake Storage ในการสมัครใช้งาน Azure ที่พวกเขาเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="9c6c5-111">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="9c6c5-112">หัวข้อนี้ไม่ครอบคลุมการซื้อของการสมัครใช้งาน Azure หรือการตั้งค่าของบัญชีที่เก็บข้อมูลที่เปิดใช้งาน Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="9c6c5-112">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="9c6c5-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Azure Data Lake Storage ดู [เอกสารประกอบอย่างเป็นทางการของ Azure Data Lake Storage Gen2](https://azure.microsoft.com/pricing/details/storage/data-lake)</span><span class="sxs-lookup"><span data-stu-id="9c6c5-113">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="9c6c5-114">ขั้นตอนการกำหนดค่า </span><span class="sxs-lookup"><span data-stu-id="9c6c5-114">Configuration steps</span></span>

<span data-ttu-id="9c6c5-115">ส่วนนี้ครอบคลุมขั้นตอนการตั้งค่าคอนฟิกที่จำเป็นสำหรับการเปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม เนื่องจากเกี่ยวข้องกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c6c5-115">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="9c6c5-116">สำหรับภาพรวมเชิงลึกเพิ่มเติมเกี่ยวกับขั้นตอนต่างๆ ที่จำเป็นในการเปิดใช้งาน Azure Data Lake Storage ให้ดูที่ [ทำให้ที่จัดเก็บเอนทิตีพร้อมใช้งานเป็น Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)</span><span class="sxs-lookup"><span data-stu-id="9c6c5-116">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="9c6c5-117">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-117">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="9c6c5-118">ล็อกอินเข้าสู่พอร์ทัลสนับสนุนของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="9c6c5-119">ค้นหา **พารามิเตอร์ระบบ** และนำทางไปที่แท็บ **การเชื่อมโยงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="9c6c5-120">ตั้งค่า **เปิดใช้งานการรวม Data Lake** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="9c6c5-121">ตั้งค่า **เปิดใช้งานการปรับปรุงทริกเกิล Data Lake** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="9c6c5-122">จากนั้นป้อนข้อมูลที่จำเป็นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9c6c5-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="9c6c5-123">**รหัสแอปพลิเคชัน** // **ข้อมูลลับของแอปพลิเคชัน** // **ชื่อ DNS** - จำเป็นต้องเชื่อมต่อกับ KeyVault ที่ซึ่งข้อมูลลับ Azure Data Lake Storage ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="9c6c5-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="9c6c5-124">**ชื่อลับ** - ชื่อลับที่เก็บไว้ใน KeyVault และใช้เพื่อรับรองความถูกต้องกับ Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="9c6c5-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="9c6c5-125">บันทึกการเปลี่ยนแปลงของคุณในหน้าที่อยู่มุมบนซ้าย</span><span class="sxs-lookup"><span data-stu-id="9c6c5-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="9c6c5-126">ภาพต่อไปนี้แสดงการตั้งค่าคอนฟิก Azure Data Lake Storage ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="9c6c5-126">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![ตัวอย่างของการตั้งค่าคอนฟิก Azure Data Lake Storage](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="9c6c5-128">ทดสอบการเชื่อมต่อ Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="9c6c5-128">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="9c6c5-129">ทดสอบการเชื่อมต่อกับ KeyVault โดยใช้ลิงก์ **ทดสอบ Azure Key Vault**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="9c6c5-130">ทดสอบการเชื่อมต่อกับ Azure Data Lake Storage โดยใช้ลิงก์ **ทดสอบที่เก็บข้อมูล Azure**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-130">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="9c6c5-131">หากการทดสอบไม่ประสบผลสำเร็จ ตรวจสอบอีกครั้งว่าข้อมูล KeyVault ทั้งหมดที่เพิ่มข้างต้นถูกต้อง จากนั้นลองอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="9c6c5-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="9c6c5-132">เมื่อการทดสอบการเชื่อมต่อสำเร็จ คุณต้องเปิดใช้งานการรีเฟรชอัตโนมัติสำหรับที่เก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9c6c5-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="9c6c5-133">เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9c6c5-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="9c6c5-134">ค้นหา **ที่เก็บเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="9c6c5-135">ในรายการด้านซ้าย นำทางไปยังรายการ **RetailSales** และเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="9c6c5-136">ตรวจสอบให้แน่ใจว่า **ได้เปิดใช้งานการรีเฟรชอัตโนมัติ** ซึ่งถูกตั้งค่าเป็น **ใช่** เลือก **รีเฟรช** แล้วจึงเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9c6c5-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="9c6c5-137">เพื่อเปิดใช้งานที่เก็บเอนทิตีสำหรับการรีเฟรชอัตโนมัติ ให้ทำตามขั้นตอนเหล่านี้ รูปภาพต่อไปนี้แสดงตัวอย่างของที่เก็บเอนทิตีพร้อมกับการเปิดใช้งานการรีเฟรชอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9c6c5-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![ตัวอย่างของที่เก็บเอนทิตีที่เปิดใช้งานการรีเฟรชอัตโนมัติ](./media/exampleADLSConfig2.png)

<span data-ttu-id="9c6c5-139">Azure Data Lake Storage ขณะนี้ถูกตั้งค่าคอนฟิกสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-139">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="9c6c5-140">หากยังไม่เสร็จสิ้น ให้ทำตามขั้นตอนสำหรับ [การเปิดใช้งานคำแนะนำผลิตภัณฑ์และการตั้งค่าส่วนบุคคล](enable-product-recommendations.md) สำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c6c5-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-141">Additional resources</span></span>

[<span data-ttu-id="9c6c5-142">ทำให้ที่จัดเก็บเอนทิตี้พร้อมใช้งานเป็น Data Lake</span><span class="sxs-lookup"><span data-stu-id="9c6c5-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="9c6c5-143">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c6c5-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9c6c5-144">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c6c5-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9c6c5-145">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9c6c5-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9c6c5-146">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9c6c5-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9c6c5-147">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="9c6c5-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9c6c5-148">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="9c6c5-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9c6c5-149">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9c6c5-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9c6c5-150">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="9c6c5-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9c6c5-151">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9c6c5-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9c6c5-152">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="9c6c5-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9c6c5-153">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9c6c5-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
