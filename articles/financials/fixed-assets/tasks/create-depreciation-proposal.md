---
title: สร้างข้อเสนอค่าเสื่อมราคา
description: หัวข้อนี้อธิบายวิธีการทำงานของข้อเสนอชุดงานค่าเสื่อมราคา และอธิบายวิธีการเสนอค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867618"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="87c45-103">สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="87c45-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87c45-104">หัวข้อนี้อธิบายวิธีการทำงานของข้อเสนอชุดงานค่าเสื่อมราคา และอธิบายวิธีการเสนอค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="87c45-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="87c45-105">งานนี้ใช้บริษัทสาธิต USMF และบทบาทของนักบัญชี</span><span class="sxs-lookup"><span data-stu-id="87c45-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="87c45-106">สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="87c45-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="87c45-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > รายการสมุดรายวัน > สร้างข้อเสนอค่าเสื่อมราคา**</span><span class="sxs-lookup"><span data-stu-id="87c45-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="87c45-108">ในฟิลด์ **ชื่อของสมุดรายวัน** ให้เลือกตัวเลือกจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="87c45-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="87c45-109">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="87c45-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="87c45-110">เลือกตัวเลือก **สรุปค่าเสื่อมราคา** เพื่อสรุปค่าเสื่อมราคารายเดือนลงในรายการสมุดรายวันหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="87c45-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="87c45-111">ตัวอย่างเช่น ถ้าค่าวันที่สิ้นสุดคือวันที่ 31 มีนาคม 2015 คำอธิบายต่อไปนี้จะถูกสร้างขึ้น: "ค่าเสื่อมราคาตั้งแต่วันที่ 31 มกราคม 2015"</span><span class="sxs-lookup"><span data-stu-id="87c45-111">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="87c45-112">จากนั้น ฟิลด์ **วันที่** บนรายการสมุดรายวันที่เสนอจะถูกตั้งเป็น 31 มีนาคม 2015</span><span class="sxs-lookup"><span data-stu-id="87c45-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="87c45-113">ข้อเสนอค่าเสื่อมราคาสามารถถูกกรองตามสินทรัพย์ กลุ่มสินทรัพย์ หรือเกณฑ์อื่นๆ โดยใช้ตัวเลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="87c45-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="87c45-114">เมื่อคุณใช้ฟอร์ม **สร้างข้อเสนอการซื้อสินทรัพย์หรือค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร** คุณสามารถเสนอค่าเสื่อมราคาในชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="87c45-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="87c45-115">นี่คือคำแนะนำสำหรับข้อเสนอใหญ่ที่จะใช้ทรัพยากรของระบบมากขึ้น </span><span class="sxs-lookup"><span data-stu-id="87c45-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="87c45-116">ถ้าคุณเลือกตัวเลือกชุดงาน คุณยังคงสามารถดำเนินงานอื่นๆ ให้สำเร็จในช่วงเวลานั้น </span><span class="sxs-lookup"><span data-stu-id="87c45-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="87c45-117">เมื่อคุณเสนอค่าเสื่อมราคาในลักษณะนี้ จะมีการคำนวณค่าเสื่อมราคาสำหรับรูปแบบมูลค่าสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="87c45-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="87c45-118">เลือก **สร้างสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="87c45-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="87c45-119">ตรวจทานรายการค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="87c45-119">Review depreciation entries</span></span>
1. <span data-ttu-id="87c45-120">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="87c45-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="87c45-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="87c45-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="87c45-122">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="87c45-122">Select **Lines**.</span></span>
4. <span data-ttu-id="87c45-123">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="87c45-123">Select **Post**.</span></span>

