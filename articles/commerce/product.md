---
title: คำแนะนำผลิตภัณฑ์บน POS
description: หัวข้อนี้จะอธิบายถึงการใช้คำแนะนำผลิตภัณฑ์บนอุปกรณ์การขายหน้าร้าน (POS)
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057452"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="701e5-103">คำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="701e5-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="701e5-104">คามหลัก คำแนะนำผลิตภัณฑ์เป็นแอปพลิเคชันทางธุรกิจเพื่อการเปลี่ยนแปลงที่ครอบคลุมพื้นที่การค้าทั้งหมด เพื่อสร้างประสบการณ์การค้นพบผลิตภัณฑ์ที่หลากหลาย น่าดึงดูด และได้รับการปรับให้เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="701e5-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="701e5-105">เมื่อต้องการใช้งานลักษณะการทำงานนี้บน[POS ให้ทำตามขั้นตอนเกี่ยวกับวิธีการเพิ่มข้อเสนอแนะให้กับอุปกรณ์ POS ของคุณ](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="701e5-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="701e5-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน  [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="701e5-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="701e5-107">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="701e5-107">Scenarios</span></span>

<span data-ttu-id="701e5-108">คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="701e5-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="701e5-109">ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="701e5-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="701e5-110">ในหน้า **รายละเอียดผลิตภัณฑ์** :</span><span class="sxs-lookup"><span data-stu-id="701e5-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="701e5-111">ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่างๆ บริการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="701e5-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="701e5-112">[![คำแนะนำเกี่ยวกับหน้ารายละเอียดผลิตภัณฑ์](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="701e5-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="701e5-113">ในหน้า **ธุรกรรม** :</span><span class="sxs-lookup"><span data-stu-id="701e5-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="701e5-114">กลไกคำแนะนำสินค้าจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในตระกร้าที่ซื้อพร้อมกันบ่อย</span><span class="sxs-lookup"><span data-stu-id="701e5-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="701e5-115">เพื่อแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ขายปลีกต้องปรับปรุงโครงร่างหน้าจอใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="701e5-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="701e5-116">จะต้องปล่อยการควบคุม **คำแนะนำ** ไปยังหน้า **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="701e5-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="701e5-117">[![คำแนะนำเกี่ยวกับหน้าธุรกรรม](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="701e5-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="701e5-118">กำหนดค่าการค้าเพื่อเปิดใช้งานคำแนะนำ POS</span><span class="sxs-lookup"><span data-stu-id="701e5-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="701e5-119">ถ้าต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="701e5-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="701e5-120">ตรวจสอบให้แน่ใจว่ายริการของคุณได้อัพเดทเป็น **10.0.6 บิวด์**</span><span class="sxs-lookup"><span data-stu-id="701e5-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="701e5-121">ปฏิบัติตามคำแนะนำเกี่ยวกับวิธีการ [เปิดใช้งานคำแนะนำผลิตภัณฑ์](../commerce/enable-product-recommendations.md) สำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="701e5-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="701e5-122">ไม่จำเป็น: เมื่อต้องการแสดงคำแนะนำบนหน้าจอธุรกรรม ไปที่ **โครงร่างหน้าจอ** เลือกโครงร่างหน้าจอของคุณ เปิดใช้ **ตัวออกแบบโครงร่างหน้าจอ** แล้วปล่อยการควบคุม **คำแนะนำ** เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="701e5-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="701e5-123">ไปที่ **พารามิเตอร์การค้า** เลือก **การเรียนรู้เกี่ยวกับเครื่อง** เลือก **ใช่** ภายใต้ **คำแนะนำการเปืดใช้งาน POS** </span><span class="sxs-lookup"><span data-stu-id="701e5-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="701e5-124">เมื่อต้องการดูคำแนะนำบน POS เรียกใช้งานการตั้งค่าคอนฟิกส่วนกลาง **1110**</span><span class="sxs-lookup"><span data-stu-id="701e5-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="701e5-125">เมื่อต้องการเปลี่ยนแปลงในตัวออกแบบโครงร่างหน้าจอ POS เรียกใช้งานการตั้งค่าคอนฟิกช่องทาง **1070**</span><span class="sxs-lookup"><span data-stu-id="701e5-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="701e5-126">แก้ไขปัญหาที่ซึ่งคุณมีคำแนะนำผลิตภัณฑ์ที่เปิดใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="701e5-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="701e5-127">นำทางไปยัง **พารามิเตอร์การค้า** \> **รายการแนะนำ** \> **ปิดใช้งานคำแนะนำผลิตภัณฑ์** และเรียกใช้ **งานการตั้งค่าส่วนกลาง \[9999\]**</span><span class="sxs-lookup"><span data-stu-id="701e5-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="701e5-128">ถ้าคุณได้เพิ่ม **ตัวควบคุมคำแนะนำ** ไปยังหน้าจอธุรกรรมของคุณโดยใช้ **โปรแกรมออกแบบโครงร่างหน้าจอ** โปรดลบรายการนั้นเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="701e5-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="701e5-129">หากคุณมีคำถามเพิ่มเติม ให้ดู [คำถามที่พบบ่อยเกี่ยวกับคำแนะนำผลิตภัณฑ์](../commerce/faq-recommendations.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="701e5-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="701e5-130">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="701e5-130">Additional resources</span></span>

[<span data-ttu-id="701e5-131">เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="701e5-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="701e5-132">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="701e5-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="701e5-133">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="701e5-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
