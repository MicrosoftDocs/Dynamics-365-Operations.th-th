---
title: คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล
description: สามารถรันการคิดค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคลในขั้นตอนเดียวได้
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2575354af322827972ffa650e9c732170c5a6eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566563"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="9e3f4-103">คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9e3f4-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e3f4-104">สามารถรันการคิดค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคลในขั้นตอนเดียวได้</span><span class="sxs-lookup"><span data-stu-id="9e3f4-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="9e3f4-105">กระบวนงานนี้แสดงวิธีตั้งค่า และรันกระบวนการสำหรับหลายนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9e3f4-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="9e3f4-106">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="9e3f4-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="9e3f4-107">ตั้งค่าสมุดรายวันการรันค่าเสื่อมราคาระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="9e3f4-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="9e3f4-108">ไปที่สินทรัพย์ถาวร > การตั้งค่า > พารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9e3f4-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="9e3f4-109">ขยายส่วนข้อเสนอสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9e3f4-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="9e3f4-110">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="9e3f4-110">Click Add.</span></span>
4. <span data-ttu-id="9e3f4-111">ในฟิลด์ชั้นของการลงรายการบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9e3f4-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="9e3f4-112">ในฟิลด์ชื่อสมุดรายวัน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9e3f4-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="9e3f4-113">ทำซ้ำการตั้งค่าสมุดรายวันบนหน้าพารามิเตอร์สินทรัพย์ถาวร ในนิติบุคคลแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="9e3f4-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="9e3f4-114">การรันค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="9e3f4-114">Depreciation run</span></span>
1. <span data-ttu-id="9e3f4-115">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สร้างข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="9e3f4-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="9e3f4-116">ในฟิลด์ชั้นของการลงรายการบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9e3f4-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="9e3f4-117">ชื่อสมุดรายวันจะเริ่มต้นจากพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9e3f4-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="9e3f4-118">ซึ่งสามารถถูกเปลี่ยนได้ที่นี่สำหรับนิติบุคคลปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="9e3f4-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="9e3f4-119">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="9e3f4-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="9e3f4-120">เลือกนิติบุคคลที่จะถูกรวมในการรันค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="9e3f4-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="9e3f4-121">จะมีการแสดงเฉพาะนิติบุคคลกับสมุดรายวันที่ตั้งค่าสำหรับข้อเสนอสินทรัพย์ถาวร บนหน้าพารามิเตอร์สินทรัพย์ถาวรในรายการ</span><span class="sxs-lookup"><span data-stu-id="9e3f4-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="9e3f4-122">เลือก ใช่ ในฟิลด์ ลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="9e3f4-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="9e3f4-123">ฟิลด์กรองข้อมูลรวมสินทรัพย์ถาวร กลุ่ม และสมุดบัญชีทั้งหมด สำหรับนิติบุคคลที่ถูกเลือกสำหรับการรันค่าเสื่อมราคานี้</span><span class="sxs-lookup"><span data-stu-id="9e3f4-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="9e3f4-124">ตัวเลือกการประมวลผลชุดงานถูกเปิดใช้งานโดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9e3f4-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="9e3f4-125">เมื่อตัวเลือกนี้ถูกเปิดใช้งาน การสร้างสมุดรายวันค่าเสื่อมราคาและการลงรายการบัญชีจะทำงานในเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="9e3f4-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="9e3f4-126">คลิกสร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="9e3f4-126">Click Create journal.</span></span>
6. <span data-ttu-id="9e3f4-127">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9e3f4-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

