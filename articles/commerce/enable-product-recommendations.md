---
title: เปิดใช้งานคำแนะนำผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770150"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="658a4-103">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="658a4-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="658a4-104">หัวข้อนี้จะอธิบายถึงวิธีการให้คำแนะนำเกี่ยวกับผลิตภัณฑ์ที่ยึดตามการเรียนรู้ของเครื่องมือปัญญาประดิษฐ์ (AL-ML) ที่มีให้ใช้งานสำหรับลูกค้า Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="658a4-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="658a4-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์ โปรดอ่าน [ภาพรวมคำแนะนำผลิตภัณฑ์](product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="658a4-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="658a4-106">การตรวจสอบคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="658a4-106">Recommendations pre-check</span></span>
<span data-ttu-id="658a4-107">ก่อนที่จะเปิดใช้งาน โปรดทราบว่าคำแนะนำของผลิตภัณฑ์สนับสนุนเฉพาะสำหรับลูกค้า F&O ซึ่งสนับสนุนเวอร์ชัน 10.0.6 และโยกย้ายพื้นที่จัดเก็บของตนไว้เพื่อใช้ BDL</span><span class="sxs-lookup"><span data-stu-id="658a4-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="658a4-108">นอกจากนี้ ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการวัด RetailSale แล้ว</span><span class="sxs-lookup"><span data-stu-id="658a4-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="658a4-109">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับขั้นตอนการตั้งค่านี้ให้ไป [ที่นี่](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="658a4-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="658a4-110">เปิดคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="658a4-110">Turn on recommendations</span></span>

<span data-ttu-id="658a4-111">ถ้าต้องการเปิดคำแนะนำผลิตภัณฑ์ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="658a4-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="658a4-112">ไปที่ **การขายปลีก** &gt; **คำแนะนำของผลิตภัณฑ์** &gt; **พารามิเตอร์คำแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="658a4-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="658a4-113">ในรายการพารามิเตอร์ที่ใช้ร่วมกันของการขายปลีก เลือก **รายการแนะนำ**</span><span class="sxs-lookup"><span data-stu-id="658a4-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="658a4-114">ตั้งค่าตัวเลือก **เปิดใช้คำแนะนำ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="658a4-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![เปิดใช้งานคำแนะนำผลิตภัณฑ์](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="658a4-116">ขั้นตอนนี้จะเริ่มต้นกระบวนการสร้างรายการคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="658a4-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="658a4-117">อาจจำเป็นต้องใช้หลายชั่วโมงก่อนที่รายการจะพร้อมใช้งาน และสามารถดูได้จากการขายหน้าร้าน (POS) หรือใน Dynamics 365 for Commerce</span><span class="sxs-lookup"><span data-stu-id="658a4-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="658a4-118">ตั้งค่าพารามิเตอร์รายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="658a4-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="658a4-119">โดยค่าเริ่มต้นรายการคำแนะนำผลิตภัณฑ์ที่ใช้ AI-ML จะแสดงค่าที่แนะนำ</span><span class="sxs-lookup"><span data-stu-id="658a4-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="658a4-120">คุณสามารถเปลี่ยนค่าเริ่มต้นที่แนะนำเพื่อให้เหมาะสมกับกระบวนการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="658a4-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="658a4-121">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับวิธีการเปลี่ยนพารามิเตอร์เริ่มต้นให้ไปที่ [การจัดการผลลัพธ์การแนะนำของผลิตภัณฑ์ที่ใช้ AI-ML](modify-product-recommendation-results.md)</span><span class="sxs-lookup"><span data-stu-id="658a4-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="658a4-122">แสดงคำแนะนำบนอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="658a4-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="658a4-123">หลังจากเปิดใช้งานคำแนะนำในฝ่ายสนับสนุน แล้วคุณต้องเพิ่มแผงคำแนะนำให้กับหน้าจอ POS ควบคุมผ่านทางเครื่องมือโครงร่าง</span><span class="sxs-lookup"><span data-stu-id="658a4-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="658a4-124">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับขั้นตอนนี้ให้ไป [ที่นี่](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="658a4-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="658a4-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="658a4-125">Additional resources</span></span>

[<span data-ttu-id="658a4-126">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="658a4-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="658a4-127">เพิ่มรายการคำแนะนำผลิตภัณฑ์ลงในหน้า</span><span class="sxs-lookup"><span data-stu-id="658a4-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="658a4-128">เพิ่มแผงคำแนะนำลงในอุปกรณ์ POS</span><span class="sxs-lookup"><span data-stu-id="658a4-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


