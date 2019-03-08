---
title: ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง)
description: หัวข้อนี้อธิบายวิธีการที่ข้อมูลเชิงลึกในการชำระเงินของลูกค้าสามารถช่วยคาดการณ์ได้ เมื่อจะมีการชำระใบแจ้งหนี้ และช่วยองค์กรในการสร้างกลยุทธ์การเพิ่มประสิทธิภาพที่ปรับปรุงความน่าจะเป็นในการชำระเงินตรงเวลา
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "344673"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="a246a-103">ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="a246a-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="a246a-104">คุณลักษณะนี้เป็นส่วนหนึ่งของการนำออกใช้ที่เป็นเป้าหมาย และพร้อมใช้งานเฉพาะสำหรับผู้ใช้ที่เลือกเข้าร่วมในการแสดงตัวอย่างแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="a246a-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="a246a-105">คุณลักษณะนี้จะถูกรวมอยู่ในรีลีสความพร้อมใช้งานทั่วไปที่กำลังจะมีขึ้น</span><span class="sxs-lookup"><span data-stu-id="a246a-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="a246a-106">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="a246a-106">Overview</span></span>

<span data-ttu-id="a246a-107">องค์กรมักจะพบความท้าทายในการคาดการณ์เวลาที่ลูกค้าจะชำระใบแจ้งหนี้ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="a246a-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="a246a-108">การขาดข้อมูลเชิงลึกนี้อาจนำไปสู่การคาดการณ์กระแสเงินสดที่ไม่ถูกต้อง กระบวนการเรียกเก็บเงินที่ไม่มีประสิทธิภาพ และความเป็นไปได้ของใบสั่งที่นำออกใช้สำหรับลูกค้าที่อาจทำให้เกิดความเสี่ยงเครดิตได้</span><span class="sxs-lookup"><span data-stu-id="a246a-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="a246a-109">ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง) ใช้ Machine Learning เพื่อคาดการณ์เวลาที่จะมีการชำระใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a246a-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a246a-110">นอกจากนี้ ยังมีกลยุทธ์การเพิ่มประสิทธิภาพที่สามารถปรับเพิ่มความน่าจะเป็นของลูกค้าที่ชำระเงินตรงเวลาได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="a246a-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="a246a-111">การคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="a246a-111">Predictions</span></span>

<span data-ttu-id="a246a-112">การคาดการณ์การชำระเงินอนุญาตให้องค์กรสามารถปรับปรุงกระบวนการทางธุรกิจของพวกเขาได้โดยการช่วย:</span><span class="sxs-lookup"><span data-stu-id="a246a-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="a246a-113">ระบุใบแจ้งหนี้ที่ถูกคาดการณ์ว่าจะมีการชำระล่าช้าได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="a246a-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="a246a-114">ใช้หน่วยวัดที่เหมาะสมเพื่อปรับปรุงโอกาสของการรับชำระเงินตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="a246a-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="a246a-115">ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง) ใช้ Machine Learning เพื่อคาดการณ์เวลาที่จะมีการชำระใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a246a-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="a246a-116">จะใช้ใบแจ้งหนี้ การชำระเงิน และข้อมูลลูกค้าในอดีต เพื่อสร้างแบบจำลอง Machine Learning ที่ใช้ในการคาดการณ์ เมื่อจะมีการชำระใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a246a-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="a246a-117">สำหรับใบแจ้งหนี้แบบเปิดแต่ละใบ ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง) คาดการณ์ความน่าจะเป็นในการชำระเงินสามแบบ:</span><span class="sxs-lookup"><span data-stu-id="a246a-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="a246a-118">ความน่าจะเป็นในการชำระเงินที่ชำระตรงเวลา (ภายในวันครบกำหนดชำระในใบแจ้งหนี้)</span><span class="sxs-lookup"><span data-stu-id="a246a-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="a246a-119">ความน่าจะเป็นในการชำระเงินที่ชำระภายใน 30 วันของวันครบกำหนดชำระในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a246a-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="a246a-120">ความน่าจะเป็นในการชำระเงินที่ชำระเกิน 30 วันของวันครบกำหนดชำระในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a246a-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="a246a-121">ความน่าจะเป็นของการชำระเงินสามารถดูได้ในส่วนการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="a246a-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="a246a-122">[![การคาดการณ์การชำระเงิน](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="a246a-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="a246a-123">ใบแจ้งหนี้แต่ละใบจะยังถูกกำหนดความน่าจะเป็นในการชนะของการชำระเงิน ที่ใช้วิธีการใดวิธีการหนึ่งในสถานการณ์จำลองความน่าจะเป็นในการชำระเงินที่คาดการณ์ไว้สามแบบที่กำหนดไว้ข้างต้น</span><span class="sxs-lookup"><span data-stu-id="a246a-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="a246a-124">สถานการณ์จำลองที่มีความน่าจะเป็นในการชำระเงินสูงสุดคือ สถานการณ์จำลองในการชนะ</span><span class="sxs-lookup"><span data-stu-id="a246a-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="a246a-125">ตัวอย่างเช่น สมมติว่าสำหรับใบแจ้งหนี้ที่การคาดการณ์แสดงความน่าจะเป็น 71 เปอร์เซ็นต์ที่จะมีการชำระใบแจ้งหนี้ตรงเวลา ความน่าจะเป็น 13 เปอร์เซ็นต์ที่จะมีการชำระใบแจ้งหนี้ภายใน 30 วันของวันครบกำหนด และความน่าจะเป็น 16 เปอร์เซ็นต์ที่จะมีการชำระใบแจ้งหนี้เกินกว่า 30 วันที่ของวันครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="a246a-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="a246a-126">ความน่าจะเป็นสูงสุดแสดงว่า ใบแจ้งหนี้จะอยู่ในสถานการณ์จำลองแบบตรงเวลา ดังนั้นจะมีการระบุป้ายใบแจ้งหนี้ด้วยความน่าจะเป็นของการชำระเงินตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="a246a-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="a246a-127">[![การคาดการณ์การชำระเงิน](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="a246a-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="a246a-128">กลยุทธ์การเพิ่มประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a246a-128">Optimization strategies</span></span>

<span data-ttu-id="a246a-129">นอกเหนือจากการคาดการณ์การชำระเงิน ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง) สามารถใช้กลยุทธ์การปรับให้เหมาะสมเพื่อเพิ่มโอกาสของการรับชำระเงินตรงเวลาได้</span><span class="sxs-lookup"><span data-stu-id="a246a-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="a246a-130">นี่จะอนุญาตให้องค์กรสามารถทำการวิเคราะห์ 'ถ้าหาก' โดยการอนุญาตให้ผู้ใช้สามารถปรับปรุงพารามิเตอร์ใบแจ้งหนี้และลูกค้าได้ และจากนั้น เปรียบเทียบผลกระทบที่สอดคล้องกันต่อความน่าจะเป็นของการรับการชำระเงินในใบแจ้งหนี้ที่ตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="a246a-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="a246a-131">ตัวอย่างเช่น องค์กรอาจต้องการประเมินผลกระทบของการปรับปรุงส่วนลดเงินสดในใบแจ้งหนี้เกี่ยวกับความน่าจะเป็นของการรับการชำระเงินที่ตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="a246a-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="a246a-132">เมื่อใบแจ้งหนี้ถูกปรับให้เหมาะสมเพื่อใช้ส่วนลดใหม่ ผู้ใช้สามารถตรวจทานผลกระทบของการใช้ส่วนลดในความน่าจะเป็นของการรับการชำระเงินสำหรับใบแจ้งหนี้เหล่านั้นตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="a246a-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="a246a-133">ถ้าต้นทุนของการใช้ส่วนลดเป็นระดับต่ำสุด เมื่อเปรียบเทียบกับสวัสดิการของการชำระเงินที่ตรงเวลา องค์กรอาจเลือกที่จะใช้ส่วนลดที่เลือกกับใบสั่งที่เปิดในอนาคตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a246a-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="a246a-134">ในปัจจุบัน เฉพาะส่วนลดจะพร้อมใช้งานเป็นกลยุทธ์การปรับให้เหมาะสมสำหรับข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="a246a-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="a246a-135">[![การคาดการณ์ที่ปรับให้เหมาะสม](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="a246a-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="a246a-136">วิธีการรับข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="a246a-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="a246a-137">ถ้าคุณสนใจที่จะลองข้อมูลเชิงลึกในการชำระเงินของลูกค้า (การแสดงตัวอย่าง) โปรดอีเมล [ทีมการแสดงตัวอย่างในข้อมูลเชิงลึกทางการเงิน](mailto:fiap@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="a246a-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="a246a-138">คำชี้แจงสิทธิ์ส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="a246a-138">Privacy Statement</span></span>

<span data-ttu-id="a246a-139">แสดงตัวอย่างข้อมูลของลูกค้าในร้านในสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="a246a-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="a246a-140">นอกจากนี้ การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 for Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการสำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="a246a-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
