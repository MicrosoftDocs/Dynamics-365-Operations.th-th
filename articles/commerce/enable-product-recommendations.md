---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259805"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="bbea5-103">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bbea5-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bbea5-104">หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bbea5-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="bbea5-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="bbea5-106">การตรวจสอบคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bbea5-106">Recommendations pre-check</span></span>

<span data-ttu-id="bbea5-107">ก่อนเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้า Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปใช้ Azure Data Lake Storage (ADLS) </span><span class="sxs-lookup"><span data-stu-id="bbea5-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="bbea5-108">ต้องเปิดใช้งานการตั้งค่าคอนฟิกต่อไปนี้ในฝ่ายสนับสนุนก่อนเปิดใช้งานคำแนะนำ:</span><span class="sxs-lookup"><span data-stu-id="bbea5-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="bbea5-109">ตรวจสอบให้แน่ใจว่ามีการซื้อ ADLS และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="bbea5-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="bbea5-110">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการซื้อ ADLS และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="bbea5-111">ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bbea5-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="bbea5-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="bbea5-113">ยืนยันว่าการตั้งค่าคอนฟิกข้อมูลเฉพาะตัว Azure AD มีรายการสำหรับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bbea5-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="bbea5-114">ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดำเนินการนี้อยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="bbea5-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="bbea5-115">นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว</span><span class="sxs-lookup"><span data-stu-id="bbea5-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="bbea5-116">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ ให้ดูที่ [การทำงานกับการวัด](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="bbea5-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="bbea5-117">การตั้งค่าคอนฟิกข้อมูลประจำตัวของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="bbea5-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="bbea5-118">ขั้นตอนนี้จำเป็นสำหรับลูกค้าทั้งหมดที่ใช้โครงสร้างแบบอินฟราเรดเป็นการตั้งค่าคอนฟิกการบริการ (IaaS)</span><span class="sxs-lookup"><span data-stu-id="bbea5-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="bbea5-119">สำหรับลูกค้าที่ทำงานบน Service Fabric (SF) ขั้นตอนนี้ควรเป็นแบบอัตโนมัติ และเราขอแนะนำให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการตั้งค่าตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="bbea5-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="bbea5-120">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="bbea5-120">Setup</span></span>

1. <span data-ttu-id="bbea5-121">จากฝ่ายสนับสนุน ให้ค้นหาหน้า **แอปพลิเคชัน Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="bbea5-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="bbea5-122">ตรวจสอบว่ามีรายการสำหรับ "RecommendationSystemApplication-1" หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bbea5-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="bbea5-123">ถ้าไม่มีรายการอยู่ ให้เพิ่มรายการใหม่ที่มีข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="bbea5-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="bbea5-124">**รหัสไคลเอนต์ ASP** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="bbea5-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="bbea5-125">**ชื่อ** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="bbea5-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="bbea5-126">**รหัสผู้ใช้** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="bbea5-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="bbea5-127">บันทึกและปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bbea5-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="bbea5-128">เปิดคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bbea5-128">Turn on recommendations</span></span>

<span data-ttu-id="bbea5-129">ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="bbea5-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="bbea5-130">ไปยัง **การขายปลีกและการค้า &gt; คำแนะนำผลิตภัณฑ์ &gt; พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="bbea5-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="bbea5-131">ในรายการของพารามิเตอร์ที่ใช้ร่วมกัน ให้เลือก **รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="bbea5-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="bbea5-132">ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="bbea5-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![กำลังเปิดคำแนะนำ](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="bbea5-134">ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bbea5-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="bbea5-135">อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bbea5-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="bbea5-136">ตั้งค่าพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="bbea5-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="bbea5-137">โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="bbea5-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="bbea5-138">คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="bbea5-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="bbea5-139">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="bbea5-140">แสดงคำแนะนำบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="bbea5-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="bbea5-141">หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="bbea5-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="bbea5-142">หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="bbea5-143">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="bbea5-143">Enable personalized recommendations</span></span>

<span data-ttu-id="bbea5-144">ใน Dynamics 365 Commerce ผู้ค้าปลีกสามารถทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งาน (หรืออีกชื่อหนึ่งว่า การตั้งค่าส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="bbea5-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="bbea5-145">ด้วยวิธีนี้ คำแนะนำแบบส่วนตัวสามารถรวมเข้ากับประสบการณ์ของลูกค้าออนไลน์และในระบบขายหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="bbea5-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="bbea5-146">เมื่อเปิดใช้งานฟังก์ชั่นการตั้งค่าส่วนบุคคล ระบบจะสามารถเชื่อมโยงข้อมูลการซื้อและผลิตภัณฑ์ของผู้ใช้เพื่อสร้างคำแนะนำผลิตภัณฑ์เฉพาะบุคคล</span><span class="sxs-lookup"><span data-stu-id="bbea5-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="bbea5-147">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคำแนะนำแบบส่วนตัว โปรดดูที่ [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="bbea5-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbea5-148">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bbea5-148">Additional resources</span></span>

[<span data-ttu-id="bbea5-149">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bbea5-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="bbea5-150">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bbea5-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="bbea5-151">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="bbea5-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="bbea5-152">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="bbea5-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="bbea5-153">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="bbea5-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="bbea5-154">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bbea5-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="bbea5-155">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="bbea5-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="bbea5-156">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="bbea5-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="bbea5-157">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="bbea5-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="bbea5-158">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bbea5-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

