---
title: ตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก
description: หัวข้อนี้อธิบายฟังก์ชันการทำงานของตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกใน Microsoft Dynamics 365 for Retail
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517180"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="1c9ff-103">ตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="1c9ff-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="1c9ff-104">หัวข้อนี้อธิบายฟังก์ชันการทำงานของตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกที่นำเสนอใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.1.3</span><span class="sxs-lookup"><span data-stu-id="1c9ff-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="1c9ff-105">ตัวตรวจสอบความสอดคล้องกันจะระบุและจำแนกธุรกรรมที่ไม่สอดคล้องกันก่อนที่จะมีการจัดการต่อโดยกระบวนการลงรายการบัญชีใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="1c9ff-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="1c9ff-106">เมื่อมีการลงรายการบัญชีใบแจ้งยอดใน Retail การลงรายการบัญชีอาจล้มเหลวเนื่องจากข้อมูลที่ไม่สอดคล้องกันในตารางธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="1c9ff-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="1c9ff-107">ปัญหาข้อมูลอาจเกิดมาจากปัญหาที่ไม่คาดคิดในแอปพลิเคชันการขายหน้าร้าน (POS) หรือหากธุรกรรมมีการนำเข้าอย่างไม่ถูกต้องจากระบบ POS ของบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="1c9ff-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="1c9ff-108">ตัวอย่างของลักษณะความไม่สอดคล้องกันเหล่านี้ที่อาจปรากฏขึ้นได้แก่:</span><span class="sxs-lookup"><span data-stu-id="1c9ff-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="1c9ff-109">ยอดรวมของธุรกรรมในตารางส่วนหัวไม่ตรงกับยอดรวมของธุรกรรมในรายการ</span><span class="sxs-lookup"><span data-stu-id="1c9ff-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="1c9ff-110">จำนวนรายการในตารางส่วนหัวไม่ตรงกับจำนวนของรายการในตารางธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1c9ff-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="1c9ff-111">ภาษีในตารางส่วนหัวไม่ตรงกับยอดเงินภาษีในรายการ</span><span class="sxs-lookup"><span data-stu-id="1c9ff-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="1c9ff-112">เมื่อธุรกรรมที่ไม่สอดคล้องกันถูกจัดการต่อโดยกระบวนการลงรายการบัญชีใบแจ้งยอด จะมีการสร้างใบแจ้งหนี้การขายและสมุดรายวันการชำระเงินที่ไม่สอดคล้องกัน และทำให้กระบวนการลงรายการบัญชีใบแจ้งยอดทั้งหมดล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="1c9ff-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="1c9ff-113">การกู้คืนใบแจ้งยอดจากสถานะดังกล่าวเป็นการแก้ไขข้อมูลที่มีความซับซ้อนในตารางธุรกรรมหลายตาราง</span><span class="sxs-lookup"><span data-stu-id="1c9ff-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="1c9ff-114">ตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีกจะป้องกันปัญหาดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="1c9ff-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="1c9ff-115">ตารางต่อไปนี้แสดงกระบวนการลงรายการบัญชีที่มีตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1c9ff-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="1c9ff-116">![กระบวนการลงรายการบัญชีใบแจ้งยอดที่มีตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก](./media/validchecker.png "กระบวนการลงรายการบัญชีใบแจ้งยอดที่มีตัวตรวจสอบความสอดคล้องกันสำหรับธุรกรรมการขายปลีก")</span><span class="sxs-lookup"><span data-stu-id="1c9ff-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="1c9ff-117">กระบวนการชุดงาน **ตรวจสอบความถูกต้องของธุรกรรมของร้านค้า** จะตรวจสอบความสอดคล้องกันของตารางธุรกรรมการขายปลีกในสถานการณ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1c9ff-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="1c9ff-118">บัญชีลูกค้า - ตรวจสอบว่าบัญชีลูกค้าในตารางธุรกรรมการขายปลีกมีอยู่ในข้อมูลหลักของลูกค้า HQ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="1c9ff-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="1c9ff-119">จำนวนรายการ - ตรวจสอบว่าจำนวนของรายการตามที่บันทึกไว้ในตารางส่วนหัวของธุรกรรมตรงกับจำนวนรายการในตารางธุรกรรมการขายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1c9ff-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="1c9ff-120">ตั้งค่าตัวตรวจสอบความสอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="1c9ff-120">Set up the consistency checker</span></span>
<span data-ttu-id="1c9ff-121">ตั้งค่าคอนฟิกกระบวนการชุดงาน "ตรวจสอบความถูกต้องของธุรกรรมของร้านค้า" ที่ **การขายปลีก \> ฝ่ายไอทีระบบขายปลีก \> การลงรายการบัญชี POS** สำหรับการดำเนินการประจำงวด</span><span class="sxs-lookup"><span data-stu-id="1c9ff-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="1c9ff-122">ชุดงานสามารถจัดกำหนดการตามลำดับชั้นขององค์กร เช่นเดียวกับวิธีการตั้งค่ากระบวนการ "คำนวณใบแจ้งยอดเป็นชุดงาน" และ "ลงรายการบัญชีใบแจ้งยอดเป็นชุดงาน"</span><span class="sxs-lookup"><span data-stu-id="1c9ff-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="1c9ff-123">เราขอแนะนำให้คุณตั้งค่าคอนฟิกกระบวนการชุดงานนี้เพื่อเรียกใช้วันละหลายครั้ง และจัดกำหนดการเพื่อให้ดำเนินการในตอนสิ้นสุดการดำเนินการของงาน P ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="1c9ff-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="1c9ff-124">ผลลัพธ์ของกระบวนการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="1c9ff-124">Results of validation process</span></span>
<span data-ttu-id="1c9ff-125">ผลลัพธ์ของการตรวจสอบความถูกต้องตามกระบวนการชุดงานได้รับการติดแท็กเป็นธุรกรรมการขายปลีกที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="1c9ff-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="1c9ff-126">ฟิลด์ **สถานะการตรวจสอบความถูกต้อง** ในเรกคอร์ดธุรกรรมการขายปลีกได้รับการตั้งค่าเป็น **สำเร็จ** หรือ **ผิดพลาด** และวันที่ของการดำเนินการตรวจสอบความถูกต้องครั้งล่าสุดจะปรากฏในฟิลด์ **เวลาที่ตรวจสอบความถูกต้องล่าสุด**</span><span class="sxs-lookup"><span data-stu-id="1c9ff-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="1c9ff-127">หากต้องการดูข้อความคำอธิบายข้อผิดพลาดเพิ่มเติมที่เกี่ยวข้องกับความล้มเหลวในการตรวจสอบความถูกต้อง เลือกเรกคอร์ดธุรกรรมของร้านค้าการขายปลีกที่เกี่ยวข้องและคลิกปุ่ม **ข้อผิดพลาดในการตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="1c9ff-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="1c9ff-128">ธุรกรรมที่ล้มเหลวในการตรวจสอบความถูกต้องและธุรกรรมที่ยังไม่ได้ตรวจสอบความถูกต้องจะไม่ถูกดึงลงในใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="1c9ff-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="1c9ff-129">ระหว่างกระบวนการ "คำนวณใบแจ้งยอด" ผู้ใช้จะได้รับแจ้งหากมีธุรกรรมที่น่าจะรวมอยู่ในใบแจ้งยอดแต่ไม่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="1c9ff-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="1c9ff-130">หากพบข้อผิดพลาดในการตรวจสอบความถูกต้อง วิธีเดียวในการแก้ไขข้อผิดพลาดคือการติดต่อฝ่ายสนับสนุนของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="1c9ff-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="1c9ff-131">ในรุ่นที่นำออกใช้ในอนาคต จะมีการเพิ่มความสามารถเพื่อให้ผู้ใช้สามารถแก้ไขเรกคอร์ดที่ล้มเหลวผ่านทางอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="1c9ff-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="1c9ff-132">ความสามารถในการลงบันทึกและการตรวจสอบยังสามารถใช้ในการติดตามประวัติการแก้ไขได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="1c9ff-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="1c9ff-133">กฎการตรวจสอบความถูกต้องเพิ่มเติมที่จะรองรับสถานการณ์อื่นๆ จะได้รับการเพิ่มลงในรุ่นที่นำออกใช้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="1c9ff-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
