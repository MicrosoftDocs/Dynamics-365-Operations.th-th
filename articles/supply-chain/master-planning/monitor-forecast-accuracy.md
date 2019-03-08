---
title: ตรวจสอบความถูกต้องของการคาดการณ์
description: บทความนี้อธิบายชนิดของความแม่นยำในการคาดการณ์ที่ Microsoft Dynamics 365 for Finance and Operations คำนวณ และอธิบายวิธีการที่คุณสามารถดูค่าความแม่นยำได้
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7070c15f9ee23cfdba871af68d1fc5954735651
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "356426"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="2f563-103">ตรวจสอบความถูกต้องของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="2f563-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f563-104">บทความนี้อธิบายชนิดของความแม่นยำในการคาดการณ์ที่ Microsoft Dynamics 365 for Finance and Operations คำนวณ และอธิบายวิธีการที่คุณสามารถดูค่าความแม่นยำได้</span><span class="sxs-lookup"><span data-stu-id="2f563-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="2f563-105">Finance and Operations คำนวณชนิดของความถูกต้องของการคาดการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2f563-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="2f563-106">ความถูกต้องของการคาดการณ์ในอดีต โดยการเปรียบเทียบการคาดการณ์ในอดีตที่การวางแผนหลักใช้กับความต้องการในอดีต</span><span class="sxs-lookup"><span data-stu-id="2f563-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="2f563-107">เมื่อต้องการดูค่า (ทั้งค่าสัมบูรณ์และค่าเปอร์เซ็นต์) สำหรับความถูกต้องของการคาดการณ์ในอดีต ให้คลิก **แสดงความถูกต้อง** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="2f563-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="2f563-108">ความถูกต้องที่มีการประเมินของแบบจำลองการคาดการณ์ที่ใช้ในการสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="2f563-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="2f563-109">คุณสามารถดูเปอร์เซ็นต์ความถูกต้องภายใต้ **รายละเอียดแบบจำลอง - MAPE** ในหน้า **รายละเอียดของการคาดการณ์ความต้องการ** ได้</span><span class="sxs-lookup"><span data-stu-id="2f563-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="2f563-110">**หมายเหตุ:** ถ้าคุณใช้ Finance and Operations Demand forecasting Microsoft Azure Machine Learning service การคำนวณของความแม่นยำของแบบจำลองภายในขึ้นอยู่กับชุดข้อมูลทดสอบ</span><span class="sxs-lookup"><span data-stu-id="2f563-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="2f563-111">เมื่อต้องการระบุขนาดของชุดข้อมูลการทดสอบ ให้ตั้งค่าพารามิเตอร์ **TEST\_SET\_SIZE\_PERCENT** ในหน้า **พารามิเตอร์การคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="2f563-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="2f563-112">ตัวอย่างเช่น ถ้าคุณตั้งค่าเป็น **20**, 20 เปอร์เซ็นต์สุดท้ายของข้อมูลในอดีตจะถูกใช้ในการคำนวณความถูกต้องของแบบจำลองภายใน</span><span class="sxs-lookup"><span data-stu-id="2f563-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="2f563-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2f563-113">Additional resources</span></span>
--------

[<span data-ttu-id="2f563-114">การอนุมัติการคาดการณ์ที่มีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="2f563-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="2f563-115">ลบจุดนอกขอบเขตออกจากข้อมูลในอดีตเกี่ยวกับธุรกรรมเมื่อคำนวณความต้องการการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="2f563-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



