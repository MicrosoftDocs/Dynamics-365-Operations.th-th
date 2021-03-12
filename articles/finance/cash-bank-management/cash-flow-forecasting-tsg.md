---
title: การแก้ไขปัญหาการตั้งค่าการคาดการณ์กระแสเงินสด
description: หัวข้อนี้ให้คำตอบแก่คำถามที่คุณอาจมีเมื่อคุณตั้งค่าคอนฟิกการคาดการณ์กระแสเงินสด เป็นการมุ่งประเด็นคำถามที่พบบ่อย (FAQ) เกี่ยวกับการตั้งค่าของกระแสเงินสด การอัพเดตกระแสเงินสด และ Power BI กระแสเงินสด
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985298"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="5aa03-104">การแก้ไขปัญหาการตั้งค่าการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="5aa03-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa03-105">หัวข้อนี้ให้คำตอบแก่คำถามที่คุณอาจมีเมื่อคุณตั้งค่าคอนฟิกการคาดการณ์กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="5aa03-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="5aa03-106">เป็นการมุ่งประเด็นคำถามที่พบบ่อย (FAQ) เกี่ยวกับการตั้งค่าของกระแสเงินสด การอัพเดตกระแสเงินสด และ Power BI กระแสเงินสด</span><span class="sxs-lookup"><span data-stu-id="5aa03-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="5aa03-107">เพราะเหตุใดกระแสเงินสดจึงแสดงขึ้นเฉพาะนิติบุคคลเพียงแห่งเดียว</span><span class="sxs-lookup"><span data-stu-id="5aa03-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="5aa03-108">การคาดการณ์กระแสเงินสดมีการตั้งค่าคอนฟิกและคํานวณได้ต่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="5aa03-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="5aa03-109">รายงาน Power BI และความสามารถของการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกของ Finance แสดงอยู่ในผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="5aa03-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="5aa03-110">ต้องมีการตั้งค่าการคาดการณ์กระแสเงินสดให้กับแต่ละนิติบุคคลที่คุณต้องการดูการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="5aa03-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="5aa03-111">รีวิวการตั้งค่าคอนฟิกของการคาดการณ์กระแสเงินสดในนิติบุคคลของคุณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5aa03-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="5aa03-112">หรือรีวิวการตั้งค่าคอนฟิกของนิติบุคคลทั้งหมดเพื่อการคาดการณ์กระแสเงินสด และตรวจสอบให้แน่ใจว่าได้ตั้งค่านิติบุคคลตามที่คุณกําหนดไว้</span><span class="sxs-lookup"><span data-stu-id="5aa03-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="5aa03-113">เพราะเหตุใด Power BI จึงไม่ได้แสดงข้อมูลกระแสเงินสดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="5aa03-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="5aa03-114">ต้องผ่านขั้นตอนหลายขั้นตอนก่อนที่การคาดการณ์กระแสเงินสดจะสามารถปรากฏในมุมมอง Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="5aa03-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="5aa03-115">รีวิวรายการตรวจสอบต่อไปนี้ และตรวจสอบให้แน่ใจว่าขั้นตอนทุกขั้นตอนเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="5aa03-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="5aa03-116">ตั้งค่ากระแสเงินสดให้กับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="5aa03-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="5aa03-117">ในพารามิเตอร์บัญชีแยกประเภททั่วไป ให้ตั้งค่าสกุลเงินของระบบและชนิดอัตราแลกเปลี่ยนของระบบ</span><span class="sxs-lookup"><span data-stu-id="5aa03-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="5aa03-118">ตั้งค่าสกุลเงินทางบัญชีของบัญชีแยกประเภทและชนิดอัตราแลกเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="5aa03-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="5aa03-119">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินของธุรกรรมและสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="5aa03-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="5aa03-120">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินทางบัญชีและสกุลเงินของระบบ</span><span class="sxs-lookup"><span data-stu-id="5aa03-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="5aa03-121">ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินทางบัญชีและสกุลเงินของแต่ละธนาคาร</span><span class="sxs-lookup"><span data-stu-id="5aa03-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="5aa03-122">เพราะเหตุใดกระแสเงินสด Power BI จึงใช้งานในเวอร์ชันก่อนหน้านี้ แต่ขณะนี้ว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="5aa03-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="5aa03-123">ตรวจสอบว่า "การวัดกระแสเงินสด V2" และ การวัด "LedgerCovLiquidityMeasurement" จากที่จัดเก็บเอนทิตีได้รับการตั้งค่าคอนฟิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="5aa03-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="5aa03-124">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งานข้อมูลในที่จัดเก็บเอนทิตี โปรดดูที่ [การรวม Power BI กับที่จัดเก็บเอนทิตี](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) ตรวจสอบว่าขั้นตอนทั้งหมดที่ต้องใช้ในการดูเนื้อหา Power BI เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="5aa03-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="5aa03-125">สำหรับข้อมูลเพิ่มเติม โปรดดู [เนื้อหาของ Power BI เกี่ยวกับภาพรวมของเงินสด](Cash-Overview-Power-BI-content.md)</span><span class="sxs-lookup"><span data-stu-id="5aa03-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="5aa03-126">เอนทิตีที่อยู่ที่จัดเก็บเอนทิตีได้รับการรีเฟรชแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5aa03-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="5aa03-127">คุณต้องรีเฟรชเอนทิตีเป็นระยะๆ เพื่อให้แน่ใจว่าข้อมูลเป็นปัจจุบันและถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5aa03-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="5aa03-128">เมื่อต้องการรีเฟรชเอนทิตีเฉพาะด้วยตนเอง ให้ไปที่ **การจัดการระบบ \> การตั้งค่า \>ที่จัดเก็บเอนทิตี** เลือกเอนทิตี แล้วเลือก **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="5aa03-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="5aa03-129">ข้อมูลยังสามารถอัพเดตได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="5aa03-129">The data can also be updated automatically.</span></span> <span data-ttu-id="5aa03-130">ในหน้า **จัดเก็บเอนทิตี** ให้ตั้งค่าตัวเลือก **เปิดใช้งานการรีเฟรชโดยอัตโนมัติ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5aa03-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
