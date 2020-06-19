---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 694e5a451b8e25f3729364dfaed0adc7d242f2fe
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404220"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="d01e0-103">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d01e0-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d01e0-104">หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d01e0-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="d01e0-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="d01e0-106">การตรวจสอบคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="d01e0-106">Recommendations pre-check</span></span>

<span data-ttu-id="d01e0-107">ก่อนการเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้า Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปโดยใช้ Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="d01e0-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="d01e0-108">ต้องเปิดใช้งานการตั้งค่าคอนฟิกต่อไปนี้ในฝ่ายสนับสนุนก่อนเปิดใช้งานคำแนะนำ:</span><span class="sxs-lookup"><span data-stu-id="d01e0-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="d01e0-109">ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="d01e0-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="d01e0-110">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="d01e0-111">ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d01e0-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="d01e0-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="d01e0-113">ยืนยันว่าการตั้งค่าคอนฟิกข้อมูลเฉพาะตัว Azure AD มีรายการสำหรับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="d01e0-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="d01e0-114">ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดำเนินการนี้อยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="d01e0-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="d01e0-115">นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว</span><span class="sxs-lookup"><span data-stu-id="d01e0-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="d01e0-116">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ ให้ดูที่ [การทำงานกับการวัด](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="d01e0-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="d01e0-117">การตั้งค่าคอนฟิกข้อมูลประจำตัวของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="d01e0-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="d01e0-118">ขั้นตอนนี้จำเป็นสำหรับลูกค้าทั้งหมดที่ใช้โครงสร้างแบบอินฟราเรดเป็นการตั้งค่าคอนฟิกการบริการ (IaaS)</span><span class="sxs-lookup"><span data-stu-id="d01e0-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="d01e0-119">สำหรับลูกค้าที่ทำงานบน Service Fabric (SF) ขั้นตอนนี้ควรเป็นแบบอัตโนมัติ และเราขอแนะนำให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการตั้งค่าตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="d01e0-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="d01e0-120">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="d01e0-120">Setup</span></span>

1. <span data-ttu-id="d01e0-121">จากฝ่ายสนับสนุน ให้ค้นหาหน้า **แอปพลิเคชัน Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="d01e0-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="d01e0-122">ตรวจสอบว่ามีรายการสำหรับ "RecommendationSystemApplication-1" หรือไม่</span><span class="sxs-lookup"><span data-stu-id="d01e0-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="d01e0-123">ถ้าไม่มีรายการอยู่ ให้เพิ่มรายการใหม่ที่มีข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d01e0-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="d01e0-124">**รหัสไคลเอนต์ ASP** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="d01e0-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="d01e0-125">**ชื่อ** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="d01e0-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="d01e0-126">**รหัสผู้ใช้** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="d01e0-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="d01e0-127">บันทึกและปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d01e0-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="d01e0-128">เปิดคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="d01e0-128">Turn on recommendations</span></span>

<span data-ttu-id="d01e0-129">ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d01e0-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="d01e0-130">ไปยัง **การขายปลีกและการค้า &gt; คำแนะนำผลิตภัณฑ์ &gt; พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="d01e0-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="d01e0-131">ในรายการของพารามิเตอร์ที่ใช้ร่วมกัน ให้เลือก **รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="d01e0-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="d01e0-132">ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="d01e0-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![กำลังเปิดคำแนะนำ](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="d01e0-134">ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d01e0-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="d01e0-135">อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d01e0-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="d01e0-136">ตั้งค่าพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="d01e0-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="d01e0-137">โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="d01e0-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="d01e0-138">คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="d01e0-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="d01e0-139">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="d01e0-140">แสดงคำแนะนำบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="d01e0-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="d01e0-141">หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="d01e0-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="d01e0-142">หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="d01e0-143">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="d01e0-143">Enable personalized recommendations</span></span>

<span data-ttu-id="d01e0-144">ใน Dynamics 365 Commerce ผู้ค้าปลีกสามารถทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งาน (หรืออีกชื่อหนึ่งว่า การตั้งค่าส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="d01e0-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="d01e0-145">ด้วยวิธีนี้ คำแนะนำแบบส่วนตัวสามารถรวมเข้ากับประสบการณ์ของลูกค้าออนไลน์และในระบบขายหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="d01e0-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="d01e0-146">เมื่อเปิดใช้งานฟังก์ชั่นการตั้งค่าส่วนบุคคล ระบบจะสามารถเชื่อมโยงข้อมูลการซื้อและผลิตภัณฑ์ของผู้ใช้เพื่อสร้างคำแนะนำผลิตภัณฑ์เฉพาะบุคคล</span><span class="sxs-lookup"><span data-stu-id="d01e0-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="d01e0-147">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคำแนะนำแบบส่วนตัว โปรดดูที่ [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="d01e0-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d01e0-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d01e0-148">Additional resources</span></span>

[<span data-ttu-id="d01e0-149">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d01e0-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d01e0-150">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d01e0-150">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d01e0-151">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="d01e0-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d01e0-152">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="d01e0-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d01e0-153">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="d01e0-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d01e0-154">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d01e0-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d01e0-155">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="d01e0-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d01e0-156">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d01e0-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d01e0-157">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="d01e0-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d01e0-158">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="d01e0-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

