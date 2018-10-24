--- 
title: "ตั้งค่ารูปแบบมูลค่า"
description: "กระบวนงานนี้จะแสดงวิธีการสร้างสมุดบัญชีสินทรัพย์ถาวรใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร "
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e067173b27488422fd05ad45f37528f00f04a2bd
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-value-models"></a><span data-ttu-id="b6130-103">ตั้งค่ารูปแบบมูลค่า</span><span class="sxs-lookup"><span data-stu-id="b6130-103">Set up value models</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6130-104">กระบวนงานนี้จะแสดงวิธีการสร้างสมุดบัญชีสินทรัพย์ถาวรใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="b6130-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="b6130-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="b6130-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="b6130-106">สร้างสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="b6130-106">Create a book</span></span>
1. <span data-ttu-id="b6130-107">ไปที่ สินทรัพย์ถาวร > ติดตั้ง > สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="b6130-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="b6130-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b6130-108">Click New.</span></span>
3. <span data-ttu-id="b6130-109">ในฟิลด์สมุดบัญชี ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b6130-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="b6130-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b6130-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b6130-111">ถ้าคำนวณค่าเสื่อมราคาถูกเลือก สินทรัพย์ที่เกี่ยวข้องกับสมุดบัญชีจะรวมในข้อเสนอค่าเสื่อมราคา </span><span class="sxs-lookup"><span data-stu-id="b6130-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="b6130-112">ถ้าไม่ได้ถูกเลือก สมุดบัญชีสินทรัพย์จะไม่ถูกคิดค่าเสื่อมราคาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b6130-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="b6130-113">เลือก ใช่ ในฟิลด์คำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b6130-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="b6130-114">ในฟิลด์โพรไฟล์ค่าเสื่อมราคา ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b6130-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="b6130-115">โพรไฟล์ค่าเสื่อมราคาสำรองจะรู้จักกันในการเปลี่ยนแปลงวิธีการคิดค่าเสื่อมราคา </span><span class="sxs-lookup"><span data-stu-id="b6130-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="b6130-116">ข้อเสนอค่าเสื่อมราคาจะสลับไปยังโพรไฟล์นี้เมื่อโพรไฟล์สำรองจะคำนวณจำนวนค่าเสื่อมราคา นั่นคือเท่ากับหรือมากกว่าโพรไฟล์ค่าเสื่อมราคาเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b6130-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="b6130-117">โพรไฟล์ค่าเสื่อมราคาพิเศษใช้สำหรับค่าเสื่อมราคาเพิ่มเติมของสินทรัพย์ในสถานการณ์ที่ผิดปกติ </span><span class="sxs-lookup"><span data-stu-id="b6130-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="b6130-118">ตัวอย่างเช่น คุณอาจใช้สิ่งนี้เพื่อบันทึกการคิดค่าเสื่อมราคาซึ่งเป็นผลมาจากภัยพิบัติธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="b6130-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="b6130-119">หากสร้างกการปรับปรุงค่าเสื่อมราคาที่มีการปรับปรุงพื้นฐานจะถูกเลือก การปรับปรุงค่าเสื่อมราคาจะสร้างอัตโนมัติเมื่อค่าของสินทรัพย์อัพเดท </span><span class="sxs-lookup"><span data-stu-id="b6130-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="b6130-120">ถ้าไม่ได้ถูกเลือก ถ้าไม่ได้ถูกเลือก มูลค่าสินทรัพย์อัพเดทจะมีผลเฉพาะกับคำนวณค่าเสื่อมราคานับจากวันนี้</span><span class="sxs-lookup"><span data-stu-id="b6130-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="b6130-121">เลือก ใช่ ในฟิลด์ สร้างการปรับปรุงค่าเสื่อมราคาที่มีการปรับปรุงเกณฑ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b6130-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="b6130-122">โดยค่าเริ่มต้น ธุรกรรมสมุดบัญชีสินทรัพย์ถาวรจะลงรายการบัญชีในบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="b6130-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="b6130-123">คุณสามารถปิดใช้งานการลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับสมุดบัญชีได้โดยการตั้งค่าฟิลด์การลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปเป็น ไม่</span><span class="sxs-lookup"><span data-stu-id="b6130-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="b6130-124">สมุดบัญชีที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภททั่วไปโดยทั่วไปจะใช้สำหรับการรายงานภาษี</span><span class="sxs-lookup"><span data-stu-id="b6130-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="b6130-125">ซึ่งทำให้คุณมีความยืดหยุ่นเพิ่มเติมในการลบธุรกรรมในอดีตสำหรับสมุดบัญชีสินทรัพย์เนื่องจากไม่ถูกส่งไปยังบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="b6130-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="b6130-126">ชั้นของการลงรายการบัญชีถูกกำหนดค่าเริ่มต้นเป็นชั้นปัจจุบัน ถ้าสมุดบัญชีลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป และไม่มี ถ้าไม่ได้ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="b6130-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="b6130-127">ปรับปรุงชั้นของการลงรายการบัญชีถ้าคุณต้องการให้ธุรกรรมสำหรับสมุดบัญชีนี้ถูกลงรายการบัญชีไปยังชั้นอื่น</span><span class="sxs-lookup"><span data-stu-id="b6130-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="b6130-128">ในฟิลด์ปฏิทิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b6130-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="b6130-129">สมุดบัญชีที่ได้รับจะลงรายการบัญชีธุรกรรมไปยังบัญชีต่างๆ พร้อมกัน </span><span class="sxs-lookup"><span data-stu-id="b6130-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="b6130-130">คุณจะสร้างธุรกรรมที่มีสมุดบัญชีหลักและในระหว่างการลงรายการบัญชี สำเนาที่เหมือนกันของธุรกรรมดังกล่าวจะถูกลงรายการบัญชีไปยังสมุดบัญชีที่ได้รับ </span><span class="sxs-lookup"><span data-stu-id="b6130-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="b6130-131">ไม่มีการคำนวณใหม่กับธุรกรรมสมุดบัญชีที่ได้รับ ดังนั้นจึงไม่ควรใช้สำหรับธุรกรรมค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="b6130-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="b6130-132">เชื่อมโยงสมุดบัญชีกับกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b6130-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="b6130-133">คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b6130-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="b6130-134">ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b6130-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="b6130-135">ในฟิลด์อายุการใช้งาน ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="b6130-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="b6130-136">โปรดทราบว่ารอบระยะเวลาการคิดค่าเสื่อมราคาจะถูกคำนวณหลังจากการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b6130-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="b6130-137">คุณสามารถกำหนดแบบแผนการคิดค่าเสื่อมราคาตามที่จำเป็นสำหรับวัตถุประสงค์ด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="b6130-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


