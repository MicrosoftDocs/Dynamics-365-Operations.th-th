---
title: ภาพรวมของการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะครอบคลุมการจัดอันดับและบทวิจารณ์ใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1248ce660d765ddade1df7d79786202235019990
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057405"
---
# <a name="ratings-and-reviews-overview"></a><span data-ttu-id="585ac-103">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="585ac-103">Ratings and reviews overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="585ac-104">หัวข้อนี้จะครอบคลุมการจัดอันดับและบทวิจารณ์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="585ac-104">This topic covers ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="585ac-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="585ac-105">Overview</span></span>

<span data-ttu-id="585ac-106">การจัดอันดับและบทวิจารณ์มีความสำคัญต่อลูกค้าอีคอมเมิร์ซที่ต้องการทราบว่าลูกค้ารายอื่น ๆ รับรู้ผลิตภัณฑ์อย่างไร</span><span class="sxs-lookup"><span data-stu-id="585ac-106">Ratings and reviews are crucial for e-Commerce customers who want to know how other customers perceive a product.</span></span> <span data-ttu-id="585ac-107">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถตัดสินใจซื้อได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="585ac-107">They can also help consumers make purchase decisions.</span></span> <span data-ttu-id="585ac-108">ใน Dynamics 365 Commerce โซลูชันการจัดอันดับและบทวิจารณ์ของร้านค้าปลีก เก็บความคิดเห็นของผลิตภัณฑ์และการจัดอันดับจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="585ac-108">In Dynamics 365 Commerce, the ratings and reviews solution lets retailers capture product reviews and ratings from customers.</span></span> <span data-ttu-id="585ac-109">ร้านค้าปลีกสามารถแสดงการจัดอันดับโดยเฉลี่ยและตรวจสอบข้อมูลบนเว็บไซต์อีคอมเมิร์ซของตนได้</span><span class="sxs-lookup"><span data-stu-id="585ac-109">Retailers can then show average ratings and review information across their e-Commerce website.</span></span>

<span data-ttu-id="585ac-110">ข้อมูลการจัดอันดับเฉลี่ยจะแสดงอยู่ในช่องทางการขาย (POS) และศูนย์กลางการโทร</span><span class="sxs-lookup"><span data-stu-id="585ac-110">Average rating information is shown in point of sale (POS) and call center channels.</span></span> <span data-ttu-id="585ac-111">ดังนั้นบริษัทผู้ขายสามารถใช้เพื่อช่วยผู้ใช้ในการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="585ac-111">Therefore, sales associates can use it to help users make decisions.</span></span> <span data-ttu-id="585ac-112">การจัดอันดับและบทวิจารณ์ยังสามารถทำหน้าที่เป็นกลไกของผลป้อนกลับที่ร้านค้าปลีกสามารถใช้เพื่อปรับปรุงคุณภาพของผลิตภัณฑ์ดังนั้นจึงเพิ่มยอดขายได้</span><span class="sxs-lookup"><span data-stu-id="585ac-112">Ratings and reviews can also serve as a feedback mechanism that retailers can use to improve the quality of a product and therefore increase sales.</span></span>

<span data-ttu-id="585ac-113">ฟังก์ชันการจัดอันดับและการตรวจทานใน Dynamics 365 Commerce เป็นโซลูชันช่องทาง Omni และเป็นส่วนหนึ่งของแพลตฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="585ac-113">Ratings and reviews functionality in Dynamics 365 Commerce is an omnichannel solution and is natively available as part of the platform.</span></span> <span data-ttu-id="585ac-114">โซลูชันการจัดอันดับและบทวิจารณ์ถูกสร้างขึ้นบน Microsoft Azure ซึ่งช่วยให้ความสามารถในการขยายและความน่าเชื่อถือได้สูง</span><span class="sxs-lookup"><span data-stu-id="585ac-114">The ratings and reviews solution is built on top of Microsoft Azure, which provides high scalability and reliability.</span></span>

<span data-ttu-id="585ac-115">ภาพประกอบต่อไปนี้แสดงโซลูชั่นการจัดอันดับและบทวิจารณ์การทำงานใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="585ac-115">The following illustration shows how the ratings and reviews solution works in Dynamics 365 Commerce.</span></span>

![การให้คะแนนและบทวิจารณ์ใน Dynamics 365 for Commerce](media/Dynamics-365-Commerce-Ratings-and-Reviews-Overview.jpg)

<span data-ttu-id="585ac-117">โซลูชั่นการจัดอันดับและบทวิจารณ์ใน Dynamics 365 Commerce ใช้ Azure Cognitive Services ควบคุมคำหยาบโดยอัตโนมัติของภาษา 40 ภาษา</span><span class="sxs-lookup"><span data-stu-id="585ac-117">The ratings and reviews solution in Dynamics 365 Commerce uses Azure Cognitive Services to offer automatic moderation of profane words in 40 languages.</span></span> <span data-ttu-id="585ac-118">เนื่องจากไม่จำเป็นต้องมีการอนุมัติของบุคคลต้นทุนการควบคุมจะลดลง</span><span class="sxs-lookup"><span data-stu-id="585ac-118">Because human approval isn't required, moderation costs are reduced.</span></span> <span data-ttu-id="585ac-119">ระบบนี้ยังมีเครื่องมือสำหรับผู้ดูแลซึ่งสามารถใช้ในการตอบสนองความต้องการของลูกค้าความคิดเห็น และการร้องขอการดำเนินการและเพื่อที่อยู่ของคำขอข้อมูลจากผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="585ac-119">The system also offers moderator tools that can be used to respond to customer concerns, feedback, and take-down requests, and to address data requests from users.</span></span>

<span data-ttu-id="585ac-120">โซลูชันการจัดอันดับและบทวิจารณ์จะแสดงวิดเจ็ตซึ่งแสดงสรุปการจัดอันดับในรายการผลิตภัณฑ์ ในผลการค้นหา ในหน้ารายละเอียดของผลิตภัณฑ์ และในที่อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="585ac-120">The ratings and reviews solution provides widgets that show rating summaries in product lists, in search results, on product details page, and in other places.</span></span> <span data-ttu-id="585ac-121">วิดเจ็ตจะแสดงรายการบทวิจารณ์ที่สมบูรณ์ และมีตัวเลือกการเรียงลำดับและการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="585ac-121">The widgets show complete review lists, and they also provide sorting and filtering options.</span></span>

<span data-ttu-id="585ac-122">โซลูชันการจัดอันดับและบทวิจารณ์ยังแสดงแม่แบบข่าวกรองธุรกิจ (BI) ซึ่งรวมถึงชุดของการวัดที่จะให้ข้อมูลเชิงลึกให้กับการจัดอันดับและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="585ac-122">The ratings and reviews solution also provides a business intelligence (BI) template that includes a set of metrics to provide insights into ratings and reviews.</span></span> <span data-ttu-id="585ac-123">สามารถส่งออกข้อมูลการจัดอันดับและบทวิจารณ์สำหรับการวิเคราะห์เพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="585ac-123">Ratings and reviews data can be exported for further analysis.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="585ac-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="585ac-124">Additional resources</span></span>

[<span data-ttu-id="585ac-125">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="585ac-125">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="585ac-126">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="585ac-126">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="585ac-127">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="585ac-127">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="585ac-128">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="585ac-128">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)
