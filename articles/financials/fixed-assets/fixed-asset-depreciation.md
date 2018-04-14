---
title: "ค่าเสื่อมราคาของสินทรัพย์ถาวร"
description: "หัวข้อนี้แสดงภาพรวมของค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร"
author: twheeloc
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c8ec644a9559946254a1d35f8698e892be1ca50d
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="fixed-asset-depreciation"></a><span data-ttu-id="364d2-103">ค่าเสื่อมราคาของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="364d2-103">Fixed asset depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="364d2-104">หัวข้อนี้แสดงภาพรวมของค่าเสื่อมราคาสำหรับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="364d2-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="364d2-105">ค่าเสื่อมราคาเป็นธุรกรรมประจำงวด ซึ่งโดยปกติแล้วจะลดมูลค่าของสินทรัพย์ถาวรในงบดุล และบันทึกเป็นค่าใช้จ่ายในงบกำไรขาดทุน</span><span class="sxs-lookup"><span data-stu-id="364d2-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="364d2-106">ดังนั้น โดยปกติบัญชีหลักจะถูกใช้ในเครดิตค่าเสื่อมราคาประจำงวดในงบดุล</span><span class="sxs-lookup"><span data-stu-id="364d2-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="364d2-107">บัญชีตรงข้ามจะเป็นบัญชีในส่วนกำไรขาดทุนของผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="364d2-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="364d2-108">การปรับปรุงค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="364d2-108">Depreciation adjustment</span></span>
<span data-ttu-id="364d2-109">โดยปกติ เฉพาะการแก้ไขธุรกรรมค่าเสื่อมราคาที่ลงรายการบัญชีไปแล้วจะถูกลงรายการบัญชีเป็นการปรับปรุงค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="364d2-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="364d2-110">ดังนั้น บัญชีหลักและบัญชีตรงข้ามมีการตั้งค่าลักษณะเดียวกับบัญชีสำหรับค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="364d2-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="364d2-111">การปรับปรุงค่าเสื่อมราคาอาจเป็นค่าบวกหรือค่าลบ แต่ฟังก์ชันของบัญชีหลัก (เป็นบัญชีงบดุล) และฟังก์ชันของบัญชีตรงข้าม (โดยปกติเป็นบัญชีกำไรขาดทุน) ยังคงเหมือนเดิม</span><span class="sxs-lookup"><span data-stu-id="364d2-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="364d2-112">ค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="364d2-112">Extraordinary depreciation</span></span>
<span data-ttu-id="364d2-113">ค่าเสื่อมราคาพิเศษทำงานเหมือนค่าเสื่อมราคาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="364d2-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="364d2-114">ดังนั้น บัญชีหลักจะถูกใช้ในการเครดิตยอดเงินค่าเสื่อมราคาไปยังงบดุล และลดมูลค่าของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="364d2-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="364d2-115">บัญชีตรงข้ามจะเป็นบัญชีกำไรขาดทุน ที่คำนวณค่าเสื่อมราคาสำหรับรอบระยะเวลาทางบัญชีเป็นค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="364d2-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="364d2-116">ค่าเสื่อมราคาพิเศษทำงานอย่างเป็นอิสระจากค่าเสื่อมราคาพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="364d2-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="364d2-117">เมื่อมีค่าเสื่อมราคาพิเศษเป็นชนิดธุรกรรมที่แยกออกมา คุณจะสามารถลงรายการบัญชีและรายงานค่าเสื่อมราคาพิเศษแยกต่างหากจากค่าเสื่อมราคาพื้นฐานได้</span><span class="sxs-lookup"><span data-stu-id="364d2-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="364d2-118">การหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="364d2-118">Special depreciation allowance</span></span>
<span data-ttu-id="364d2-119">คุณสามารถใช้การหักค่าเสื่อมราคาพิเศษช่วยให้คุณสามารถมีจำนวนเงินค่าเสื่อมราคาพิเศษในระหว่างปีแรกที่เริ่มใช้งานและคิดค่าเสื่อมราคาสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="364d2-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="364d2-120">จะต้องหักค่าเสื่อมราคาพิเศษก่อนที่จะคำนวณค่าเสื่อมราคาอื่น</span><span class="sxs-lookup"><span data-stu-id="364d2-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="364d2-121">เนื่องจากมักจะไม่ทราบหลังจากมีการหักค่าเสื่อมราคาพิเศษของอายุการใช้งานของสินทรัพย์ถาวร ควรใช้การคิดค่าเสื่อมราคาชนิดนี้กับสมุดบัญชีที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="364d2-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="364d2-122">คุณสามารถใช้ฟังก์ชันประจำงวด ลบธุรกรรมที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไป ในการลบประวัติธุรกรรมสำหรับสมุดบัญชีเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="364d2-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="364d2-123">จากนั้นคุณสามารถลบประวัติค่าเสื่อมราคาสำหรับสมุดบัญชีสินทรัพย์ถาวร ลงรายการบัญชีการหักค่าเสื่อมราคาพิเศษเมื่อทราบ และจากนั้นลงรายบัญชีธุรกรรมค่าเสื่อมราคาที่เหลืออยู่ของปีนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="364d2-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="364d2-124">คุณสามารถสร้างเรกคอร์ดการหักค่าเสื่อมราคาพิเศษได้ไม่จำกัดจำนวน</span><span class="sxs-lookup"><span data-stu-id="364d2-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="364d2-125">หลังจากที่คุณกำหนดเรกคอร์ดเหล่านั้นให้กับสมุดบัญชีกลุ่มสินทรัพย์ จะถูกนำไปใช้กับสมุดบัญชีสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="364d2-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="364d2-126">การหักค่าเสื่อมราคาพิเศษจะถูกป้อนเป็นเปอร์เซ็นต์หรือเป็นจำนวนเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="364d2-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="364d2-127">เมื่อคุณลงรายการบัญชีข้อเสนอค่าเสื่อมราคา ธุรกรรมการหักค่าเสื่อมราคาพิเศษจะถูกลงรายการบัญชีที่สมุดบัญชีโดยเป็นธุรกรรมที่แยกต่างหากจากธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="364d2-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="364d2-128"> ปฏิทินค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="364d2-128">Depreciation calendars</span></span>
<span data-ttu-id="364d2-129">สมุดบัญชีแต่ละรายการมีปฏิทินที่จะใช้เมื่อคุณคิดค่าเสื่อมราคาสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="364d2-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="364d2-130">โดยค่าเริ่มต้น ถ้าคุณไม่ระบุปฏิทินในสมุดบัญชี สมุดบัญชีจะใช้ปฏิทินทางการเงินของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="364d2-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="364d2-131">คุณต้องเลือกปฏิทินทางการเงินสำหรับสมุดบัญชีเมื่อโพรไฟล์การคิดค่าเสื่อมราคาที่เชื่อมโยงกับสมุดบัญชีใช้ปีการคิดค่าเสื่อมราคาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="364d2-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="364d2-132">คุณสามารถสร้างปฏิทินที่ใช้ร่วมกันโดยใช้หน้า **ปฏิทินทางการเงิน** ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="364d2-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="364d2-133">สำหรับข้อมูลเพิ่มเติม ดู [วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา](depreciation-methods-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="364d2-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>




