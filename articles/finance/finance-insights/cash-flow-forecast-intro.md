---
title: การคาดการณ์กระแสเงินสด (พรีวิว)
description: หัวข้อนี้จะอธิบายความสามารถในการคาดการณ์กระแสเงินสด
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186551"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="280bc-103">การคาดการณ์กระแสเงินสด (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="280bc-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="280bc-104">กระแสเงินสดมีความสำคัญต่อธุรกิจใดๆ</span><span class="sxs-lookup"><span data-stu-id="280bc-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="280bc-105">แม้บริษัทที่ทำกำไรก็อาจพบกับความล้มเหลวได้ ถ้าไม่มีการรักษากระแสเงินสดเพื่อตอบสนองความต้องการในทันที</span><span class="sxs-lookup"><span data-stu-id="280bc-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="280bc-106">ความสามารถในการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึก Finance สามารถช่วยบริษัทตรวจสอบและจัดการยอดดุลเงินสดได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="280bc-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="280bc-107">คุณลักษณะนี้ใช้การเรียนรู้ของเครื่องเพื่อช่วยธุรกิจในการคาดการณ์กระแสเงินสดได้อย่างถูกต้องมากกว่าที่มีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="280bc-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="280bc-108">นอกจากนี้ คุณยังสามารถช่วยผู้จัดการตัดสินใจที่จะปรับโอกาสให้เหมาะสมในเนื้อหาของตำแหน่งเงินสดปัจจุบันของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="280bc-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="280bc-109">สำหรับบริษัทส่วนใหญ่ การจัดการกระแสเงินสดและการรันการคาดการณ์กระแสเงินสดเป็นกระบวนการที่น่าเบื่อและซ้ำซากและเป็นแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="280bc-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="280bc-110">บริษัทส่วนใหญ่อาศัยโซลูชัน Microsoft Excel ที่มีระดับความซับซ้อนที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="280bc-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="280bc-111">ความท้าทายของการคาดการณ์กระแสเงินสดอย่างถูกต้องรวมถึงรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="280bc-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="280bc-112">ข้อมูลไม่พร้อมใช้งานสำหรับผู้ที่ตัดสินใจ เนื่องจากมีการกระจายอยู่หลายแห่ง ซึ่งรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="280bc-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="280bc-113">ระบบการวางแผนทรัพยากรการบัญชีหรือองค์กร</span><span class="sxs-lookup"><span data-stu-id="280bc-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="280bc-114">ซอฟต์แวร์วางแผนทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="280bc-114">Financial planning software</span></span>
  - <span data-ttu-id="280bc-115">Excel</span><span class="sxs-lookup"><span data-stu-id="280bc-115">Excel</span></span>
  - <span data-ttu-id="280bc-116">แอปพลิเคชันซอฟต์แวร์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="280bc-116">Additional software applications</span></span> 
- <span data-ttu-id="280bc-117">การคาดการณ์จะขึ้นอยู่กับความรู้ภายในที่อยู่ใน "ไซโล" ภายในแต่ละโดเมนหรือแผนก</span><span class="sxs-lookup"><span data-stu-id="280bc-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="280bc-118">การวัดความถูกต้องของการคาดการณ์กระแสเงินสดหลังจากที่มีการรับรู้ทางการเงินแล้ว จะไม่มีความแน่นอนและยาก</span><span class="sxs-lookup"><span data-stu-id="280bc-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="280bc-119">รายละเอียดของความสามารถในการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="280bc-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="280bc-120">คุณลักษณะการคาดการณ์กระแสเงินสดจะมีฟังก์ชันดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="280bc-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="280bc-121">ทำให้สามารถรวมข้อมูลกระแสเงินสดจากระบบภายนอกไปยัง Dynamics 365 Finance เป็นเรื่องง่าย</span><span class="sxs-lookup"><span data-stu-id="280bc-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="280bc-122">นอกจากนี้ การคาดการณ์กระแสเงินสดยังสามารถใช้กรอบงานการนำเข้า-ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="280bc-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="280bc-123">กรอบงานนี้ช่วยให้การรวมกับ Excel OData ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="280bc-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="280bc-124">นอกจากนี้ คุณยังสามารถรวมข้อมูลจากแหล่งที่มาต่างๆ เพื่อสร้างโซลูชันกระแสเงินสดที่ครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="280bc-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="280bc-125">นำเสนอตำแหน่งเงินสดอัจฉริยะ</span><span class="sxs-lookup"><span data-stu-id="280bc-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="280bc-126">ตำแหน่งเงินสดถูกสร้างขึ้นตามพฤติกรรมการชำระเงินของลูกค้า เพื่อคาดการณ์เวลาที่บริษัทสามารถคาดหวังเงินสดที่จะมาถึงในบัญชีของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="280bc-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="280bc-127">นอกจากนี้ ยังวิเคราะห์รูปแบบในอดีตของผู้จัดจำหน่ายที่ชำระเงิน เพื่อคาดการณ์เวลาที่น่าจะมีการชำระใบแจ้งหนี้และใบสั่งในอนาคต</span><span class="sxs-lookup"><span data-stu-id="280bc-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="280bc-128">แสดงการคาดการณ์กระแสเงินสดอัจฉริยะสำหรับการคาดการณ์ระยะยาว โดยใช้การคาดการณ์ชุดเวลาโดยใช้การรวมแบบอัตโนมัติกับ AI Builder</span><span class="sxs-lookup"><span data-stu-id="280bc-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="280bc-129">มีความสามารถในการบันทึกตำแหน่งของกระแสเงินสดหรือการคาดการณ์เฉพาะ แก้ไข แล้วจากนั้น เปรับเทียบและวัดประสิทธิภาพของการคาดการณ์กับการเงินจริงอย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="280bc-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="280bc-130">เปิดใช้งานการวิเคราะห์ what-if โดยใช้การเปรียบเทียบสแนปช็อต</span><span class="sxs-lookup"><span data-stu-id="280bc-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="280bc-131">ตัวอย่างเช่น คุณสามารถสร้างสแนปช็อตหลายรายการซึ่งแสดงถึงในมุมมองเชิงบวก เชิงลบ และสมจริงที่สุด ของกระแสเงินสดของคุณ แล้วจากนั้น เปรียบเทียบและดูความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="280bc-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="280bc-132">มีความสามารถในการดูการคาดการณ์กระแสเงินสดในหลายสกุลเงิน ระหว่างนิติบุคคล และกรองข้อมูลและดูกระแสเงินสดที่เกี่ยวข้องกับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="280bc-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="280bc-133">ช่วยให้คุณสามารถกรองข้อมูลและดูบัญชีธนาคารที่เกี่ยวข้องกับมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="280bc-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="280bc-134">ฟังก์ชันการคาดการณ์กระแสเงินสดใน Dynamics 365 Finance จะช่วยให้องค์กรของคุณสามารถแปลงการคาดการณ์กระแสเงินสดที่น่าเบื่อ ซับซ้อน และซ้ำซาก เป็นกระบวนการแบบอัตโนมัติที่ง่ายได้</span><span class="sxs-lookup"><span data-stu-id="280bc-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="280bc-135">การทำให้การคาดการณ์กระแสเงินสดที่น่าเบื่อมากที่สุดเป็นแบบอัตโนมัติ จะช่วยให้คุณสามารถมุ่งเน้นไปที่การตัดสินใจที่สำคัญที่จะขับเคลื่อนผลลัพธ์ทางธุรกิจที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="280bc-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="280bc-136">การตั้งค่ามิติสำหรับการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="280bc-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="280bc-137">แท็บใหม่บนหน้า **การตั้งค่าการคาดการณ์กระแสเงินสด** ช่วยให้คุณสามารถควบคุมมิติทางการเงินที่จะใช้สำหรับการกรองในพื้นที่ทำงาน **การคาดการณ์กระแสเงินสด**</span><span class="sxs-lookup"><span data-stu-id="280bc-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="280bc-138">แท็บนี้จะปรากฏเฉพาะเมื่อมีการเปิดใช้งานคุณลักษณะการคาดการณ์กระแสเงินสดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="280bc-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="280bc-139">บนแท็บ **มิติ** ให้เลือกจากรายการของมิติที่จะใช้สำหรับการกรองข้อมูล และใช้คีย์ลูกศรเพื่อย้ายไปที่คอลัมน์ด้านขวา</span><span class="sxs-lookup"><span data-stu-id="280bc-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="280bc-140">สามารถเลือกได้เพียงสองมิติเท่านั้นสำหรับการกรองข้อมูลการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="280bc-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
