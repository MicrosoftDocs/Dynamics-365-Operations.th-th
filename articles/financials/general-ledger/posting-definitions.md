---
title: "ข้อกำหนดการลงรายการบัญชี"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดการลงรายการบัญชี และวิธีการกำหนดการเชื่อมโยง สำหรับการสนับสนุนชนิดการลงรายการบัญชี และเอกสาร คุณสามารถใช้ข้อกำหนดการลงรายการบัญชีแทนโพรไฟล์การลงรายการบัญชีเพื่อจัดประเภทบัญชีหลัก และมิติทางการเงินบนรายการการบัญชี"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 513d3e20e0c89eb0064e3c1bc11a3a8dea43cfe4
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definitions"></a><span data-ttu-id="d86f8-104">ข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-104">Posting definitions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d86f8-105">บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดการลงรายการบัญชี และวิธีการกำหนดการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="d86f8-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="d86f8-106">สำหรับการสนับสนุนชนิดการลงรายการบัญชี และเอกสาร คุณสามารถใช้ข้อกำหนดการลงรายการบัญชีแทนโพรไฟล์การลงรายการบัญชีเพื่อจัดประเภทบัญชีหลัก และมิติทางการเงินบนรายการการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="d86f8-107">สำหรับการสนับสนุนชนิดการลงรายการบัญชี และเอกสาร คุณสามารถใช้ข้อกำหนดการลงรายการบัญชีแทนโพรไฟล์การลงรายการบัญชีเพื่อจัดประเภทบัญชีหลัก และมิติทางการเงินบนรายการการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="d86f8-108">คุณสามารถดูเอกสารที่สนับสนุน และชนิดการลงรายการบัญชีในหน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="d86f8-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="d86f8-109">เมื่อเริ่มต้นการใช้งานข้อกำหนดการลงรายการบัญชี เลือกตัวเลือก**ใช้ข้อกำหนดการลงรายการบัญชี** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="d86f8-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="d86f8-110">แม้ว่าเมื่อคุณใช้ข้อกำหนดการลงรายการบัญชี คุณต้องกำหนดโพรไฟล์การลงรายการบัญชีสำหรับรายการเริ่มต้น และชนิดการลงรายการบัญชีที่ไม่สนับสนุน และเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d86f8-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="d86f8-111">คุณต้องใช้ข้อกำหนดการลงรายการบัญชีในใบสั่งเพื่อเปิดใช้งานบัญชีภาระผูกพันสำหรับใบสั่งซื้อ และบัญชีภาระผูกพันที่เกิดขึ้นก่อนสำหรับใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="d86f8-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="d86f8-112">กำหนดข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-112">Defining posting definitions</span></span>
<span data-ttu-id="d86f8-113">ใช้หน้า**ข้อกำหนดการลงรายการบัญชี** เพื่อระบุเกณฑ์การจับคู่ และกำหนดรายการที่ควรจะสร้างเมื่อการจับคู่เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="d86f8-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="d86f8-114">เกณฑ์การจับคู่จะถูกประเมินสำหรับรายการเริ่มต้นเป็นการกระจายการลงบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="d86f8-115">ในหน้า **ข้อกำหนดการลงรายการบัญชี** คุณยังสามารถมอบหมายเลขระดับความสำคัญไปยังรายการเพื่อควบคุมลำดับในบรรทัดที่ถูกประเมิน</span><span class="sxs-lookup"><span data-stu-id="d86f8-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="d86f8-116">รายการที่มีเลขลำดับความสำคัญต่ำสุดจะถูกประเมินก่อน</span><span class="sxs-lookup"><span data-stu-id="d86f8-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="d86f8-117">ตัวอย่างเช่น รายการทั้งหมดที่มีระดับความสำคัญเป็น 1 จะถูกประเมิน และจากนั้นรายการที่มีระดับความสำคัญเป็น 2 และต่อๆไป</span><span class="sxs-lookup"><span data-stu-id="d86f8-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="d86f8-118">เมื่อพบการจับคู่ เกณฑ์การจับคู่อื่นจะถูกละเว้น</span><span class="sxs-lookup"><span data-stu-id="d86f8-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="d86f8-119">นอกจากนี้ เฉพาะเกณฑ์ในกลุ่มที่ตรงกับธุรกรรมเริ่มต้นสร้างรายการที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d86f8-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="d86f8-120">คุณสามารถตรวจสอบข้อกำหนดการลงรายการบัญชีของคุณ โดยใช้วิซาร์ด **ทดสอบข้อกำหนดการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d86f8-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="d86f8-121">หลังจากคุณกำหนดตัวอย่างรายการเริ่มต้นสำหรับข้อกำหนดการลงรายการบัญชี คุณจะเห็นรายการที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="d86f8-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="d86f8-122">คุณสามารถใช้เวอร์ชันข้อกำหนดการลงรายการบัญชีร่วมกับวันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="d86f8-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="d86f8-123">ตัวอย่างเช่น คุณสามารถสร้างเวอร์ชันในอนาคตของข้อกำหนดการลงรายการบัญชีเพื่อลงรายการบัญชีไปยังบัญชีแยกประเภทอื่นในปีบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="d86f8-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="d86f8-124">ใช้หน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** เพื่อกำหนดข้อกำหนดการลงรายการบัญชีให้กับชนิดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="d86f8-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="d86f8-125">การเชื่อมโยงข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-125">Linking posting definitions</span></span>
<span data-ttu-id="d86f8-126">คุณสามารถเชื่อมโยงจากข้อกำหนดการลงรายการบัญชีหนึ่งไปยังอันอื่นเมื่อคุณสร้างข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="d86f8-127">เกณฑ์สำหรับข้อกำหนดที่คุณเชื่อมโยงจะถูกพิจารณาเพิ่มเติมสำหรับเกณฑ์ข้อกำหนดการลงรายการบัญชีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d86f8-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="d86f8-128">คุณลักษณะนี้ช่วยคุณประหยัดเวลา เนื่องจากคุณไม่จำเป็นต้องป้อนเกณฑ์อีกครั้งบนแท็บด่วน **รายการ** บนหน้า **ข้อกำหนดการลงรายการบัญชี** สำหรับข้อกำหนดการลงรายการบัญชีปัจจุบัน ถ้าคุณได้ป้อนรายการเหล่านั้นสำหรับคำนิยามอื่นแล้ว</span><span class="sxs-lookup"><span data-stu-id="d86f8-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="d86f8-129">ในแผนภาพ หรือตาราง รวมถึงการเชื่อมโยงใดๆที่คุณใช้</span><span class="sxs-lookup"><span data-stu-id="d86f8-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="d86f8-130">เพื่อหลีกเลี่ยงความขัดแย้งกับข้อกำหนดการลงรายการบัญชีปัจจุบัน ทำให้แน่ใจว่าบรรทัดในข้อกำหนดการลงรายการบัญชีใดๆที่คุณเชื่อมโยงไปเป็นแบบเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d86f8-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="d86f8-131">ข้อจำกัดต่อไปนี้ใช้เมื่อคุณสร้างการเชื่อมโยงในข้อกำหนดการลงรายการบัญชี:</span><span class="sxs-lookup"><span data-stu-id="d86f8-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="d86f8-132">ข้อกำหนดการลงรายการบัญชีที่ระบุสามารถเชื่อมโยงไปยังข้อกำหนดการลงรายการบัญชีอื่น หรือเชื่อมโยงจากข้อกำหนดการลงรายการบัญชีอื่น แต่ไม่ใช่ทั้งสอง</span><span class="sxs-lookup"><span data-stu-id="d86f8-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="d86f8-133">อย่างไรก็ตาม ข้อกำหนดการลงรายการบัญชีสามารถเชื่อมโยงกับข้อกำหนดการลงรายการบัญชีหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="d86f8-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="d86f8-134">คุณสามารถตั้งค่าการเชื่อมโยงได้เฉพาะระหว่างข้อกำหนดการลงรายการบัญชีที่อยู่ในโมดูลเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d86f8-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="d86f8-135">คุณสามารถกำหนดข้อกำหนดการลงรายการบัญชีไปยังชนิดธุรกรรมใดๆ แต่ต้องเป็นชนิดธุรกรรมในโมดูลเดียวกันกับข้อกำหนดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86f8-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="d86f8-136">ใช้หน้า **ข้อกำหนดการลงรายการบัญชีธุรกรรม** เพื่อดูว่าชนิดธุรกรรมอยู่ในโมดูใด</span><span class="sxs-lookup"><span data-stu-id="d86f8-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="d86f8-137">สำหรับข้อมูลเพิ่มเติม ดู [ตัวอย่างข้อกำหนดการลงรายการบัญชี](example-posting-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="d86f8-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



