---
title: เปลี่ยนหรือกำหนดปฏิทินบัญชีแยกประเภทใหม่
description: หัวข้อนี้อธิบายวิธีการเปลี่ยนปฏิทินที่กําหนดให้กับบัญชีแยกประเภทในปัจจุบัน และวิธีกําหนดปฏิทินใหม่ให้กับบัญชีแยกประเภท
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039961"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="4e1f4-103">เปลี่ยนหรือกำหนดปฏิทินบัญชีแยกประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e1f4-104">หัวข้อนี้อธิบายวิธีการเปลี่ยนปฏิทินที่กําหนดให้กับบัญชีแยกประเภทในปัจจุบัน และวิธีกําหนดปฏิทินใหม่ให้กับบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4e1f4-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="4e1f4-105">ปัญหา</span><span class="sxs-lookup"><span data-stu-id="4e1f4-105">Issue</span></span>

<span data-ttu-id="4e1f4-106">บางครั้งบริษัทต้องเปลี่ยนปฏิทินที่มีอยู่ซึ่งกําหนดให้กับบัญชีแยกประเภทหรือกําหนดปฏิทินใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="4e1f4-107">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="4e1f4-107">Resolution</span></span>

<span data-ttu-id="4e1f4-108">มีสองสถานการณ์ที่จะมีการเปลี่ยนหรือกำหนดปฏิทินบัญชีแยกประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="4e1f4-109">สถานการณ์แรกเกี่ยวข้องกับการเปลี่ยนปฏิทินที่มีอยู่ซึ่งกำหนดให้กับบัญชีแยกประเภทแล้ว</span><span class="sxs-lookup"><span data-stu-id="4e1f4-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="4e1f4-110">สถานการณ์ที่สองเกี่ยวข้องกับการสร้างปฏิทินใหม่และกําหนดปฏิทินนั้นให้กับบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="4e1f4-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="4e1f4-111">การเปลี่ยนแปลงทั้งสองอย่างสามารถทำได้ตลอดเวลาแม้แต่หลังจากที่ลงรายการบัญชีธุรกรรมในบัญชีแยกประเภทแล้ว</span><span class="sxs-lookup"><span data-stu-id="4e1f4-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="4e1f4-112">เปลี่ยนปฏิทินทางการเงินที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="4e1f4-113">เมื่อต้องการเปลี่ยนปฏิทินที่มีอยู่ซึ่งกำหนดให้กับบัญชีแยกประเภทของคุณ ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่าบัญชีแยกประเภท \> บัญชีแยกประเภท** และเลือกลิงก์ให้กับปฏิทินทางการเงินเพื่อเปิดหน้า **ปฏิทินบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="4e1f4-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="4e1f4-114">มีข้อจำกัดสำหรับการเปลี่ยนแปลงที่สามารถดำเนินการกับปฏิทินได้</span><span class="sxs-lookup"><span data-stu-id="4e1f4-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="4e1f4-115">ตัวอย่างเช่น คุณสามารถเปลี่ยนวันที่เริ่มต้นและวันที่สิ้นสุดของ *รอบระยะเวลา* ในแต่ละปีได้ แต่คุณไม่สามารถเปลี่ยนวันที่เริ่มต้นและวันที่สิ้นสุดของ *ปี* ในปฏิทินได้</span><span class="sxs-lookup"><span data-stu-id="4e1f4-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="4e1f4-116">เมื่อต้องการเปลี่ยนแปลงรอบระยะเวลาในปี ให้เลือกปฏิทินและปีที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4e1f4-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="4e1f4-117">อันดับแรกให้ใช้ปุ่ม **ลบรอบระยะเวลา** เพื่อลบรอบระยะเวลาการดําเนินงานที่มีอยู่บางส่วนหรือทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4e1f4-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="4e1f4-118">รอบระยะเวลาการดําเนินงานทั้งหมดยกเว้นรอบระยะเวลาแรกที่สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="4e1f4-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="4e1f4-119">จากนั้นใช้ **ปุ่มแบ่งรอบระยะเวลา** เพื่อแบ่งรอบระยะเวลาหรือรอบระยะเวลาที่เหลือออกเป็นรอบระยะเวลาใหม่ โดยป้อนวันที่เริ่มต้นที่เหมาะสมให้กับรอบระยะเวลาถัดไป</span><span class="sxs-lookup"><span data-stu-id="4e1f4-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="4e1f4-120">หลังจากที่คุณเปลี่ยนรอบระยะเวลาในปฏิทินแล้ว คุณต้องรันกระบวนการ **คำนวณรอบระยะเวลาบัญชีแยกประเภทใหม่** ในนิติบุคคล (บริษัท) ทุกแห่งที่จะกำหนดปฏิทินให้</span><span class="sxs-lookup"><span data-stu-id="4e1f4-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="4e1f4-121">แม้ว่าจะไม่มีข้อความแจ้งเตือนให้คุณดำเนินขั้นตอนนี้ให้เสร็จสิ้น แต่กระบวนการการคำนวณใหม่จะต้องอัพเดตรอบระยะเวลาที่กำหนดให้กับแต่ละธุรกรรมที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="4e1f4-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="4e1f4-122">หากต้องการรันกระบวนการคำนวณใหม่ ให้เลือก **คำนวณรอบระยะเวลาของบัญชีแยกประเภทใหม่** ในหน้า **การตั้งค่าบัญชีแยกประเภท** ในแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="4e1f4-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="4e1f4-123">หากไม่มีการรันกระบวนการคำนวณใหม่ ยอดดุลธุรกรรมในงบทดลองหรือในงบการเงินอาจรวมอยู่ในรอบระยะเวลาอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4e1f4-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="4e1f4-124">ในกรณีนี้ คุณสามารถแก้ไขยอดดุลได้ตลอดเวลาด้วยการรันกระบวนการการคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="4e1f4-125">กําหนดปฏิทินทางการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="4e1f4-126">เมื่อต้องการกําหนดปฏิทินทางการเงินใหม่ ให้ไปที่ **บัญชีแยกประเภททั่วไป \> การตั้งค่าบัญชีแยกประเภท \> บัญชีแยกประเภท** แล้วเลือก **แก้ไข** เพื่อวางหน้า **บัญชีแยกประเภท** ไปยังโหมดแก้ไข</span><span class="sxs-lookup"><span data-stu-id="4e1f4-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="4e1f4-127">จากนั้น ในฟิลด์ **ปฏิทินทางการเงิน** ให้เลือกปฏิทินทางการเงินใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="4e1f4-128">หลังจากที่คุณเปลี่ยนปฏิทินทางการเงินของบัญชีแยกประเภทแล้ว คุณต้องรัน **คำนวณรอบระยะเวลาบัญชีแยกประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="4e1f4-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="4e1f4-129">เมื่อคุณกําหนดปฏิทินทางการเงินใหม่ให้กับบัญชีแยกประเภท ข้อความจะเตือนให้คุณดำเนินขั้นตอนนี้ให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="4e1f4-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="4e1f4-130">แม้ว่าข้อความอาจดูเหมือนจะบ่งชี้ว่ากระบวนการคำนวณใหม่ไม่จำเป็นต้องระบุ แต่ไม่ใช่เช่นนั้น</span><span class="sxs-lookup"><span data-stu-id="4e1f4-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="4e1f4-131">ต้องอัพเดตรอบระยะเวลาที่กำหนดให้กับแต่ละธุรกรรมที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="4e1f4-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="4e1f4-132">หากต้องการรันกระบวนการคำนวณใหม่ ให้เลือก **คำนวณรอบระยะเวลาของบัญชีแยกประเภทใหม่** ในหน้า **การตั้งค่าบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="4e1f4-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="4e1f4-133">หากไม่มีการรันกระบวนการคำนวณใหม่ ยอดดุลธุรกรรมในงบทดลองหรือในงบการเงินอาจรวมอยู่ในรอบระยะเวลาอย่างไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="4e1f4-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="4e1f4-134">ในกรณีนี้ คุณสามารถแก้ไขยอดดุลได้ตลอดเวลาด้วยการรันกระบวนการการคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="4e1f4-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
