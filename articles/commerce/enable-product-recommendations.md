---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154424"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="cdbf8-103">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cdbf8-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cdbf8-104">หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cdbf8-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="cdbf8-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="cdbf8-106">การตรวจสอบคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="cdbf8-106">Recommendations pre-check</span></span>

<span data-ttu-id="cdbf8-107">ก่อนเปิดใช้งาน โปรดทราบว่าคำแนะนำผลิตภัณฑ์ได้รับการสนับสนุนเฉพาะสำหรับลูกค้าเชิงพาณิชย์ที่โอนย้ายที่เก็บข้อมูลของตนไปใช้ Azure Data Lake Storage (ADLS) </span><span class="sxs-lookup"><span data-stu-id="cdbf8-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="cdbf8-108">สำหรับขั้นตอนการเปิดใช้งาน ADLS ดู [ธีเปิดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365](enable-ADLS-environment.md)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="cdbf8-109">นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว</span><span class="sxs-lookup"><span data-stu-id="cdbf8-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="cdbf8-110">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับกระบวนการตั้งค่านี้ให้ไปที่ [ที่นี่](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="cdbf8-111">เปิดคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="cdbf8-111">Turn on recommendations</span></span>

<span data-ttu-id="cdbf8-112">ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cdbf8-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="cdbf8-113">ไปยัง **การขายปลีกและการค้า &gt; คำแนะนำผลิตภัณฑ์ &gt; พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="cdbf8-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="cdbf8-114">ในรายการของพารามิเตอร์ที่ใช้ร่วมกัน ให้เลือก **รายการคำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="cdbf8-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="cdbf8-115">ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cdbf8-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![เปิดใช้งานคำแนะนำผลิตภัณฑ์](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="cdbf8-117">ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cdbf8-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="cdbf8-118">อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cdbf8-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="cdbf8-119">ตั้งค่าพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="cdbf8-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="cdbf8-120">โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="cdbf8-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="cdbf8-121">คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="cdbf8-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="cdbf8-122">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="cdbf8-123">แสดงคำแนะนำบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="cdbf8-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="cdbf8-124">หลังจากเปิดใช้งานคำแนะนำในแผนกสนับสนุน (Back Office) เชิงพาณิชย์จะต้องเพิ่มแผงคำแนะนำลงในหน้าจอการควบคุม POS โดยใช้เครื่องมือเค้าโครง</span><span class="sxs-lookup"><span data-stu-id="cdbf8-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="cdbf8-125">หากต้องการเรียนรู้เกี่ยวกับกระบวนการนี้ ให้ดู [เพิ่มการควบคุมคำแนะนำให้กับหน้าจอธุรกรรมบนอุปกรณ์ POS](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="cdbf8-126">เปิดใช้งานคำแนะนำแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="cdbf8-126">Enable personalized recommendations</span></span>

<span data-ttu-id="cdbf8-127">เรียนรู้เพิ่มเติมเกี่ยวกับวิธีรับคำแนะนำแบบส่วนตัว โปรดดู [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="cdbf8-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdbf8-128">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cdbf8-128">Additional resources</span></span>

[<span data-ttu-id="cdbf8-129">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cdbf8-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="cdbf8-130">เปืดใช้งาน ADLS ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cdbf8-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="cdbf8-131">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="cdbf8-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="cdbf8-132">เลือกปฏิเสธคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="cdbf8-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="cdbf8-133">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="cdbf8-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="cdbf8-134">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cdbf8-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="cdbf8-135">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="cdbf8-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="cdbf8-136">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="cdbf8-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="cdbf8-137">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cdbf8-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="cdbf8-138">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cdbf8-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

