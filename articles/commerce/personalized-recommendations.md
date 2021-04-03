---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์แบบส่วนตัว
description: หัวข้อนี้อธิบายวิธีวิธีทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งานสำหรับลูกค้าใน Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.openlocfilehash: be460ec5ce8a9a625dc1a80f761bea9e2ab2f632
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477671"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="be5eb-103">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="be5eb-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be5eb-104">หัวข้อนี้อธิบายวิธีวิธีทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งานสำหรับลูกค้าใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="be5eb-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="be5eb-105">ใน Dynamics 365 Commerce ผู้ค้าปลีกสามารถทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวพร้อมใช้งาน (หรืออีกชื่อหนึ่งว่า การตั้งค่าส่วนบุคคล)</span><span class="sxs-lookup"><span data-stu-id="be5eb-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="be5eb-106">ด้วยวิธีนี้ คำแนะนำแบบส่วนตัวสามารถรวมเข้ากับประสบการณ์ของลูกค้าออนไลน์และในระบบขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="be5eb-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="be5eb-107">เมื่อเปิดใช้งานฟังก์ชั่นการตั้งค่าส่วนบุคคล ระบบจะสามารถเชื่อมโยงข้อมูลการซื้อและผลิตภัณฑ์ของผู้ใช้เพื่อสร้างคำแนะนำผลิตภัณฑ์เฉพาะบุคคล</span><span class="sxs-lookup"><span data-stu-id="be5eb-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="be5eb-108">ข้อกำหนดเบื้องต้นในการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="be5eb-108">Personalization prerequisites</span></span>

<span data-ttu-id="be5eb-109">ก่อนที่คุณจะทำให้คำแนะนำผลิตภัณฑ์แบบส่วนตัวมีพร้อมใช้งานสำหรับลูกค้า ให้สังเกตว่าคำแนะนำได้รับการสนับสนุนเฉพาะสำหรับลูกค้าเชิงพาณิชย์ที่โอนย้ายที่เก็บข้อมูลของตนไปยัง Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="be5eb-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="be5eb-110">ก่อนที่ลูกค้าจะสามารถรับคำแนะนำผลิตภัณฑ์แบบส่วนตัว ผู้ค้าปลีกจะต้อง [เปิดใช้งานคำแนะนำผลิตภัณฑ์](enable-product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="be5eb-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="be5eb-111">เมื่อเปิดคำแนะนำผลิตภัณฑ์ คุณจะเปิดใช้การตั้งค่าส่วนบุคคลด้วย</span><span class="sxs-lookup"><span data-stu-id="be5eb-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="be5eb-112">อย่างไรก็ตาม หากคุณปิดการตั้งค่าส่วนบุคคล คุณจะไม่ได้ปิดคำแนะนำผลิตภัณฑ์ชนิดอื่น</span><span class="sxs-lookup"><span data-stu-id="be5eb-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="be5eb-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ ดู [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="be5eb-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="be5eb-114">เปิดการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="be5eb-114">Turn on personalization</span></span>

<span data-ttu-id="be5eb-115">หากต้องการเปิดการตั้งค่าส่วนบุคคล ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="be5eb-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="be5eb-116">ในศูนย์ควบคุม Commerce ให้ค้นหา **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="be5eb-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="be5eb-117">เลือก **ทั้งหมด** เพื่อดูรายการของคุณลักษณะที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="be5eb-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="be5eb-118">ในกล่องค้นหา ให้ป้อน **คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="be5eb-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="be5eb-119">เลือกคุณลักษณะ **คำแนะนำผลิตภัณฑ์แบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="be5eb-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="be5eb-120">ในบานหน้าต่างคุณสมบัติ **คำแนะนำผลิตภัณฑ์แบบส่วนบุคคล** ให้เลือก **เปิดใช้งานเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="be5eb-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![เปิดการตั้งค่าส่วนบุคคล](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="be5eb-122">เมื่อคุณเปิดการตั้งค่าส่วนบุคคล จะเป็นการเริ่มกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์แบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="be5eb-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="be5eb-123">อาจต้องใช้เวลาสูงสุดหนึ่งวัน ก่อนที่รายการเหล่านี้จะพร้อมใช้งานและสามารถมองเห็นได้ทางออนไลน์และที่ POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="be5eb-124">รายการที่ปรับให้เป็นแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="be5eb-124">Personalized lists</span></span>

<span data-ttu-id="be5eb-125">นอกเหนือจากการอนุญาตให้มีการตั้งค่าส่วนบุคคลสำหรับรายการที่สร้างจากเครื่องที่มีอยู่แล้ว การบริการคำแนะนำยังอนุญาตให้มีการตั้งค่าส่วนบุคคลสำหรับประสบการณ์การค้นพบผลิตภัณฑ์ทั้งแบบออนไลน์และที่ POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="be5eb-126">หลังจากเปิดใช้งานการตั้งค่าส่วนบุคคล ผู้ค้าปลีกสามารถแสดงรายการออนไลน์ "เลือกให้คุณ" ให้กับผู้ซื้อในแบบส่วนตัว หรือรายการ "คำแนะนำสำหรับลูกค้า" ในเทอร์มินัล POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="be5eb-127">นอกจากนี้ ผู้ค้าปลีกสามารถใช้การตั้งค่าส่วนบุคคลให้กับรายการคำแนะนำผลิตภัณฑ์ที่มีอยู่ และมอบประสบการณ์ในการเลือกปฏิเสธข้อบังคับทั่วไปเกี่ยวกับการคุ้มครองข้อมูล (GDPR) สำหรับผู้ใช้ที่ได้รับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="be5eb-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="be5eb-128">หากคุณปิดการตั้งค่าส่วนบุคคล คุณจะต้องปิดคุณลักษณะเหล่านี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="be5eb-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="be5eb-129">รายการ "เลือกให้คุณ" ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="be5eb-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="be5eb-130">รายการ "เลือกให้คุณ" เป็นรายการการเรียนรู้เกี่ยวกับเครื่องปัญญาประดิษฐ์​ (AI-ML) ที่แสดงรายการแบบส่วนตัวของผลิตภัณฑ์ที่แนะนำให้ผู้ใช้ที่ผ่านการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="be5eb-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="be5eb-131">รายการนี้ขึ้นอยู่กับประวัติการซื้อของผู้ใช้ช่องทาง Omni </span><span class="sxs-lookup"><span data-stu-id="be5eb-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="be5eb-132">คำแนะนำแบบส่วนตัวจะได้รับการปรับปรุงแบบไดนามิกในขณะที่ผู้ใช้ทำการสั่งซื้อมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="be5eb-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="be5eb-133">รายการชนิดนี้ยังสนับสนุนการกรองประเภท เพื่อให้ผู้ค้าปลีกสามารถแสดงตัวเลือกยอดนิยมยึดตามลำดับชั้นของการนำทาง</span><span class="sxs-lookup"><span data-stu-id="be5eb-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="be5eb-134">ก่อนรายการ "เลือกให้คุณ" สามารถปรากฏบนหน้า e-Commerce ใด ๆ ข้อกำหนดของผู้ใช้ต่อไปนี้จะต้องตรงกัน:</span><span class="sxs-lookup"><span data-stu-id="be5eb-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="be5eb-135">ผู้ใช้จะต้องเข้าสู่ระบบ</span><span class="sxs-lookup"><span data-stu-id="be5eb-135">Users must be signed in.</span></span> <span data-ttu-id="be5eb-136">ผู้ใช้ที่ไม่ระบุชื่อจะไม่เห็นคำแนะนำแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="be5eb-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="be5eb-137">ผู้ใช้ต้องมีการซื้ออย่างน้อยหนึ่งครั้งในบัญชีของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="be5eb-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="be5eb-138">ผู้ใช้จะต้องเข้าร่วมเพื่อรับคำแนะนำแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="be5eb-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="be5eb-139">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายการ "เลือกให้คุณ" บนหน้าร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="be5eb-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![รายการ "เลือกให้คุณ" ออนไลน์](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="be5eb-141">รายการ "คำแนะนำสำหรับลูกค้า" ที่ POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="be5eb-142">เพื่อเสริมสร้างประสบการณ์การใช้งานของลูกค้า ผู้ค้าปลีกสามารถปรับแต่งหน้าหน้ารายละเอียดลูกค้าที่มีอยู่แบบส่วนตัวได้ โดยเพิ่มรายการ "คำแนะนำสำหรับลูกค้า" ตามบริบท</span><span class="sxs-lookup"><span data-stu-id="be5eb-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="be5eb-143">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายการ "คำแนะนำสำหรับลูกค้า" บนเทอร์มินัล POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![รายการ "คำแนะนำสำหรับลูกค้า" ที่ POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="be5eb-145">ใช้การตั้งค่าส่วนบุคคลกับรายการคำแนะนำที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="be5eb-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="be5eb-146">ผู้ค้าปลีกสามารถใช้การตั้งค่าส่วนบุคคลกับรายการคำแนะนำที่มีอยู่ เช่น "ใหม่" "ได้รับความนิยม" "ขายดีที่สุด" "ผู้คนยังถูกใจ" และ "ซื้อด้วยกันบ่อย"</span><span class="sxs-lookup"><span data-stu-id="be5eb-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="be5eb-147">เมื่อมีการใช้การตั้งค่าส่วนบุคคลกับรายการที่มีอยู่ รายการที่ผู้ใช้ลงชื่อเข้าใช้ที่ซื้อก่อนหน้านี้จะถูกลบออกจากรายการเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="be5eb-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="be5eb-148">สำหรับผู้ใช้ที่ไม่ระบุชื่อและผู้ใช้ที่ไม่ได้รับคำแนะนำแบบส่วนตัวจะมีการแสดงรุ่นเริ่มต้นของรายการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="be5eb-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="be5eb-149">ดังนั้น ผู้ค้าปลีกไม่จำเป็นต้องรักษาประสบการณ์การใช้หน้าที่แยกต่างหากด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="be5eb-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="be5eb-150">ตัวอย่างเช่น ผู้ใช้ที่ลงชื่อเข้าใช้ซื้อนาฬิกาสีดำแล้ว และรองเท้าบูทสีน้ำตาลที่ปรากฏในรายการ "เป็นที่นิยม - ค่าเริ่มต้น" ในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="be5eb-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="be5eb-151">ดังนั้นผู้ใช้จะเห็นผลิตภัณฑ์ใหม่แทนที่จะเป็นผลิตภัณฑ์เหล่านั้นดังที่แสดงในรายการ "เป็นที่นิยม - ปรับให้เป็นแบบส่วนตัว"</span><span class="sxs-lookup"><span data-stu-id="be5eb-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![ใช้งานการตั้งค่าส่วนบุคคล](./media/applypersonalization.png)

<span data-ttu-id="be5eb-153">เมื่อต้องการใช้การใช้งานการตั้งค่าส่วนบุคคลกับรายการคำแนะนำที่มีอยู่ในเครื่องมือสร้างไซต์การค้า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="be5eb-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="be5eb-154">เปิดหน้าตัวสร้างไซต์ที่มีอยู่ซึ่งมีโมดูลกลุ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="be5eb-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="be5eb-155">ในหน้าต่างการนำทางทางด้านซ้าย เลือกโมดูลกลุ่มผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="be5eb-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="be5eb-156">ในบานหน้าต่างการนำทางด้านขวา ใต้ **ผลิตภัณฑ์** เลือกรายการ </span><span class="sxs-lookup"><span data-stu-id="be5eb-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="be5eb-157">ในกล่องโต้ตอบ **เลือกการกำหนดค่ารายการผลิตภัณฑ์** ภายใต้ **ชนิด** ให้เลือกชนิดรายการ</span><span class="sxs-lookup"><span data-stu-id="be5eb-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="be5eb-158">เลือกกล่องกาเครื่องหมาย **ใช้การตั้งค่าส่วนบุคคล** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="be5eb-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![ใช้งานการตั้งค่าส่วนบุคคลกับรายการที่เป็นที่นิยม](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="be5eb-160">บันทึกหน้า แก้ไขให้เสร็จสิ้น แล้วจึงเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="be5eb-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="be5eb-161">หลังจากเผยแพร่หน้านี้แล้ว ผู้ใช้ที่ลงชื่อเข้าใช้จะเห็นรายการที่เป็นที่นิยมแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="be5eb-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be5eb-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="be5eb-162">Additional resources</span></span>

[<span data-ttu-id="be5eb-163">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="be5eb-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="be5eb-164">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="be5eb-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="be5eb-165">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="be5eb-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="be5eb-166">เปิดใช้งานคำแนะนำ "เลือกซื้อสินค้าที่คล้ายกัน"</span><span class="sxs-lookup"><span data-stu-id="be5eb-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="be5eb-167">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="be5eb-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="be5eb-168">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="be5eb-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="be5eb-169">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="be5eb-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="be5eb-170">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="be5eb-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="be5eb-171">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="be5eb-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="be5eb-172">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="be5eb-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="be5eb-173">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="be5eb-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
