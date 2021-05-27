---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 873266405638cd277eb748ad7e966ba8a4976b13
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019870"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="95d83-103">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="95d83-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95d83-104">หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95d83-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="95d83-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="95d83-106">การตรวจสอบคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="95d83-106">Recommendations pre-check</span></span>

<span data-ttu-id="95d83-107">ก่อนการเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้า Commerce ที่โอนย้ายที่เก็บข้อมูลของตนไปโดยใช้ Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="95d83-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="95d83-108">ต้องเปิดใช้งานการตั้งค่าคอนฟิกต่อไปนี้ในฝ่ายสนับสนุนก่อนเปิดใช้งานคำแนะนำ:</span><span class="sxs-lookup"><span data-stu-id="95d83-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="95d83-109">ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="95d83-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="95d83-110">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการซื้อ Azure Data Lake Storage และตรวจสอบความถูกต้องในสภาพแวดล้อมเรียบร้อยแล้ว](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="95d83-111">ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="95d83-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="95d83-112">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตรวจสอบให้แน่ใจว่ามีการรีเฟรชที่จัดเก็บเอนทิตี้โดยอัตโนมัติ](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="95d83-113">ยืนยันว่าการตั้งค่าคอนฟิกข้อมูลเฉพาะตัว Azure AD มีรายการสำหรับคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="95d83-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="95d83-114">ข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดำเนินการนี้อยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="95d83-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="95d83-115">นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว</span><span class="sxs-lookup"><span data-stu-id="95d83-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="95d83-116">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ ให้ดูที่ [การทำงานกับการวัด](/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="95d83-116">To learn more about this set up process, see [Work with measures](/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="95d83-117">การตั้งค่าคอนฟิกข้อมูลประจำตัวของ Azure AD</span><span class="sxs-lookup"><span data-stu-id="95d83-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="95d83-118">ขั้นตอนนี้จำเป็นสำหรับลูกค้าทั้งหมดที่ใช้โครงสร้างแบบอินฟราเรดเป็นการตั้งค่าคอนฟิกการบริการ (IaaS)</span><span class="sxs-lookup"><span data-stu-id="95d83-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="95d83-119">สำหรับลูกค้าที่ทำงานบน Service Fabric (SF) ขั้นตอนนี้ควรเป็นแบบอัตโนมัติ และเราขอแนะนำให้ตรวจสอบว่ามีการตั้งค่าคอนฟิกการตั้งค่าตามที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="95d83-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="95d83-120">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="95d83-120">Setup</span></span>

1. <span data-ttu-id="95d83-121">จากฝ่ายสนับสนุน ให้ค้นหาหน้า **แอปพลิเคชัน Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="95d83-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="95d83-122">ตรวจสอบว่ามีรายการสำหรับ "RecommendationSystemApplication-1" หรือไม่</span><span class="sxs-lookup"><span data-stu-id="95d83-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="95d83-123">ถ้าไม่มีรายการอยู่ ให้เพิ่มรายการใหม่ที่มีข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95d83-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="95d83-124">**รหัสไคลเอนต์ ASP** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="95d83-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="95d83-125">**ชื่อ** - RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="95d83-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="95d83-126">**รหัสผู้ใช้** - RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="95d83-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="95d83-127">บันทึกและปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="95d83-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="95d83-128">เปิดคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="95d83-128">Turn on recommendations</span></span>

<span data-ttu-id="95d83-129">ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="95d83-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="95d83-130">ในศูนย์ควบคุม Commerce ให้ค้นหา **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="95d83-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="95d83-131">เลือก **ทั้งหมด** เพื่อดูรายการของคุณลักษณะที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="95d83-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="95d83-132">ในกล่องค้นหา ให้ป้อน **คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="95d83-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="95d83-133">เลือกคุณลักษณะ **คำแนะนำผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="95d83-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="95d83-134">ในบานหน้าต่างคุณสมบัติ **คำแนะนำผลิตภัณฑ์** ให้เลือก **เปิดใช้งานเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="95d83-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![กำลังเปิดคำแนะนำ](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="95d83-136">ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="95d83-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="95d83-137">อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95d83-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="95d83-138">ตั้งค่าพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="95d83-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="95d83-139">โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="95d83-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="95d83-140">คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="95d83-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="95d83-141">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="95d83-142">แสดงคำแนะนำบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="95d83-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="95d83-143">หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="95d83-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="95d83-144">หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="95d83-145">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="95d83-145">Enable personalized recommendations</span></span>

<span data-ttu-id="95d83-146">ใน Dynamics 365 Commerce ผู้ค้าปลีกสามารถทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งาน (หรืออีกชื่อหนึ่งว่า การตั้งค่าส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="95d83-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="95d83-147">ด้วยวิธีนี้ คำแนะนำแบบส่วนตัวสามารถรวมเข้ากับประสบการณ์ของลูกค้าออนไลน์และในระบบขายหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="95d83-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="95d83-148">เมื่อเปิดใช้งานฟังก์ชั่นการตั้งค่าส่วนบุคคล ระบบจะสามารถเชื่อมโยงข้อมูลการซื้อและผลิตภัณฑ์ของผู้ใช้เพื่อสร้างคำแนะนำผลิตภัณฑ์เฉพาะบุคคล</span><span class="sxs-lookup"><span data-stu-id="95d83-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="95d83-149">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคำแนะนำแบบส่วนตัว โปรดดูที่ [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="95d83-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95d83-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="95d83-150">Additional resources</span></span>

[<span data-ttu-id="95d83-151">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="95d83-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="95d83-152">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="95d83-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="95d83-153">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="95d83-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="95d83-154">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="95d83-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="95d83-155">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="95d83-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="95d83-156">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="95d83-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="95d83-157">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="95d83-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="95d83-158">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="95d83-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="95d83-159">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="95d83-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="95d83-160">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="95d83-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="95d83-161">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="95d83-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]