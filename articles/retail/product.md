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
ms.openlocfilehash: 98c84e987c40adf136d0240117f7b0f119bf2f59
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811128"
---
# <a name="product-recommendations-on-pos"></a><span data-ttu-id="1e99d-103">คำแนะนำผลิตภัณฑ์บน POS</span><span class="sxs-lookup"><span data-stu-id="1e99d-103">Product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e99d-104">ตามหลัก คำแนะนำของผลิตภัณฑ์เป็นแอพลิเคชันธุรกิจการเปลี่ยนแบบซึ่งครอบคลุมทั้งพื้นที่ขายปลีกทั้งหมดเพื่อสร้างประสบการณ์การค้นหาผลิตภัณฑ์ที่เหมาะเจาะ น่าติดตาม อย่างมากมาย</span><span class="sxs-lookup"><span data-stu-id="1e99d-104">At its core, product Recommendations are a transformative business application that span across all retail spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="1e99d-105">เมื่อต้องการใช้งานลักษณะการทำงานนี้บน[POS ให้ทำตามขั้นตอนเกี่ยวกับวิธีการเพิ่มข้อเสนอแนะให้กับอุปกรณ์ POS ของคุณ](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="1e99d-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="1e99d-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน  [คำแนะนำผลิตภัณฑ์ในเอกสารของ POS](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="1e99d-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="1e99d-107">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="1e99d-107">Scenarios</span></span>

<span data-ttu-id="1e99d-108">คำแนะนำผลิตภัณฑ์ถูกเปิดใช้งานสำหรับสถานการณ์ POS ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1e99d-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="1e99d-109">ซึ่งจะพร้อมใช้งานใน Cloud POS หรือ Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="1e99d-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="1e99d-110">ในหน้า **รายละเอียดผลิตภัณฑ์** :</span><span class="sxs-lookup"><span data-stu-id="1e99d-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="1e99d-111">ถ้าการเชื่อมโยงของร้านค้าเยี่ยมชมหน้า **รายละเอียดผลิตภัณฑ์** เมื่อดูที่ธุรกรรมก่อนหน้านี้ผ่านช่องทางต่างๆ บริการคำแนะนำจะแนะนำสินค้าเพิ่มเติมที่มีแนวโน้มที่จะถูกซื้อพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="1e99d-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="1e99d-112">[![คำแนะนำเกี่ยวกับหน้ารายละเอียดผลิตภัณฑ์](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="1e99d-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="1e99d-113">ในหน้า **ธุรกรรม** :</span><span class="sxs-lookup"><span data-stu-id="1e99d-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="1e99d-114">กลไกคำแนะนำสินค้าจะแนะนำสินค้าตามรายการสินค้าทั้งหมดในตระกร้าที่ซื้อพร้อมกันบ่อย</span><span class="sxs-lookup"><span data-stu-id="1e99d-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e99d-115">เพื่อแสดงคำแนะนำในหน้า **ธุรกรรม** ผู้ขายปลีกต้องปรับปรุงโครงร่างหน้าจอใน Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="1e99d-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="1e99d-116">จะต้องปล่อยการควบคุม **คำแนะนำ** ไปยังหน้า **ธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="1e99d-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="1e99d-117">[![คำแนะนำเกี่ยวกับหน้าธุรกรรม](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="1e99d-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a><span data-ttu-id="1e99d-118">ตั้งค่าคอนฟิก Dynamics 365 Retail เพื่อเปิดใช้งานคำแนะนำ POS</span><span class="sxs-lookup"><span data-stu-id="1e99d-118">Configure Dynamics 365 Retail to enable POS recommendations</span></span>

<span data-ttu-id="1e99d-119">ถ้าต้องการตั้งค่าคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="1e99d-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="1e99d-120">ตรวจสอบให้แน่ใจว่ายริการของคุณได้อัพเดทเป็น **10.0.6 บิวด์**</span><span class="sxs-lookup"><span data-stu-id="1e99d-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="1e99d-121">ปฏิบัติตามคำแนะนำเกี่ยวกับวิธีการ [เปิดใช้งานคำแนะนำผลิตภัณฑ์](../commerce/enable-product-recommendations.md) สำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="1e99d-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="1e99d-122">ไม่จำเป็น: เมื่อต้องการแสดงคำแนะนำบนหน้าจอธุรกรรม ไปที่ **โครงร่างหน้าจอ** เลือกโครงร่างหน้าจอของคุณ เปิดใช้ **ตัวออกแบบโครงร่างหน้าจอ** แล้วปล่อยการควบคุม **คำแนะนำ** เมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="1e99d-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="1e99d-123">ไปที่ **พารามิเตอร์การขายปลีก** เลือก **Machine-learning** เลือก **ใช่** ภายใต้ **เปิดใช้งานคำแนะนำ POS**</span><span class="sxs-lookup"><span data-stu-id="1e99d-123">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="1e99d-124">เมื่อต้องการดูคำแนะนำบน POS เรียกใช้งานการตั้งค่าคอนฟิกส่วนกลาง **1110**</span><span class="sxs-lookup"><span data-stu-id="1e99d-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="1e99d-125">เมื่อต้องการเปลี่ยนแปลงในตัวออกแบบโครงร่างหน้าจอ POS เรียกใช้งานการตั้งค่าคอนฟิกช่องทาง **1070**</span><span class="sxs-lookup"><span data-stu-id="1e99d-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="1e99d-126">แก้ไขปัญหาที่ซึ่งคุณมีคำแนะนำผลิตภัณฑ์ที่เปิดใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="1e99d-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="1e99d-127">นำทางไปยัง **พารามิเตอร์การขายปลีก** \> **ลิสต์คำแนะนำ** \> **ปิดใช้งานคำแนะนำผลิตภัณฑ์** และรัน **งานการตั้งค่าคอนฟิกส่วนกลาง \[9999\]**</span><span class="sxs-lookup"><span data-stu-id="1e99d-127">Navigate to **Retail Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="1e99d-128">ถ้าคุณได้เพิ่ม **ตัวควบคุมคำแนะนำ** ไปยังหน้าจอธุรกรรมของคุณโดยใช้ **โปรแกรมออกแบบโครงร่างหน้าจอ** โปรดลบรายการนั้นเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="1e99d-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="1e99d-129">หากคุณมีคำถามเพิ่มเติม ให้ดู [คำถามที่พบบ่อยเกี่ยวกับคำแนะนำผลิตภัณฑ์](../commerce/faq-recommendations.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1e99d-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e99d-130">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1e99d-130">Additional resources</span></span>

[<span data-ttu-id="1e99d-131">เพิ่มตัวควบคุมคำแนะนำในหน้าจอธุรกรรมบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="1e99d-131">Add a recommendations control to the transaction screen on POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1e99d-132">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1e99d-132">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="1e99d-133">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1e99d-133">Enable product recommendations</span></span>](../commerce/enable-product-recommendations.md) 
