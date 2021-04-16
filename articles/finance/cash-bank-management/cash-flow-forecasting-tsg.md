---
title: การแก้ไขปัญหาการตั้งค่าการคาดการณ์กระแสเงินสด
description: หัวข้อนี้ให้คำตอบแก่คำถามที่คุณอาจมีเมื่อคุณตั้งค่าคอนฟิกการคาดการณ์กระแสเงินสด เป็นการมุ่งประเด็นคำถามที่พบบ่อย (FAQ) เกี่ยวกับการตั้งค่าของกระแสเงินสด การอัพเดตกระแสเงินสด และ Power BI กระแสเงินสด
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827325"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="9b52e-104">การแก้ไขปัญหาการตั้งค่าการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9b52e-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b52e-105">หัวข้อนี้ให้คำตอบแก่คำถามที่คุณอาจมีเมื่อคุณตั้งค่าคอนฟิกการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9b52e-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="9b52e-106">เป็นการมุ่งประเด็นคำถามที่พบบ่อย (FAQ) เกี่ยวกับการตั้งค่าของกระแสเงินสด การอัพเดตกระแสเงินสด และ Power BI กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9b52e-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="9b52e-107">เพราะเหตุใดกระแสเงินสดจึงแสดงขึ้นเฉพาะนิติบุคคลเพียงแห่งเดียว</span><span class="sxs-lookup"><span data-stu-id="9b52e-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="9b52e-108">การคาดการณ์กระแสเงินสดมีการตั้งค่าคอนฟิกและคํานวณได้ต่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9b52e-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="9b52e-109">รายงาน Power BI และความสามารถของการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกของ Finance แสดงอยู่ในผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="9b52e-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="9b52e-110">ต้องมีการตั้งค่าการคาดการณ์กระแสเงินสดให้กับแต่ละนิติบุคคลที่คุณต้องการดูการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="9b52e-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="9b52e-111">รีวิวการตั้งค่าคอนฟิกของการคาดการณ์กระแสเงินสดในนิติบุคคลของคุณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9b52e-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="9b52e-112">หรือรีวิวการตั้งค่าคอนฟิกของนิติบุคคลทั้งหมดเพื่อการคาดการณ์กระแสเงินสด และตรวจสอบให้แน่ใจว่าได้ตั้งค่านิติบุคคลตามที่คุณกําหนดไว้</span><span class="sxs-lookup"><span data-stu-id="9b52e-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="9b52e-113">เพราะเหตุใด Power BI จึงไม่ได้แสดงข้อมูลกระแสเงินสดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9b52e-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="9b52e-114">ต้องผ่านขั้นตอนหลายขั้นตอนก่อนที่การคาดการณ์กระแสเงินสดจะสามารถปรากฏในมุมมอง Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="9b52e-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="9b52e-115">รีวิวรายการตรวจสอบต่อไปนี้ และตรวจสอบให้แน่ใจว่าขั้นตอนทุกขั้นตอนเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="9b52e-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="9b52e-116">ตั้งค่ากระแสเงินสดให้กับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9b52e-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="9b52e-117">ในพารามิเตอร์บัญชีแยกประเภททั่วไป ให้ตั้งค่าสกุลเงินของระบบและชนิดอัตราแลกเปลี่ยนของระบบ</span><span class="sxs-lookup"><span data-stu-id="9b52e-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="9b52e-118">ตั้งค่าสกุลเงินทางบัญชีของบัญชีแยกประเภทและชนิดอัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="9b52e-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="9b52e-119">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินของธุรกรรมและสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="9b52e-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="9b52e-120">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินทางบัญชีและสกุลเงินของระบบ</span><span class="sxs-lookup"><span data-stu-id="9b52e-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="9b52e-121">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินทางบัญชีและสกุลเงินของแต่ละธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9b52e-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="9b52e-122">เพราะเหตุใดกระแสเงินสด Power BI จึงใช้งานในเวอร์ชันก่อนหน้านี้ แต่ขณะนี้ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="9b52e-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="9b52e-123">ตรวจสอบว่า "การวัดกระแสเงินสด V2" และ การวัด "LedgerCovLiquidityMeasurement" จากที่จัดเก็บเอนทิตีได้รับการตั้งค่าคอนฟิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9b52e-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="9b52e-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับข้อมูลในเอนทิตี ดูที่ [การรวม Power BI กับที่จัดเก็บเอนทิตี](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="9b52e-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="9b52e-125">ตรวจสอบว่าขั้นตอนทั้งหมดที่ต้องใช้เพื่อดูเนื้อหา Power BI เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="9b52e-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="9b52e-126">สำหรับข้อมูลเพิ่มเติม โปรดดู [เนื้อหาของ Power BI เกี่ยวกับภาพรวมของเงินสด](Cash-Overview-Power-BI-content.md)</span><span class="sxs-lookup"><span data-stu-id="9b52e-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="9b52e-127">เอนทิตีที่อยู่ที่จัดเก็บเอนทิตีได้รับการรีเฟรชแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9b52e-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="9b52e-128">คุณต้องรีเฟรชเอนทิตีเป็นระยะๆ เพื่อให้แน่ใจว่าข้อมูลเป็นปัจจุบันและถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="9b52e-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="9b52e-129">เมื่อต้องการรีเฟรชเอนทิตีเฉพาะด้วยตนเอง ให้ไปที่ **การจัดการระบบ \> การตั้งค่า \>ที่จัดเก็บเอนทิตี** เลือกเอนทิตี แล้วเลือก **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="9b52e-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="9b52e-130">ข้อมูลยังสามารถอัพเดตได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9b52e-130">The data can also be updated automatically.</span></span> <span data-ttu-id="9b52e-131">ในหน้า **จัดเก็บเอนทิตี** ให้ตั้งค่าตัวเลือก **เปิดใช้งานการรีเฟรชโดยอัตโนมัติ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9b52e-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="9b52e-132">ควรใช้วิธีการคํานวณวิธีใด เมื่อคํานวณการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="9b52e-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="9b52e-133">วิธีการคํานวณการคาดการณ์กระแสเงินสดมีตัวเลือกสองตัวเลือกที่สําคัญ</span><span class="sxs-lookup"><span data-stu-id="9b52e-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="9b52e-134">ตัวเลือก **ใหม่** จะคํานวณการคาดการณ์กระแสเงินสดสำหรับเอกสารและเอกสารใหม่ที่เปลี่ยนแปลงไปนับตั้งแต่การรันชุดงานล่าสุด</span><span class="sxs-lookup"><span data-stu-id="9b52e-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="9b52e-135">ตัวเลือกนี้มีแนวโน้มที่จะรันได้เร็วขึ้น เนื่องจากจะประมวลผลชุดย่อยของเอกสารที่มีขนาดเล็กลง</span><span class="sxs-lookup"><span data-stu-id="9b52e-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="9b52e-136">ตัวเลือก **ยอดรวม** จะคำนวณการคาดการณ์กระแสเงินสดใหม่สำหรับเอกสารทุกฉบับในระบบ</span><span class="sxs-lookup"><span data-stu-id="9b52e-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="9b52e-137">ตัวเลือกนี้จะใช้เวลามากขึ้น เนื่องจากมีงานมากขึ้นที่จะต้องดำเนินการให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9b52e-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="9b52e-138">ฉันจะปรับปรุงประสิทธิภาพของการคาดการณ์กระแสเงินสดของชุดงานที่เกิดซ้ำอย่างไร</span><span class="sxs-lookup"><span data-stu-id="9b52e-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="9b52e-139">เราขอแนะนาให้รันการคาดการณ์กระแสเงินสดของคุณวันละครั้งในช่วงเวลาที่ระบบมีปริมาณงานไม่มาก โดยใช้วิธีการคํานวณ **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9b52e-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="9b52e-140">เราขอแนะนาให้ใช้วิธีการนี้หกวันต่อสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="9b52e-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="9b52e-141">จากนั้น รันการคาดการณ์กระแสเงินสดสัปดาห์ละครั้ง โดยใช้วิธีการคํานวณ **ผลรวม** ในวันที่มีจํานวนกิจกรรมน้อยที่สุด</span><span class="sxs-lookup"><span data-stu-id="9b52e-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

