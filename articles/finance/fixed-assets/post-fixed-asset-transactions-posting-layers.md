---
title: ลงรายการบัญชีธุรกรรมสินทรัพย์ถาวรที่ชั้นของการลงรายการบัญชี
description: บทความนี้ให้ภาพรวมของฟังก์ชันชั้นของการลงรายการบัญชีสำหรับธุรกรรมสินทรัพย์ถาวร
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8c4f4f41ed39447ae441dd8e01cfcf80c939b5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770723"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="f87a4-103">ลงรายการบัญชีธุรกรรมสินทรัพย์ถาวรที่ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f87a4-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f87a4-104">บทความนี้ให้ภาพรวมของฟังก์ชันชั้นของการลงรายการบัญชีสำหรับธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f87a4-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="f87a4-105">โดยทั่วไป สินทรัพย์ถาวรจะมีการคิดค่าเสื่อมราคาในลักษณะต่างๆ เพื่อวัตถุประสงค์ที่แตกต่างกัน </span><span class="sxs-lookup"><span data-stu-id="f87a4-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="f87a4-106">การคิดค่าเสื่อมราคาเพื่อวัตถุประสงค์ทางภาษีจะคำนวณโดยใช้กฎระเบียบภาษีปัจจุบันเพื่อให้ได้ค่าเสื่อมราคาสูงสุดที่เป็นไปได้ก่อนการคำนวณภาษี แต่การคิดค่าเสื่อมราคาเพื่อวัตถุประสงค์ในการรายงานจะคำนวณตามกฎหมายและมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="f87a4-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="f87a4-107">การคิดค่าเสื่อมราคาชนิดต่างๆ จะถูกคำนวณและบันทึกแยกกันในชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f87a4-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="f87a4-108">สมุดบัญชีแต่ละรายการที่แนบกับสินทรัพย์ถาวรจะถูกตั้งค่าไว้สำหรับชั้นของการลงรายการบัญชีเฉพาะที่มีวัตถุประสงค์ของการคิดค่าเสื่อมราคาโดยรวม</span><span class="sxs-lookup"><span data-stu-id="f87a4-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="f87a4-109">ชั้นของการลงรายการบัญชีมีสิบชั้น: ชั้นปัจจุบัน การดำเนินงาน ภาษี และชั้นที่กำหนดเองเจ็ดชั้น</span><span class="sxs-lookup"><span data-stu-id="f87a4-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="f87a4-110">คุณยังสามารถปิดใช้งานการลงรายการบัญชีในบัญชีแยกประเภททั่วไปสำหรับสมุดบัญชีได้โดยการตั้งค่าฟิลด์ ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป เป็น ไม่ใช่</span><span class="sxs-lookup"><span data-stu-id="f87a4-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="f87a4-111">จากนั้นฟิลด์ ชั้นของการลงรายการบัญชี จะถูกกำหนดเป็น ไม่มีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f87a4-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="f87a4-112">โดยทั่วไป สมุดบัญชีที่ไม่ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไปจะถูกนำมาใช้สำหรับการรายงานภาษี</span><span class="sxs-lookup"><span data-stu-id="f87a4-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="f87a4-113">วิธีการนี้ช่วยให้คุณมีความยืดหยุ่นเพิ่มเติมในการลบธุรกรรมในอดีตสำหรับสมุดบัญชีสินทรัพย์ เนื่องจากรายการเหล่านั้นไม่ได้ถูกกำหนดให้กับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f87a4-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="f87a4-114">กำหนดสมุดรายวันสินทรัพย์ถาวรโดยใช้หน้า ชื่อสมุดรายวัน ใน บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > ชื่อสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="f87a4-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="f87a4-115">สมุดรายวันแต่ละเล่มที่คุณสามารถลงรายการบัญชีค่าเสื่อมราคาจะถูกกำหนดโดยชื่อสมุดรายวันของการคิดค่าเสื่อมราคาสำหรับชั้นของการลงรายการบัญชีเพียงชั้นเดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f87a4-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="f87a4-116">ไม่สามารถเปลี่ยนแปลงชั้นของการลงรายการบัญชีในสมุดรายวันได้</span><span class="sxs-lookup"><span data-stu-id="f87a4-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="f87a4-117">ข้อจำกัดนี้ช่วยรับประกันว่าธุรกรรมสำหรับชั้นของการลงรายการบัญชีแต่ละชั้นถูกเก็บโดยแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="f87a4-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="f87a4-118">สำหรับแต่ละชั้นของการลงรายการบัญชี จะต้องมีการสร้างชื่อสมุดรายวันอย่างน้อยหนึ่งชื่อ</span><span class="sxs-lookup"><span data-stu-id="f87a4-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="f87a4-119">ถ้าคุณใช้สมุดบัญชีที่ไม่ได้ลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป คุณยังต้องสร้างสมุดรายวันที่ตั้งค่าชั้นการลงรายการบัญชีเป็น ไม่มี</span><span class="sxs-lookup"><span data-stu-id="f87a4-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="f87a4-120">คุณสามารถกำหนดรหัสบัญชีสำหรับธุรกรรมสินทรัพย์ถาวรได้ในหน้า โพรไฟล์การลงบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f87a4-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="f87a4-121">สำหรับแต่ละโพรไฟล์การลงบัญชี คุณต้องเลือกชนิดของธุรกรรมและสมุดบัญชีที่เกี่ยวข้อง และจากนั้น กำหนดบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="f87a4-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="f87a4-122">ตั้งค่าเรกคอร์ดโพรไฟล์การลงรายการบัญชีสำหรับแต่ละสมุดบัญชีที่จะลงรายการบัญชีไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="f87a4-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="f87a4-123">คุณสามารถใช้สมุดบัญชีที่ได้รับเพื่อลงรายการบัญชีธุรกรรมที่ชั้นของการลงรายการบัญชีต่างๆ พร้อมกันได้</span><span class="sxs-lookup"><span data-stu-id="f87a4-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="f87a4-124">คุณสามารถสร้างธุรกรรมของสมุดบัญชีหลักในสมุดรายวันที่มีชั้นของการลงรายการบัญชีที่ตรงกันกับชั้นของการลงรายการบัญชีสมุดบัญชีนั้นได้</span><span class="sxs-lookup"><span data-stu-id="f87a4-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="f87a4-125">ในระหว่างการลงรายการบัญชี ธุรกรรมสมุดบัญชีที่ได้รับจะถูกลงรายการบัญชีที่ชั้นของการลงรายการบัญชีเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="f87a4-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="f87a4-126">สำหรับข้อมูลเพิ่มเติม ดูที่ [สมุดบัญชีที่ได้รับ](derived-books.md) และ [ลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ](post-derived-value-models.md)</span><span class="sxs-lookup"><span data-stu-id="f87a4-126">For more information see, [Derived books](derived-books.md) and [Post with derived books](post-derived-value-models.md).</span></span>



