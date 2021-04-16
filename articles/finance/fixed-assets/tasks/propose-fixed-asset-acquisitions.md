---
title: นำเสนอการซื้อสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายวิธีการได้รับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817183"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="9217b-103">นำเสนอการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9217b-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9217b-104">หัวข้อนี้อธิบายวิธีการได้รับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9217b-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="9217b-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="9217b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="9217b-106">เมื่อต้องการรับสินทรัพย์ถาวรโดยใช้สมุดรายวันข้อเสนอสินทรัพย์ถาวร คุณต้องสร้างเรกคอร์ดสินทรัพย์ถาวรก่อนแล้วกำหนดราคาการซื้อสินทรัพย์ในสมุดบัญชีสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9217b-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="9217b-107">สร้างข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9217b-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="9217b-108">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9217b-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="9217b-109">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9217b-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="9217b-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9217b-110">Select **New**.</span></span>
3. <span data-ttu-id="9217b-111">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9217b-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="9217b-112">ในบานหน้าต่างการดำเนินการ เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="9217b-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="9217b-113">เลือก **ข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="9217b-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="9217b-114">เลือก **ข้อเสนอการซื้อสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9217b-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="9217b-115">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="9217b-115">Select **Filter**.</span></span> <span data-ttu-id="9217b-116">เลือก **รีเซ็ต** เพื่อล้างค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9217b-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="9217b-117">เลือกแถว **จำนวนสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9217b-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="9217b-118">ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="9217b-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="9217b-119">กำหนดเงื่อนไขที่เหลือสำหรับสินทรัพย์ถาวรที่คุณต้องการได้รับกับข้อเสนอนี้</span><span class="sxs-lookup"><span data-stu-id="9217b-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="9217b-120">เลือก **ตกลง** สองครั้ง เพื่อออกจากบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="9217b-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="9217b-121">ตรวจสอบว่ามีการสร้างรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9217b-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="9217b-122">เฉพาะสินทรัพย์ถาวรที่มีวันที่ซื้อสินทรัพย์ และราคาทุนของสินทรัพย์ที่ตั้งค่าไว้ในสมุดบัญชีจะรวมอยู่ในข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9217b-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="9217b-123">บนหน้า เลือกแท็บ **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="9217b-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="9217b-124">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="9217b-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="9217b-125">รวมมิติทางการเงินเริ่มต้นในข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9217b-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="9217b-126">ธุรกรรมการซื้อสินทรัพย์สามารถสร้างขึ้นโดยใช้ Add-in ของ Excel ได้ โดยไปที่ **สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="9217b-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="9217b-127">สร้างสมุดรายวันใหม่ และย้ายไปยังส่วน **บรรทัด** บนหน้า และเลือกไอคอน Excel แล้วจากนั้น เลือกบรรทัดสมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="9217b-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="9217b-128">ระบบจะสร้างและเปิดเท็มเพลต Excel ที่แสดงถึงบรรทัดสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="9217b-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="9217b-129">คุณสามารถเพิ่มข้อมูลให้กับบรรทัดสมุดรายวันที่คุณเพิ่มเข้าในเท็มเพลต แล้วจากนั้น เผยแพร่ข้อมูลนั้นกลับไปยังระบบ</span><span class="sxs-lookup"><span data-stu-id="9217b-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="9217b-130">ถ้ามีการตั้งค่ามิติเริ่มต้นสำหรับสมุดบัญชีสินทรัพย์ที่เลือก และสินทรัพย์ถาวรที่สอดคล้องกันที่ป้อนไว้ในเท็มเพลต Excel มิติทางการเงินเริ่มต้นจะถูกเรียกจากข้อมูลหลักของสมุดบัญชีสินทรัพย์ เมื่อมีการเผยแพร่สมุดรายวันจาก Excel ไปยังระบบ</span><span class="sxs-lookup"><span data-stu-id="9217b-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="9217b-131">เมื่อต้องการรวมมิติทางการเงินในสมุดบัญชีสินทรัพย์โดยอัตโนมัติ ในขณะที่เผยแพร่สมุดรายวันสินทรัพย์ถาวรจาก Add-in ของ Excel คุณต้องตั้งค่ามิติเริ่มต้นล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="9217b-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
