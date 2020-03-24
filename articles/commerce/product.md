---
title: เพิ่มคำแนะนำผลิตภัณฑ์ใน POS
description: หัวข้อนี้จะอธิบายถึงการใช้คำแนะนำผลิตภัณฑ์บนอุปกรณ์การขายหน้าร้าน (POS)
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127824"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="852c4-103">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="852c4-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="852c4-104">คามหลัก คำแนะนำผลิตภัณฑ์เป็นแอปพลิเคชันทางธุรกิจเพื่อการเปลี่ยนแปลงที่ครอบคลุมพื้นที่การค้าทั้งหมด เพื่อสร้างประสบการณ์การค้นพบผลิตภัณฑ์ที่หลากหลาย น่าดึงดูด และได้รับการปรับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="852c4-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="852c4-105">เมื่อต้องการใช้งานลักษณะการทำงานนี้บน[POS ให้ทำตามขั้นตอนเกี่ยวกับวิธีการเพิ่มข้อเสนอแนะให้กับอุปกรณ์ POS ของคุณ](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="852c4-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="852c4-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน  [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="852c4-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="852c4-107">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="852c4-107">Scenarios</span></span>

<span data-ttu-id="852c4-108">คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="852c4-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="852c4-109">ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="852c4-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="852c4-110">ในหน้า **รายละเอียดผลิตภัณฑ์** :</span><span class="sxs-lookup"><span data-stu-id="852c4-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="852c4-111">ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่างๆ บริการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="852c4-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="852c4-112">[![คำแนะนำเกี่ยวกับหน้ารายละเอียดผลิตภัณฑ์](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="852c4-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="852c4-113">ในหน้า **ธุรกรรม** :</span><span class="sxs-lookup"><span data-stu-id="852c4-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="852c4-114">กลไกคำแนะนำสินค้าจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในตระกร้าที่ซื้อพร้อมกันบ่อย</span><span class="sxs-lookup"><span data-stu-id="852c4-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="852c4-115">เพื่อแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ขายปลีกต้องปรับปรุงโครงร่างหน้าจอใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="852c4-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="852c4-116">จะต้องปล่อยการควบคุม **คำแนะนำ** ไปยังหน้า **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="852c4-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="852c4-117">[![คำแนะนำเกี่ยวกับหน้าธุรกรรม](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="852c4-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="852c4-118">กำหนดค่าการค้าเพื่อเปิดใช้งานคำแนะนำ POS</span><span class="sxs-lookup"><span data-stu-id="852c4-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="852c4-119">ถ้าต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="852c4-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="852c4-120">ตรวจสอบให้แน่ใจว่ายริการของคุณได้อัพเดทเป็น **10.0.6 บิวด์**</span><span class="sxs-lookup"><span data-stu-id="852c4-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="852c4-121">ปฏิบัติตามคำแนะนำเกี่ยวกับวิธีการ [เปิดใช้งานคำแนะนำผลิตภัณฑ์](../commerce/enable-product-recommendations.md) สำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="852c4-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="852c4-122">ไม่จำเป็น: เมื่อต้องการแสดงคำแนะนำบนหน้าจอธุรกรรม ไปที่ **โครงร่างหน้าจอ** เลือกโครงร่างหน้าจอของคุณ เปิดใช้ **ตัวออกแบบโครงร่างหน้าจอ** แล้วปล่อยการควบคุม **คำแนะนำ** เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="852c4-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="852c4-123">ไปที่ **พารามิเตอร์การค้า** เลือก **การเรียนรู้เกี่ยวกับเครื่อง** เลือก **ใช่** ภายใต้ **คำแนะนำการเปืดใช้งาน POS** </span><span class="sxs-lookup"><span data-stu-id="852c4-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="852c4-124">เมื่อต้องการดูคำแนะนำบน POS เรียกใช้งานการตั้งค่าคอนฟิกส่วนกลาง **1110**</span><span class="sxs-lookup"><span data-stu-id="852c4-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="852c4-125">เมื่อต้องการเปลี่ยนแปลงในตัวออกแบบโครงร่างหน้าจอ POS เรียกใช้งานการตั้งค่าคอนฟิกช่องทาง **1070**</span><span class="sxs-lookup"><span data-stu-id="852c4-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="852c4-126">แก้ไขปัญหาที่ซึ่งคุณมีคำแนะนำผลิตภัณฑ์ที่เปิดใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="852c4-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="852c4-127">นำทางไปยัง **พารามิเตอร์การค้า** \> **รายการแนะนำ** \> **ปิดใช้งานคำแนะนำผลิตภัณฑ์** และเรียกใช้ **งานการตั้งค่าส่วนกลาง \[9999\]**</span><span class="sxs-lookup"><span data-stu-id="852c4-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="852c4-128">ถ้าคุณได้เพิ่ม **ตัวควบคุมคำแนะนำ** ไปยังหน้าจอธุรกรรมของคุณโดยใช้ **โปรแกรมออกแบบโครงร่างหน้าจอ** โปรดลบรายการนั้นเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="852c4-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="852c4-129">หากคุณมีคำถามเพิ่มเติม ให้ดู [คำถามที่พบบ่อยเกี่ยวกับคำแนะนำผลิตภัณฑ์](../commerce/faq-recommendations.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="852c4-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="852c4-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="852c4-130">Additional resources</span></span>

[<span data-ttu-id="852c4-131">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="852c4-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="852c4-132">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="852c4-132">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="852c4-133">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="852c4-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="852c4-134">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="852c4-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="852c4-135">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="852c4-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="852c4-136">เพิ่มรายการคำแนะนำลงในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="852c4-136">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="852c4-137">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="852c4-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="852c4-138">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="852c4-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="852c4-139">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="852c4-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="852c4-140">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="852c4-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="852c4-141">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="852c4-141">Product recommendations FAQ</span></span>](faq-recommendations.md)
