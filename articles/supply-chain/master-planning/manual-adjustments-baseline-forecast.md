---
title: ทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐาน
description: หัวข้อนี้อธิบายวิธีการทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐาน และวิธีการดูรายละเอียดของการคาดการณ์
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afdcbb98c96b2a685f64a16886b9a064ed13c2c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967041"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="d08af-103">ทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="d08af-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d08af-104">หัวข้อนี้อธิบายวิธีการทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐาน และวิธีการดูรายละเอียดของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="d08af-105">ก่อนที่คุณจะทำการปรับปรุงด้วยตนเอง สิ่งสำคัญคือคุณเข้าใจแนวความคิดต่างๆในหน้าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="d08af-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="d08af-106">กริดบนหน้าการคาดการณ์ความต้องการที่มีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="d08af-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="d08af-107">หน้า **การคาดการณ์ความต้องการที่มีการปรับปรุง** ประกอบด้วยกริดที่มีโครงสร้างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d08af-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="d08af-108">คอลัมน์แรกแสดงรายการ คีย์การปันส่วนสินค้า บริษัท และอื่นๆ ที่การคาดการณ์ได้ถูกสร้างให้</span><span class="sxs-lookup"><span data-stu-id="d08af-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="d08af-109">หัวข้อย่อยของหน้าแสดงคำอธิบายของมิติการคาดการณ์ปัจจุบันทีถูกแสดงในกริด</span><span class="sxs-lookup"><span data-stu-id="d08af-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="d08af-110">ตัวอย่างเช่น ถ้าหัวข้อย่อยของหน้าเป็น **บริษัท / ไซต์ / คีย์การปันส่วนสินค้า** และอีกส่วนหนึ่งของส่วนหัวของแถวในกริดเป็น **USMF / 1 / D\_Alloc** ซึ่งแถวแสดงการคาดการณ์สำหรับบริษัท USMF ไซต์ 1 และคีย์การปันส่วนสินค้า **D\_Alloc**</span><span class="sxs-lookup"><span data-stu-id="d08af-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="d08af-111">คอลัมน์ในลำดับต่อมาแสดงถึงกลุ่มการคาดการณ์ที่มีการสร้างการคาดการณ์ให้</span><span class="sxs-lookup"><span data-stu-id="d08af-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="d08af-112">ส่วนหัวของคอลัมน์แต่ละส่วนคือ วันที่แรกของกลุ่มการคาดการณ์ที่มีการแสดงคอลัมน์</span><span class="sxs-lookup"><span data-stu-id="d08af-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="d08af-113">ค่าในเซลล์แสดงถึงการคาดการณ์สำหรับสินค้าหนึ่งรายการ คีย์การปันส่วนสินค้า และอื่นๆ สำหรับกลุ่มการคาดการณ์ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d08af-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="d08af-114">การรวมและการแยกการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="d08af-115">หัวข้อย่อยของหน้าแสดงระดับของการรวมการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="d08af-116">ตัวอย่างเช่น ถ้าหัวข้อย่อยของหน้าเป็น **บริษัท / ไซต์ / คีย์การปันส่วน / หมายเลขสินค้า/ สี / ขนาด / การตั้งค่าคอนฟิก / ลักษณะ** จะไม่มีการรวมการคาดการณ์ และการคาดการณ์จะถูกแสดงที่ระดับของสินค้าและมิติ</span><span class="sxs-lookup"><span data-stu-id="d08af-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="d08af-117">เมื่อต้องการเปลี่ยนการรวม ให้ใช้หน้า **เปลี่ยนแปลงมิติการคาดการณ์** ซึ่งคุณสามารถเปิดจากเมนูแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="d08af-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="d08af-118">เมื่อต้องการแก้ไขการคาดการณ์ ให้คลิกในเซลล์ใดๆที่มีอยู่ และพิมพ์ค่าการคาดการณ์ที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="d08af-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="d08af-119">เซลล์ที่แก้ไขแล้วกลายเป็นตัวหนาทันที เพื่อบ่งชี้ว่าการคาดการณ์ที่แสดงไม่ใช่การคาดการณ์ที่บริการการคาดการณ์ความต้องการได้สร้างขึ้น แต่ได้มีการปรับปรุงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d08af-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="d08af-120">ถ้าคุณเปลี่ยนการรวมเพื่อให้หน้าแสดงข้อมูลรวมมากขึ้น คุณสามารถใช้หน้า **รายการการคาดการณ์ความต้องการ** เพื่อดูรายการการคาดการณ์แต่ละรายการที่สร้างการคาดการณ์รวม</span><span class="sxs-lookup"><span data-stu-id="d08af-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="d08af-121">ตัวอย่างเช่น คุณได้สร้างการคาดการณ์ที่ระดับสินค้า แต่คุณทราบว่าความต้องการสำหรับสินค้านี้จะเพิ่มทั่วทั้งไซต์เนื่องจากโปรโมชันหรือเหตุการณ์อื่นที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="d08af-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="d08af-122">ในกรณีนี้ คุณสามารถตั้งค่าการรวมไปยัง **บริษัท / คีย์การปันส่วนสินค้า / สินค้า** ในหน้า **เปลี่ยนมิติการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="d08af-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="d08af-123">คุณสามารถปรับปรุงการคาดการณ์แบบรวมสำหรับสินค้าทั้งหมดทั่วทั้งไซต์ในกริด **การคาดการณ์ความต้องการที่มีการปรับปรุง** ได้</span><span class="sxs-lookup"><span data-stu-id="d08af-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="d08af-124">เมื่อต้องการดูผลกระทบของการเปลี่ยนแปลงของคุณทั่วทั้งไซต์ ให้เปิดหน้า **รายการการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="d08af-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="d08af-125">ในหน้านี้ คุณจะเห็นรายการหนึ่งรายการสำหรับสินค้าสำหรับไซต์แต่ละไซต์ ปริมาณการคาดการณ์ที่ปรับปรุงแล้ว และปริมาณการคาดการณ์ดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="d08af-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="d08af-126">เมื่อมีการปรับปรุงของปริมาณที่คาดการณ์ไว้ที่ระดับรวม ระบบจะใช้การปันส่วนแบบถ่วงน้ำหนักเพื่อกระจายการเปลี่ยนแปลงในรายการที่สร้างการรวม</span><span class="sxs-lookup"><span data-stu-id="d08af-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="d08af-127">คุณยังสามารถทำการปรับปรุงด้วยตนเองในหน้า **รายการการคาดการณ์ความต้องการ** ได้อีกด้วย ด้วยการปรับเปลี่ยนเซลล์ **ปริมาณรวม** ค่า หรือ **ปริมาณ** อย่างใดอย่างหนึ่งในกริดการแยก</span><span class="sxs-lookup"><span data-stu-id="d08af-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="d08af-128">การดูรายละเอียดของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-128">Viewing details of the forecast</span></span>
<span data-ttu-id="d08af-129">คุณสามารถเปิดหน้า **รายละเอียดของการคาดการณ์ความต้องการ** เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับการคาดการณ์ได้</span><span class="sxs-lookup"><span data-stu-id="d08af-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="d08af-130">หน้า **รายละเอียดของการคาดการณ์ความต้องการ** แสดงข้อมูลต่อไปนี้ในรูปแบบตารางและรูปภาพ:</span><span class="sxs-lookup"><span data-stu-id="d08af-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="d08af-131">ความต้องการในอดีตที่การทำนายการคาดการณ์ยึดตาม</span><span class="sxs-lookup"><span data-stu-id="d08af-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="d08af-132">การคาดการณ์ปัจจุบันที่ถูกใช้โดยการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="d08af-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="d08af-133">ค่าการคาดการณ์ความต้องการใหม่และยอดเงินที่พวกเขาได้ปรับปรุงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d08af-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="d08af-134">ช่วงเวลาความเชื่อมั่นสำหรับค่าที่คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="d08af-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="d08af-135">แบบจำลองการคาดการณ์ที่ถูกใช้ในการสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="d08af-136">ถ้าคุณกำลังดูข้อมูลรวม คุณจะเห็นรายการของวิธีการทั้งหมดที่ถูกใช้สำหรับชุดเวลารวมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d08af-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="d08af-137">ความถูกต้องของแบบจำลองภายใน (MAPE)</span><span class="sxs-lookup"><span data-stu-id="d08af-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="d08af-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความถูกต้องการคาดการณ์ ให้ดู [ตรวจสอบความถูกต้องของการคาดการณ์](monitor-forecast-accuracy.md)</span><span class="sxs-lookup"><span data-stu-id="d08af-138">For more information about forecast accuracy, see [Monitor forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="d08af-139">**หมายเหตุ:**</span><span class="sxs-lookup"><span data-stu-id="d08af-139">**Notes:**</span></span>

-   <span data-ttu-id="d08af-140">ถ้าคุณเปิดใช้งาน **การเลือกแบบจำลองการคาดการณ์ในรายละเอียดการคาดการณ์ความต้องการ** จากการจัดการคุณลักษณะ คุณจะสามารถเลือกแบบจำลองการคาดการณ์ที่จะรวมไว้สำหรับการคาดการณ์ในอดีตในหน้า **รายละเอียดการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="d08af-140">If you enable **Forecast model selection on Demand forecast details** from Feature management, you will be able to select the forecast models to be include, for the historical forecast, on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="d08af-141">ช่วงเวลาความเชื่อมั่นที่ปรากฏในส่วน **การคาดการณ์** ของหน้า แสดงถึงความแตกต่างระหว่างขีดจำกัดบนของช่วงเวลาความน่าเชื่อถือและขีดจำกัดล่างของช่วงเวลาความน่าเชื่อถือ</span><span class="sxs-lookup"><span data-stu-id="d08af-141">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="d08af-142">เมื่อต้องการดูค่าสำหรับขีดจำกัดบนและล่าง ให้วางเมาส์ไว้เหนือแผนภูมิในส่วน **ความต้องการและการคาดการณ์ในอดีตแบบกราฟิก**</span><span class="sxs-lookup"><span data-stu-id="d08af-142">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="d08af-143">ถ้าคุณใช้การคาดการณ์ความต้องการ Microsoft Azure Machine Learning คุณสามารถระบุเปอร์เซนต์ระดับความมั่นใจที่การคาดการณ์ที่ถูกสร้างควรมี</span><span class="sxs-lookup"><span data-stu-id="d08af-143">If you use the Demand forecasting Microsoft Azure Machine Learning, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="d08af-144">ช่วงเวลาความเชื่อมั่นประกอบด้วยช่วงของค่าที่ทำหน้าที่เป็นการประเมินที่ดีสำหรับการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="d08af-144">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="d08af-145">เปอร์เซ็นต์ระดับความเชื่อมั่น 95% บ่งชี้ว่ามีความเสี่ยง 5% ที่การคาดการณ์ความต้องการจะอยู่นอกช่วงเวลาความเชื่อมั่น</span><span class="sxs-lookup"><span data-stu-id="d08af-145">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="d08af-146">คุณยังสามารถทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์ในหน้า **รายละเอียดการคาดการณ์ความต้องการ** ด้วยการปรับเปลี่ยนค่าในแถว **การคาดการณ์** ในส่วน **การคาดการณ์** ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="d08af-146">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d08af-147">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d08af-147">Additional resources</span></span>
--------

[<span data-ttu-id="d08af-148">ตรวจสอบความถูกต้องของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d08af-148">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="d08af-149">สร้างการคาดการณ์พื้นฐานทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="d08af-149">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



