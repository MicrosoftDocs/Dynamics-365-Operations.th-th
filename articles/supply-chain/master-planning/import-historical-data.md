---
title: นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ
description: เพื่อให้ได้การคาดการณ์ความต้องการที่ถูกต้อง คุณจำเป็นต้องมีข้อมูลความต้องการในอดีตสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า หัวข้อนี้อธิบายวิธีการใช้เอนทิตี้ข้อมูลเพื่อนำเข้าข้อมูลความต้องการในอดีตจากระบบใด ๆ เพื่อให้คุณทราบประวัติของข้อมูลการคาดการณ์ความต้องการที่ยาวนานขึ้น
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301661"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="6f699-104">นำเข้าข้อมูลในอดีตสำหรับการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="6f699-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f699-105">เพื่อช่วยในการรับรองความถูกต้องของการคาดการณ์ความต้องการ คุณต้องมีข้อมูลความต้องการในอดีตที่มากเท่ากับข้อมูลที่คุณสามารถได้รับสำหรับแต่ละสินค้าหรือคีย์การปันส่วนสินค้า</span><span class="sxs-lookup"><span data-stu-id="6f699-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="6f699-106">ถ้าข้อมูลความต้องการที่ผ่านมาไม่ได้ถูกนำเข้าอยู่แล้ว ใช้เอนทิตีข้อมูล **ความต้องการภายนอกที่ผ่านมา** (ReqDemPlanHistoricalExternalDemandEntity) ใน Dynamics 365 Supply Chain Management เพื่อนำเข้า</span><span class="sxs-lookup"><span data-stu-id="6f699-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="6f699-107">ในพื้นที่ทำงาน **การจัดการข้อมูล** คุณสามารถดูภาพรวมของฟิลด์ทั้งหมดในเอนทิตี้ได้</span><span class="sxs-lookup"><span data-stu-id="6f699-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="6f699-108">เปิดพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6f699-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="6f699-109">เลือกไทล์ **เอนทิตี้ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6f699-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="6f699-110">ค้นหารายการเอนทิตี้สำหรับ **ความต้องการภายนอกในอดีต**</span><span class="sxs-lookup"><span data-stu-id="6f699-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="6f699-111">เลือก **ฟิลด์เป้าหมาย**</span><span class="sxs-lookup"><span data-stu-id="6f699-111">Select **Target fields**.</span></span> <span data-ttu-id="6f699-112">ฟิลด์เอนทิตี้ต่อไปนี้เป็นฟิลด์บังคับ: ไซต์ (**DeliveringSiteId**) วันที่ (**DemandDate**) ปริมาณ (**DemandQuantity**) และหมายเลขสินค้า (**ItemNumber**) หรือคีย์การปันส่วนสินค้า (**ProductAllocationKeyId**) อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6f699-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="6f699-113">เพื่อใช้เอนทิตีข้อมูล คุณต้องมีไฟล์ Microsoft Excel หรือไฟล์ค่าที่คั่นด้วยจุลภาค (CSV) ที่ประกอบด้วยข้อมูลความต้องการที่ผ่านมา</span><span class="sxs-lookup"><span data-stu-id="6f699-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="6f699-114">ตัวอย่างต่อไปนี้แสดงวิธีการนำเข้าข้อมูลจากไฟล์ CSV</span><span class="sxs-lookup"><span data-stu-id="6f699-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="6f699-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการนําเข้าข้อมูล รวมถึงวิธีการล้างข้อมูลหลังจากการนําเข้า โปรดดู [ภาพรวมของงานการนําเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) และหัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6f699-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="6f699-116">ดูเพิ่มเติมที่ [สร้างการคาดการณ์พื้นฐานทางสถิติ](generate-statistical-baseline-forecast.md)</span><span class="sxs-lookup"><span data-stu-id="6f699-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]