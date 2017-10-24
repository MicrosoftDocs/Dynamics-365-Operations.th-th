---
title: "ภาพรวมคำแนะนำผลิตภัณฑ์แบบส่วนบุคคล"
description: "ใน Dynamics 365 for Retail สามารถแสดงคำแนะนำผลิตภัณฑ์บนอุปกรณ์ขายหน้าร้าน (POS) รายการแนะนำคือสินค้าที่ลูกค้าอาจสนใจโดยยึดตามของประวัติการซื้อของพวกเขา สินค้าในรายการสิ่งที่ต้องการของพวกเขา และสินค้าที่ลูกค้ารายอื่นซื้อแบบออนไลน์และในร้านค้าจริง สำหรับผู้ค้าปลีกที่มีแค็ตตาล็อกขนาดใหญ่ รายการแนะนำจะช่วยลูกค้าในการค้นหาผลิตภัณฑ์ โดยการแสดงผลิตภัณฑ์ที่ตรงกับความสนใจและพฤติกรรมการซื้อของลูกค้า คำแนะนำผลิตภัณฑ์จะช่วยผู้ค้าปลีกในการเพิ่มการขายและการขายสินค้าชนิดอื่น และสามารถเพิ่มเงินวางประกันของลูกค้าได้ ใน Dynamics 365 for Operations for Retail คำแนะนำผลิตภัณฑ์ได้รับการจัดการโดยบริการที่มีการรับรู้และ Machine Learning ของ Microsoft Azure"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="3b0bd-107">ภาพรวมคำแนะนำผลิตภัณฑ์แบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="3b0bd-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="3b0bd-108">คุณลักษณะนี้จะพร้อมใช้งานในโทโพโลยีการปรับใช้งาน sandbox และการผลิต (ความพร้อมใช้งานสูง) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b0bd-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="3b0bd-109">ใน Dynamics 365 for Retail สามารถแสดงคำแนะนำผลิตภัณฑ์บนอุปกรณ์ขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="3b0bd-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="3b0bd-110">รายการแนะนำคือสินค้าที่ลูกค้าอาจสนใจโดยยึดตามของประวัติการซื้อของพวกเขา สินค้าในรายการสิ่งที่ต้องการของพวกเขา และสินค้าที่ลูกค้ารายอื่นซื้อแบบออนไลน์และในร้านค้าจริง</span><span class="sxs-lookup"><span data-stu-id="3b0bd-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="3b0bd-111">สำหรับผู้ค้าปลีกที่มีแค็ตตาล็อกขนาดใหญ่ รายการแนะนำจะช่วยลูกค้าในการค้นหาผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3b0bd-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="3b0bd-112">โดยการแสดงผลิตภัณฑ์ที่ตรงกับความสนใจและพฤติกรรมการซื้อของลูกค้า คำแนะนำผลิตภัณฑ์จะช่วยผู้ค้าปลีกในการเพิ่มการขายและการขายสินค้าชนิดอื่น และสามารถเพิ่มเงินวางประกันของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="3b0bd-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="3b0bd-113">ใน Dynamics 365 for Operations for Retail คำแนะนำผลิตภัณฑ์ได้รับการจัดการโดยบริการที่มีการรับรู้และ Machine Learning ของ Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="3b0bd-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="3b0bd-114">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="3b0bd-114">Scenarios</span></span>
---------

<span data-ttu-id="3b0bd-115">คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b0bd-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="3b0bd-116">ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3b0bd-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="3b0bd-117">ในหน้า **รายละเอียดผลิตภัณฑ์** :</span><span class="sxs-lookup"><span data-stu-id="3b0bd-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="3b0bd-118">ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่าง ๆ กลไกจัดการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="3b0bd-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="3b0bd-119">ถ้าการเชื่อมโยงของร้านค้าเพิ่มลูกค้าลงในธุรกรรม และจากนั้น เยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** กลไกจัดการคำแนะนำจะให้คำแนะนำแบบส่วนบุคคลโดยใช้ประวัติธุรกรรมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b0bd-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="3b0bd-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="3b0bd-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="3b0bd-121">ในหน้า **ธุรกรรม** :</span><span class="sxs-lookup"><span data-stu-id="3b0bd-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="3b0bd-122">กลไกจัดการคำแนะนำจะแนะนำสินค้าตามรายการทั้งหมดของสินค้าในตะกร้า</span><span class="sxs-lookup"><span data-stu-id="3b0bd-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="3b0bd-123">ถ้าการเชื่อมโยงของร้านค้าเพิ่มลูกค้าลงในธุรกรรม และจากนั้น เยี่ยมชมหน้า รายละเอียดผลิตภัณฑ์ กลไกจัดการคำแนะนำจะให้คำแนะนำแบบส่วนบุคคลโดยใช้ประวัติธุรกรรมของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b0bd-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="3b0bd-124">เมื่อต้องการแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ค้าปลีกจะต้องอัพเดตโครงร่างหน้าจอใน Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="3b0bd-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="3b0bd-125">จะต้องปล่อยการควบคุม **คำแนะนำ** ลงในหน้า **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="3b0bd-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="3b0bd-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="3b0bd-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="3b0bd-127">ในหน้า **รายละเอียดลูกค้า** :</span><span class="sxs-lookup"><span data-stu-id="3b0bd-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="3b0bd-128">กลไกจัดการคำแนะนำจะแนะนำสินค้าตามรหัสผู้ใช้และสินค้าในรายการสิ่งที่ต้องการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3b0bd-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="3b0bd-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="3b0bd-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="3b0bd-130">ตั้งค่าคอนฟิก Dynamics 365 for Retail เพื่อเปิดใช้งานคำแนะนำของ POS</span><span class="sxs-lookup"><span data-stu-id="3b0bd-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="3b0bd-131">ถ้าต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ คุณต้องตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b0bd-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="3b0bd-132">ตรวจสอบให้แน่ใจว่าคุณได้เลือก **นิติบุคคล** ที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="3b0bd-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="3b0bd-133">นำทางไปยัง **ที่จัดเก็บเอนทิตี** เลือก **การขายปลีก** แล้วคลิก **รีเฟรช** ซึ่งจะใช้ข้อมูลสาธิต (หรือข้อมูลของคุณ) จากฐานข้อมูลการดำเนินงานของคุณ และย้ายไปยังที่จัดเก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="3b0bd-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="3b0bd-134">ไม่จำเป็น: เมื่อต้องการแสดงคำแนะนำบนหน้าจอธุรกรรม ไปที่ **โครงร่างหน้าจอ** เลือกโครงร่างหน้าจอของคุณ เปิดใช้ **ตัวออกแบบโครงร่างหน้าจอ** แล้วปล่อยการควบคุม **คำแนะนำ** เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="3b0bd-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="3b0bd-135">ไปที่ **พารามิเตอร์การขายปลีก** เลือก **Machine-learning** เลือก **ใช่** ภายใต้ **เปิดใช้งานคำแนะนำ POS**</span><span class="sxs-lookup"><span data-stu-id="3b0bd-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="3b0bd-136">เมื่อต้องการดูคำแนะนำบน POS เรียกใช้งานการตั้งค่าคอนฟิกส่วนกลาง **1110**</span><span class="sxs-lookup"><span data-stu-id="3b0bd-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="3b0bd-137">เมื่อต้องการเปลี่ยนแปลงในตัวออกแบบโครงร่างหน้าจอ POS เรียกใช้งานการตั้งค่าคอนฟิกช่องทาง **1070**</span><span class="sxs-lookup"><span data-stu-id="3b0bd-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="3b0bd-138">[]()สิ่งนี้ทำงานอย่างไร</span><span class="sxs-lookup"><span data-stu-id="3b0bd-138">[]()How does it work?</span></span>
<span data-ttu-id="3b0bd-139">เมื่อคุณรีเฟรชเอนทิตี **ที่จัดเก็บเอนทิตี** การดำเนินการต่อไปนี้จะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b0bd-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="3b0bd-140">ข้อมูลในรูปแบบที่กำหนดโดยบริการที่มีการรับรู้จะถูกแยกออกจาก Dynamics 365 for Retail สำหรับฐานข้อมูลในการดำเนินงาน และถูกส่งไปยังที่จัดเก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="3b0bd-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="3b0bd-141">ข้อมูลจะถูกใช้โดย Azure Data Factory (ADF) เพื่อลบข้อมูลโดยใช้สคริปต์ Hive โดยเป็นส่วนหนึ่งของกิจกรรม ADF</span><span class="sxs-lookup"><span data-stu-id="3b0bd-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="3b0bd-142">ข้อมูลที่ถูกลบข้อมูลแล้วจะถูกเก็บไว้ใน Blob Storage</span><span class="sxs-lookup"><span data-stu-id="3b0bd-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="3b0bd-143">ข้อมูลจาก Blob Storage จะถูกใช้โดย API บริการที่มีการรับรู้เพื่อฝึกแบบจำลองคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="3b0bd-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="3b0bd-144">เมื่อคุณเปิดใช้ **เปิดใช้งานคำแนะนำ** และเรียกใช้งานการตั้งค่าคอนฟิก การดำเนินการต่อไปนี้จะเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="3b0bd-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="3b0bd-145">ข้อมูลประจำตัวและรหัสแบบจำลองจะได้รับมาจาก API และจะถูกเก็บไว้ในฐานข้อมูลในการดำเนินการ Dynamics 365 for Retail ใน web.config สำหรับ AOS และในเซิร์ฟเวอร์การขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3b0bd-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="3b0bd-146">ข้อมูลประจำตัวและรหัสแบบจำลองจะพร้อมใช้งานสำหรับ CRT เพื่อให้สามารถจ่ายการเรียกใช้คำแนะนำผลิตภัณฑ์จาก Cloud POS and MPOS ในโหมดออนไลน์ได้</span><span class="sxs-lookup"><span data-stu-id="3b0bd-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="3b0bd-147">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3b0bd-147">See also</span></span>
--------

[<span data-ttu-id="3b0bd-148">เพิ่มตัวควบคุมคำแนะนำในหน้าธุรกรรมบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="3b0bd-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




