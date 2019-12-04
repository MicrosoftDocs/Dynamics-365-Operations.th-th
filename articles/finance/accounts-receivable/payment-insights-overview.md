---
title: ข้อมูลเชิงลึกเกี่ยวกับการชำระเงินของลูกค้า (รุ่นตัวอย่าง)
description: หัวข้อนี้จะอธิบายถึงความสามารถในการชำระเงินเชิงลึก ซึ่งช่วยเพิ่มความเข้าใจในการปฏิบัติตามวิธีการชำระเงินโดยทั่วไปของลูกค้าแต่ละราย และสามารถระบุถึงสถานการณ์ที่มีการเริ่มต้นกระบวนการเรียกเก็บเงินก่อนหน้าที่คุณทำไว้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774058"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="07efe-103">ข้อมูลเชิงลึกเกี่ยวกับการชำระเงินของลูกค้า (รุ่นตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="07efe-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="07efe-104">หัวข้อนี้จะอธิบายถึงความสามารถในการชำระเงินเชิงลึก ซึ่งช่วยเพิ่มความเข้าใจในการปฏิบัติตามวิธีการชำระเงินโดยทั่วไปของลูกค้าแต่ละราย และสามารถระบุถึงสถานการณ์ที่มีการเริ่มต้นกระบวนการเรียกเก็บเงินก่อนหน้าที่คุณจะทำในรูปแบบอื่น</span><span class="sxs-lookup"><span data-stu-id="07efe-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="07efe-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="07efe-105">Overview</span></span>

<span data-ttu-id="07efe-106">องค์กรมักจะพบความท้าทายในการคาดการณ์เวลาที่ลูกค้าจะชำระใบแจ้งหนี้ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="07efe-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="07efe-107">การขาดข้อมูลเชิงลึกนี้นำไปสู่การคาดการณ์กระแสเงินสดที่มีความถูกต้องน้อยลง กระบวนการเรียกเก็บเงินที่เริ่มต้นสายเกินไป และใบสั่งที่นำออกใช้สำหรับลูกค้าที่อาจไม่สามารถชำระเงินได้</span><span class="sxs-lookup"><span data-stu-id="07efe-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="07efe-108">เชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง) ช่วยองค์กรคาดการณ์ได้ว่า เมื่อไหร่ถึงจะมีการชำระใบแจ้งหนี้ ซึ่งช่วยองค์กรในการสร้างชุดของกลยุทธ์ที่เพิ่มประสิทธิภาพและเพิ่มความน่าจะเป็นในการชำระเงินตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="07efe-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="07efe-109">การคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="07efe-109">Predictions</span></span>

<span data-ttu-id="07efe-110">การคาดการณ์การชำระเงินจะช่วยให้องค์กรสามารถพัฒนากระบวนการทางธุรกิจของตนเองได้ โดยการช่วยระบุใบแจ้งหนี้ที่มีแนวโน้มจะเป็นผู้จ่ายเงินล่าช้า และใช้มาตรการที่เหมาะสมเพื่อปรับปรุงโอกาสในการได้รับค่าจ้างตามเวลา</span><span class="sxs-lookup"><span data-stu-id="07efe-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="07efe-111">การใช้แบบจำลอง Machine Learning ซึ่งใช้ประโยชน์จากใบแจ้งหนี้ในอดีต การชำระเงินและข้อมูลลูกค้า ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง) สามารถคาดคะเนได้อย่างถูกต้องมากขึ้นว่าเมื่อไดลูกค้าจะชำระเงินใบแจ้งหนี้ที่คงค้าง</span><span class="sxs-lookup"><span data-stu-id="07efe-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="07efe-112">สำหรับใบแจ้งหนี้แบบเปิดแต่ละใบ ข้อมูลเชิงลึกในการชำระเงินของลูกค้า (ตัวอย่าง) คาดการณ์ความน่าจะเป็นในการชำระเงินสามแบบ:</span><span class="sxs-lookup"><span data-stu-id="07efe-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="07efe-113">ความน่าจะเป็นของการชำระเงินที่เกิดขึ้นตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="07efe-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="07efe-114">ความน่าจะเป็นของการชำระเงินที่เกิดขึ้นช้า</span><span class="sxs-lookup"><span data-stu-id="07efe-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="07efe-115">ความน่าจะเป็นของการชำระเงินที่เกิดขึ้นช้ามาก</span><span class="sxs-lookup"><span data-stu-id="07efe-115">Probability of payment being made very late</span></span>

<span data-ttu-id="07efe-116">เพื่อช่วยให้องค์กรเข้าใจยอดเงินรวมของการชำระเงินทั้งหมดที่สามารถคาดหวังจากลูกค้าในหนึ่งในสามของกลุ่ม ตรงเวลา ล่าช้า และล่าช้ามาก การเงินข้อมูลเชิงลึกของลูกค้า (ตัวอย่าง) นอกจากนี้ยังมีมุมมองรวมของการชำระเงินที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="07efe-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="07efe-117">[![มุมมองรวมของการคาดการณ์การชำระเงิน](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="07efe-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="07efe-118">นอกจากนี้ ใบแจ้งหนี้แต่ละใบจะถูกกำหนดความน่าจะเป็นของการชำระเงินตรงเวลา</span><span class="sxs-lookup"><span data-stu-id="07efe-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="07efe-119">ถ้าความน่าจะเป็นของการชำระเงินในเวลาน้อยกว่า 50% ใบแจ้งหนี้จะถูกติดแท็กด้วยวงกลมสีแดงเพื่อบ่งชี้ว่าใบแจ้งหนี้เหล่านี้อาจจำเป็นต้องได้รับความสนใจจากคอลเลกชัน</span><span class="sxs-lookup"><span data-stu-id="07efe-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="07efe-120">[![รายการความน่าจะเป็นในการชำระเงิน](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="07efe-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="07efe-121">ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (การแสดงตัวอย่าง) ยังมีข้อมูลบริบทเพื่ออธิบายการคาดการณ์ เช่น ปัจจัยใหญ่ที่มีผลกระทบต่อการคาดการณ์สถานะปัจจุบันของธุรกิจที่มีลูกค้า และรายละเอียดเกี่ยวกับการชำระเงินของลูกค้าในอดีต</span><span class="sxs-lookup"><span data-stu-id="07efe-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="07efe-122">ในธุรกิจจำนวนมาก กระบวนการเรียกเก็บเงินเป็นกิจกรรมที่มีการดำเนินการ กระบวนการเรียกเก็บเงินไม่เริ่มต้นจนกว่าใบแจ้งหนี้จะครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="07efe-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="07efe-123">ด้วยข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง) องค์กรสามารถใช้ในเชิงรุกมากขึ้นเกี่ยวกับการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="07efe-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="07efe-124">พวกเขาไม่จำเป็นต้องรอให้ธุรกรรมเกิดขึ้น เพื่อเริ่มต้นกระบวนการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="07efe-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="07efe-125">แต่ เขาจะสามารถใช้ความสามารถในการคาดคะเนการชำระเงิน เพื่อตรวจสอบว่าคอลเลกชันเชิงรุกจะปรับปรุงความน่าจะเป็นของการชำระเงินตรงเวลาหรือไม่</span><span class="sxs-lookup"><span data-stu-id="07efe-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="07efe-126">การคาดการณ์การชำระเงินจะช่วยให้ธุรกิจมีข้อมูลที่จำเป็นในการจัดให้มีการเริ่มต้นกระบวนการเรียกเก็บเงินล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="07efe-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="07efe-127">ระเบียบวิธี</span><span class="sxs-lookup"><span data-stu-id="07efe-127">Methodology</span></span>

<span data-ttu-id="07efe-128">การพัฒนาและการจัดวางโซลูชัน AI เป็นเรื่องยาก</span><span class="sxs-lookup"><span data-stu-id="07efe-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="07efe-129">ต้องใช้ทีมนักวิทยาศาสตร์ข้อมูล และผู้เชี่ยวชาญทำงานเป็นระยะเวลานาน เพื่อกำหนด พัฒนา ปรับใช้ และรักษาโซลูชัน AI ที่ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="07efe-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="07efe-130">เรากำลังทำให้การปรับใช้และใช้โซลูชัน AI ในการเงินอย่างง่าย</span><span class="sxs-lookup"><span data-stu-id="07efe-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="07efe-131">เรากำลัง เตรียมรวมบรรจุภัณฑ์โซลูชัน AI ในการเงินที่สร้างขึ้นบน Microsoft AI Builder</span><span class="sxs-lookup"><span data-stu-id="07efe-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="07efe-132">ผู้ใช้คลิกปุ่มเพียงครั้งเดียวก็สามารถจัดวางโซลูชัน AI และเริ่มใช้ประโยชน์จากการคาดคะเนแบบอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="07efe-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="07efe-133">ถ้าองค์กรไม่พอใจกับความถูกต้องของการคาดการณ์ ผู้ใช้ระดับสูงสามารถคลิกอีกครั้ง และสามารถป้อนประสบการณ์การใช้งานของส่วนขยายของ AI builder แล้วเลือก หรือยกเลิกการเลือกฟิลด์ที่ใช้ในการสร้างการคาดคะเน</span><span class="sxs-lookup"><span data-stu-id="07efe-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="07efe-134">เมื่อพร้อมแล้วพวกเขาสามารถฝึกอบรม และเผยแพร่การเปลี่ยนแปลง และแบบจำลองที่ได้รับการฝึกฝนใหม่ จะถูกเลือกโดยอัตโนมัติสำหรับการคาดการณ์ในการเงิน</span><span class="sxs-lookup"><span data-stu-id="07efe-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="07efe-135">วิธีการรับข้อมูลเชิงลึกในการชำระเงินของลูกค้า (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="07efe-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="07efe-136">โปรดอีเมลไปที่ [ทีมการแสดงตัวอย่างในข้อมูลเชิงลึกทางการเงิน (ตัวอย่าง)](mailto:fiap@microsoft.com) ถ้าคุณสนใจที่จะลองข้อมูลเชิงลึกในการชำระเงินของลูกค้า (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="07efe-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="07efe-137">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="07efe-137">Privacy Notice</span></span>

<span data-ttu-id="07efe-138">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการสำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="07efe-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


