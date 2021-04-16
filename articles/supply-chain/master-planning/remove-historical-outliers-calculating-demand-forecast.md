---
title: ลบจุดนอกขอบเขตออกจากข้อมูลในอดีตเกี่ยวกับธุรกรรมเมื่อคำนวณความต้องการการคาดการณ์
description: บทความนี้อธิบายวิธีการแยกจุดนอกขอบเขตจากข้อมูลในอดีตที่ใช้ในการคำนวณความต้องการการคาดการณ์ออก โดยไม่รวมจุดนอกขอบเขต คุณสามารถปรับปรุงความถูกต้องของการคาดการณ์
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2131ae11e634f9ced0d9696acb61d7b8a94c59cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841826"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="123fc-104">ลบจุดนอกขอบเขตออกจากข้อมูลในอดีตเกี่ยวกับธุรกรรมเมื่อคำนวณความต้องการการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="123fc-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="123fc-105">บทความนี้อธิบายวิธีการแยกจุดนอกขอบเขตจากข้อมูลในอดีตที่ใช้ในการคำนวณความต้องการการคาดการณ์ออก</span><span class="sxs-lookup"><span data-stu-id="123fc-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="123fc-106">โดยไม่รวมจุดนอกขอบเขต คุณสามารถปรับปรุงความถูกต้องของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="123fc-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="123fc-107">คุณสามารถแยกจุดนอกขอบเขตเพื่อปรับปรุงความถูกต้องที่คาดการณ์</span><span class="sxs-lookup"><span data-stu-id="123fc-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="123fc-108">งานนี้เป็นงานที่ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="123fc-108">This is an optional task.</span></span> <span data-ttu-id="123fc-109">นี่คือภาพรวมของกระบวนการ:</span><span class="sxs-lookup"><span data-stu-id="123fc-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="123fc-110">คลิก **การวางแผนหลัก** &gt; **การตั้งค่า** &gt; **การคาดการณ์ความต้องการ** &gt; **การลบจุดนอกขอบเขต** เพื่อเปิดหน้า **การลบจุดนอกขอบเขต** ซึ่งคุณสามารถใช้แบบสอบถามเพื่อเลือกธุรกรรมที่จะแยกออก</span><span class="sxs-lookup"><span data-stu-id="123fc-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="123fc-111">เลือกบริษัทที่ใช้แบบสอบถาม และป้อนชื่อและคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="123fc-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="123fc-112">ฟิลด์ **วันที่ของการสอบถาม** ถูกกำหนดเป็นวันปัจจุบันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="123fc-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="123fc-113">เลือกกล่องกาเครื่องหมาย **ใช้งานอยู่** เพื่อแยกธุรกรรมที่ค้นหาการสอบถามจากข้อมูลในอดีตออก</span><span class="sxs-lookup"><span data-stu-id="123fc-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="123fc-114">การตั้งค่านี้จะมีผลเมื่อคุณสร้างการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="123fc-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="123fc-115">ในหน้า **การสอบถามการลบจุดนอกขอบเขต** คุณสามารถเพิ่ม ลบ และเลือกเกณฑ์ที่กำหนดที่ธุรกรรมจะถูกแยกออกเมื่อการคาดการณ์พื้นฐานที่คำนวณ</span><span class="sxs-lookup"><span data-stu-id="123fc-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="123fc-116">ตัวอย่างเช่น เลือกเฉพาะสินค้า หรือใบสั่งธุรกรรมที่จะแยกออก</span><span class="sxs-lookup"><span data-stu-id="123fc-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="123fc-117">คลิก **แสดงธุรกรรม**.</span><span class="sxs-lookup"><span data-stu-id="123fc-117">Click **Display transactions**.</span></span> <span data-ttu-id="123fc-118">หน้า **ธุรกรรมจุดนอกขอบเขต** จะแสดงรายการธุรกรรมที่ตรงกับเงื่อนไขที่คุณกำหนดไว้ในการสอบถาม และที่จะถูกแยกออกจากข้อมูลในอดีตเมื่อคำนวณการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="123fc-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="123fc-119">**หมายเหตุ:** คุณยังสามารถสร้างแบบสอบถามที่ยึดตามแบบสอบถามที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="123fc-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="123fc-120">เลือกการสอบถามที่คุณต้องการคัดลอก จากนั้นคลิก **ทำซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="123fc-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="123fc-121">ฟิลด์ **วันที่ของการสอบถาม** ระบุเวอร์ชัน</span><span class="sxs-lookup"><span data-stu-id="123fc-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="123fc-122">คุณสามารถใช้การสอบถาม หรือคุณสามารถคลิก **แก้ไขการสอบถาม** เพื่อแก้ไขเงื่อนไขได้</span><span class="sxs-lookup"><span data-stu-id="123fc-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="123fc-123">อีกทางหนึ่งคือคุณสามารถแก้ไขชื่อและคำอธิบายของแบบสอบถามใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="123fc-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="123fc-124">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="123fc-124">Additional resources</span></span>
--------

[<span data-ttu-id="123fc-125">ภาพรวมของการคาดการณ์ความต้องการ</span><span class="sxs-lookup"><span data-stu-id="123fc-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="123fc-126">ตรวจสอบความถูกต้องของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="123fc-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]