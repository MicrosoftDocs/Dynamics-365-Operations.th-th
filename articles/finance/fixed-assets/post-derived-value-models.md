---
title: ลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ
description: บทความนี้อธิบายวิธีการใช้สมุดบัญชี
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 628110e62d30a717b243530367196aeaf930e3e3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256750"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="ce35a-103">ลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="ce35a-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce35a-104">บทความนี้อธิบายวิธีการใช้สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="ce35a-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="ce35a-105">เมื่อคุณลงรายบัญชีธุรกรรมสำหรับสมุดบัญชีที่ประกอบด้วยสมุดบัญชีที่ได้รับ ธุรกรรมสมุดบัญชีที่ได้รับนี้จะมีการลงรายการบัญชีโดยอัตโนมัติในสมุดรายวัน ใบสั่งซื้อ หรือใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="ce35a-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="ce35a-106">อย่างไรก็ตาม ถ้าคุณจัดเตรียมธุรกรรมสมุดบัญชีหลักในสมุดรายวันสินทรัพย์ถาวร คุณสามารถดูและแก้ไขยอดเงินของธุรกรรมที่ได้รับก่อนที่จะลงรายการบัญชีธุรกรรมเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="ce35a-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="ce35a-107">บัญชีบางบัญชี เช่น บัญชีภาษีขายและบัญชีลูกค้าหรือผู้จัดจำหน่าย จะถูกอัพเดตเพียงครั้งเดียวด้วยการลงรายการบัญชีสมุดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ce35a-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="ce35a-108">ธุรกรรมสมุดบัญชีที่ได้รับจะมีการลงรายการบัญชีไปยังบัญชีที่กำหนดไว้สำหรับสมุดบัญชีที่ได้รับในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="ce35a-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="ce35a-109">การซื้อสินทรัพย์มักใช้เป็นชนิดธุรกรรมสำหรับสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="ce35a-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="ce35a-110">คุณจะใช้ธุรกรรมชนิดนี้เมื่อใช้สมุดบัญชีและสมุดบัญชีค่าเสื่อมราคาที่ได้รับกับสินทรัพย์ถาวรตั้งแต่เมื่อซื้อสินทรัพย์ถาวรนั้นมา</span><span class="sxs-lookup"><span data-stu-id="ce35a-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="ce35a-111">มูลค่าอื่นๆ สำหรับชนิดธุรกรรมสามารถใช้ได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="ce35a-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="ce35a-112">นอกจากนี้ คุณสามารถใช้ค่าอื่นๆ สำหรับชนิดธุรกรรมได้เช่นกัน ตัวอย่างเช่น ถ้าสมุดบัญชีหลักและสมุดบัญชีที่ได้รับอยู่ในช่วงเดียวกัน ซึ่งเกี่ยวข้องกับการขายหรือการตัดจำหน่าย ชนิดธุรกรรมสินทรัพย์ถาวรทั้งหมดจะพร้อมใช้งานสำหรับการตั้งค่าสมุดบัญชีค่าเสื่อมราคาที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="ce35a-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="ce35a-113">ค่าเสื่อมราคาที่ลงรายการบัญชีในสมุดบัญชีที่ได้รับจะเป็นจำนวนยอดเงินเดียวกันกับที่ลงรายการบัญชีไว้สำหรับสมุดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="ce35a-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="ce35a-114">ถ้าวิธีการคิดค่าเสื่อมราคาแตกต่างกันระหว่างสมุดบัญชีต่างๆ คุณไม่ควรสร้างธุรกรรมค่าเสื่อมราคาโดยใช้กระบวนการที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="ce35a-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="ce35a-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ce35a-115">Example</span></span> 
<span data-ttu-id="ce35a-116">ข้อมูลต่อไปนี้อธิบายวิธีการตั้งค่าธุรกรรมการซื้อด้วยฟังก์ชันสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="ce35a-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="ce35a-117">สร้างสมุดบัญชีบนหน้าสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="ce35a-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="ce35a-118">สมุดบัญชีสำหรับการลงบัญชี: VM 1 ชั้นการลงรายการบัญชีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ce35a-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="ce35a-119">สมุดบัญชีสำหรับวัตถุประสงค์ด้านภาษี: VM 2 ชั้นของการลงรายการบัญชีภาษี</span><span class="sxs-lookup"><span data-stu-id="ce35a-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="ce35a-120">บน VM 1 คลิกแท็บสมุดบัญชีที่ได้รับมา และเลือก VM 2 ในฟิลด์สมุดบัญชี และการซื้อสินทรัพย์ในฟิลด์ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="ce35a-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="ce35a-121">จากนั้น ก็สามารถแนบสมุดบัญชีกับสินทรัพย์ถาวรที่เฉพาะเจาะจงได้</span><span class="sxs-lookup"><span data-stu-id="ce35a-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="ce35a-122">เมื่อมีการลงรายการบัญชีการซื้อสำหรับสินทรัพย์ถาวรที่มีสมุดบัญชี VM 1 จะมีการลงรายการบัญชีการซื้อไม่เพียงแต่ใน VM 1 เท่านั้น แต่ยังลงบัญชีในสมุดบัญชีที่ได้รับ VM 2 อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="ce35a-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="ce35a-123">สถานะของสมุดบัญชีสินทรัพย์ถาวรทั้งสองจะถูกอัพเดตเป็นเปิด</span><span class="sxs-lookup"><span data-stu-id="ce35a-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="ce35a-124">ถ้าคุณไม่ใช้สมุดบัญชีที่ได้รับ คุณต้องลงรายการบัญชีการซื้อสินทรัพย์ถาวรทั้งสำหรับสมุดบัญชี VM 1 และสมุดบัญชี VM 2</span><span class="sxs-lookup"><span data-stu-id="ce35a-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="ce35a-125">สำหรับข้อมูลเพิ่มเติม ดู [สมุดบัญชีที่ได้รับ](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="ce35a-125">For more information, see [Derived books](derived-books.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]