---
title: สร้างข้อเสนอค่าเสื่อมราคา
description: 'ขั้นตอนนี้อธิบายถึงการทำงานของข้อเสนอของชุดค่าเสื่อมราคา และอธิบายวิธีการเสนอค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร '
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "361302"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="5c958-103">สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="5c958-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c958-104">ขั้นตอนนี้อธิบายถึงการทำงานของข้อเสนอของชุดค่าเสื่อมราคา และอธิบายวิธีการเสนอค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="5c958-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="5c958-105">งานนี้ใช้บริษัทสาธิต USMF และบทบาทของนักบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c958-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="5c958-106">สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="5c958-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="5c958-107">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="5c958-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="5c958-108">ในฟิลด์ชื่อของสมุดรายวัน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="5c958-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5c958-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="5c958-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5c958-110">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="5c958-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5c958-111">เลือกตัวเลือกการสรุปค่าเสื่อมราคาเพื่อสรุปค่าเสื่อมราคารายเดือนเข้าไปในสมุดรายวันหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5c958-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="5c958-112">ตัวอย่างเช่น ถ้าค่าวันที่สิ้นสุดคือวันที่ 31 มีนาคม 2015 คำอธิบายต่อไปนี้จะถูกสร้างขึ้น: "ค่าเสื่อมราคาตั้งแต่วันที่ 31 มกราคม 2015"</span><span class="sxs-lookup"><span data-stu-id="5c958-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="5c958-113">ฟิลด์วันที่บนสมุดรายวันที่เสนอจะถูกตั้งเป็น 31 มีนาคม 2015</span><span class="sxs-lookup"><span data-stu-id="5c958-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="5c958-114">ข้อเสนอค่าเสื่อมราคาสามารถกรองตามสินทรัพย์ กลุ่มสินทรัพย์ หรือเกณฑ์อื่นๆ โดยใช้ตัวเลือกในการกรอง</span><span class="sxs-lookup"><span data-stu-id="5c958-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="5c958-115">เมื่อคุณใช้แบบฟอร์มสร้างข้อเสนอการซื้อสินทรัพย์หรือการเสื่อมราคาสำหรับสินทรัพย์ถาวร คุณสามารถเสนอค่าเสื่อมราคาในชุดงาน </span><span class="sxs-lookup"><span data-stu-id="5c958-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="5c958-116">นี่คือคำแนะนำสำหรับข้อเสนอใหญ่ที่จะใช้ทรัพยากรของระบบมากขึ้น </span><span class="sxs-lookup"><span data-stu-id="5c958-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="5c958-117">ถ้าคุณเลือกตัวเลือกชุดงาน คุณยังคงสามารถดำเนินงานอื่นๆ ให้สำเร็จในช่วงเวลานั้น </span><span class="sxs-lookup"><span data-stu-id="5c958-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="5c958-118">เมื่อคุณเสนอค่าเสื่อมราคาในลักษณะนี้ จะมีการคำนวณค่าเสื่อมราคาสำหรับรูปแบบมูลค่าสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="5c958-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="5c958-119">คลิกสร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="5c958-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="5c958-120">ตรวจทานรายการค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="5c958-120">Review depreciation entries</span></span>
1. <span data-ttu-id="5c958-121">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="5c958-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="5c958-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5c958-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5c958-123">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="5c958-123">Click Lines.</span></span>
4. <span data-ttu-id="5c958-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="5c958-124">Click Post.</span></span>

