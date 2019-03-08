---
title: นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ
description: เพื่อให้ได้การคาดการณ์ความต้องการที่ถูกต้อง คุณจำเป็นต้องมีข้อมูลความต้องการในอดีตสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า หัวข้อนี้อธิบายวิธีการใช้เอนทิตี้ข้อมูลเพื่อนำเข้าข้อมูลความต้องการในอดีตจากระบบใด ๆ เพื่อให้คุณทราบประวัติของข้อมูลการคาดการณ์ความต้องการที่ยาวนานขึ้น
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "328619"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="92ae8-104">นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="92ae8-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92ae8-105">เพื่อช่วยในการรับรองความถูกต้องของการคาดการณ์ความต้องการ คุณต้องมีข้อมูลความต้องการในอดีตที่มากเท่ากับข้อมูลที่คุณสามารถได้รับสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="92ae8-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="92ae8-106">ถ้าข้อมูลความต้องการที่ผ่านมาไม่ได้ถูกนำเข้าอยู่แล้ว ใช้เอนทิตีข้อมูล **ความต้องการภายนอกที่ผ่านมา** (ReqDemPlanHistoricalExternalDemandEntity) ใน Microsoft Dynamics 365 for Finance and Operations เพื่อนำเข้า</span><span class="sxs-lookup"><span data-stu-id="92ae8-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="92ae8-107">ในพื้นที่ทำงาน **การจัดการข้อมูล** คุณสามารถดูภาพรวมของฟิลด์ทั้งหมดในเอนทิตี้ได้</span><span class="sxs-lookup"><span data-stu-id="92ae8-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="92ae8-108">เปิดพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92ae8-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="92ae8-109">คลิกไทล์ **เอนทิตี้ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92ae8-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="92ae8-110">ค้นหารายการเอนทิตี้สำหรับ **ความต้องการภายนอกในอดีต**</span><span class="sxs-lookup"><span data-stu-id="92ae8-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="92ae8-111">คลิก **ฟิลด์เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="92ae8-111">Click **Target fields**.</span></span> <span data-ttu-id="92ae8-112">ฟิลด์เอนทิตี้ต่อไปนี้เป็นฟิลด์บังคับ: ไซต์ (**DeliveringSiteId**) วันที่ (**DemandDate**) ปริมาณ (**DemandQuantity**) และหมายเลขสินค้า (**ItemNumber**) หรือคีย์การปันส่วนสินค้า (**ProductAllocationKeyId**) อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="92ae8-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="92ae8-113">เพื่อใช้เอนทิตีข้อมูล คุณต้องมีไฟล์ Microsoft Excel หรือไฟล์ค่าที่คั่นด้วยจุลภาค (CSV) ที่ประกอบด้วยข้อมูลความต้องการที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="92ae8-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="92ae8-114">ตัวอย่างต่อไปนี้แสดงวิธีการนำเข้าข้อมูลจากไฟล์ CSV</span><span class="sxs-lookup"><span data-stu-id="92ae8-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="92ae8-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="92ae8-115">Example</span></span>

<span data-ttu-id="92ae8-116">คุณสามารถใช้ไฟล์ต่อไปนี้เป็นตัวอย่างได้</span><span class="sxs-lookup"><span data-stu-id="92ae8-116">You can use the following file as an example.</span></span> <span data-ttu-id="92ae8-117">ดาวน์โหลด [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast)</span><span class="sxs-lookup"><span data-stu-id="92ae8-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="92ae8-118">ไฟล์นี้ประกอบด้วยข้อมูลความต้องการในอดีตสำหรับสินค้า D0001</span><span class="sxs-lookup"><span data-stu-id="92ae8-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="92ae8-119">ซึ่งประกอบด้วยฟิลด์บังคับต่อไปนี้เท่านั้น: ไซต์ ปริมาณ และวันที่ของความต้องการ</span><span class="sxs-lookup"><span data-stu-id="92ae8-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="92ae8-120">เลือกบริษัทที่จะนำเข้าข้อมูลความต้องการในอดีต</span><span class="sxs-lookup"><span data-stu-id="92ae8-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="92ae8-121">เปิดพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="92ae8-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="92ae8-122">คลิกไทล์ **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="92ae8-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="92ae8-123">ป้อนชื่อสำหรับโครงการนำเข้า เช่น **นำเข้าความต้องการในอดีตสำหรับสินค้า D0001**</span><span class="sxs-lookup"><span data-stu-id="92ae8-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="92ae8-124">ในฟิลด์ **รูปแบบข้อมูลต้นทาง** เลือกรูปแบบไฟล์ของไฟล์ที่คุณกำลังนำเข้า</span><span class="sxs-lookup"><span data-stu-id="92ae8-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="92ae8-125">เมื่อต้องการนำเข้าไฟล์ HistoricalDemandData สำหรับตัวอย่างนี้ เลือก **CSV**</span><span class="sxs-lookup"><span data-stu-id="92ae8-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="92ae8-126">ในฟิลด์ **ชื่อเอนทิตี้** เลือก **ความต้องการภายนอกในอดีต**</span><span class="sxs-lookup"><span data-stu-id="92ae8-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="92ae8-127">บันทึกไฟล์ลงในคอมพิวเตอร์ของคุณ แล้วอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="92ae8-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="92ae8-128">คลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="92ae8-128">Click **Import**.</span></span>
9. <span data-ttu-id="92ae8-129">หน้า **สรุปการดำเนินการ** เปิดขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="92ae8-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="92ae8-130">ตรวจสอบข้อมูลที่นำเข้าบนหน้า</span><span class="sxs-lookup"><span data-stu-id="92ae8-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="92ae8-131">หลังจากที่คุณนำเข้าข้อมูลความต้องการในอดีต คุณสามารถสร้างการคาดการณ์ความต้องการได้</span><span class="sxs-lookup"><span data-stu-id="92ae8-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92ae8-132">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="92ae8-132">Additional resources</span></span>

[<span data-ttu-id="92ae8-133">สร้างการคาดการณ์พื้นฐานทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="92ae8-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
