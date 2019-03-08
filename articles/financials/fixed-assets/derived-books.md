---
title: สมุดบัญชีที่ได้รับ
description: บทความนี้แสดงภาพรวมของฟังก์ชันสมุดบัญชีที่ได้รับ
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 153b6437205d5a849fa6a90c0d3b9f3d51dd6768
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "313922"
---
# <a name="derived-books"></a><span data-ttu-id="78045-103">สมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="78045-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78045-104">บทความนี้แสดงภาพรวมของฟังก์ชันสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="78045-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="78045-105">วัตถุประสงค์ของสมุดบัญชีที่ได้รับคือ เพื่อให้การลงรายการบัญชีธุรกรรมสมุดบัญชีสินทรัพย์ถาวร ที่วางแผนไว้สำหรับช่วงเวลาที่สม่ำเสมอ เป็นไปได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="78045-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="78045-106">คุณสามารถเลือกสมุดบัญชีหนึ่งรายการเป็นสมุดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="78045-106">You choose one book as the primary book.</span></span> <span data-ttu-id="78045-107">โดยปกติแล้วนี่คือสมุดบัญชีที่ใช้สำหรับการคิดค่าเสื่อมราคาทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="78045-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="78045-108">จากนั้นคุณสามารถแนบกับสมุดบัญชีอื่นๆ ที่ถูกตั้งค่าไว้เพื่อลงรายบัญชีธุรกรรมในช่วงเวลาเดียวกับสมุดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="78045-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="78045-109">สมุดบัญชีค่าเสื่อมราคาภาษีมักจะถูกตั้งค่าเป็นสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="78045-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="78045-110">ธุรกรรมที่พบได้บ่อยที่สุดที่จะตั้งค่าให้ลงรายการบัญชีที่สมุดบัญชีที่ได้รับคือ การซื้อสินทรัพย์ การปรับปรุงการซื้อสินทรัพย์ และการตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="78045-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="78045-111">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="78045-111">Example</span></span>

<span data-ttu-id="78045-112">สมุดบัญชี B และ C ถูกตั้งค่าเป็นหนังสือที่ได้รับสำหรับสมุดบัญชี A สำหรับชนิดของธุรกรรมการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="78045-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="78045-113">ในสมุดบัญชี A ให้คุณป้อนธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ 123 เป็นเงิน 1,500.00</span><span class="sxs-lookup"><span data-stu-id="78045-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="78045-114">เมื่อมีการลงรายการบัญชีธุรกรรม ธุรกรรมการซื้อจะถูกสร้างขึ้นและลงรายการบัญชีในสินทรัพย์ 123 สำหรับสมุดบัญชี B และในสินทรัพย์ 123 สำหรับสมุดบัญชี C เป็นเงิน 1,500.00</span><span class="sxs-lookup"><span data-stu-id="78045-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="78045-115">เมื่อคุณเตรียมธุรกรรมของสมุดบัญชีหลักสำหรับการลงรายการบัญชีในสมุดรายวันสินทรัพย์ถาวร คุณสามารถดู และแก้ไขธุรกรรมของสมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="78045-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="78045-116">ถ้าคุณจัดเตรียมธุรกรรมมูลสมุดบัญชีหลักในสมุดรายวันอื่น ธุรกรรมของมูลค่าที่ได้รับจะไม่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="78045-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="78045-117">อย่างไรก็ตาม จะมีการลงรายการบัญชีธุรกรรมนั้นที่บัญชีและชั้นของการลงรายการบัญชีที่เหมาะสม เมื่อคุณลงรายการบัญชีธุรกรรมสมุดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="78045-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="78045-118">สมุดบัญชีที่มีการตั้งค่าให้ลงรายการบัญชีธุรกรรมเป็นช่วงๆ ที่ไม่ใช่ช่วงของสมุดบัญชีหลัก ต้องแนบกับสินทรัพย์ถาวรเป็นสมุดบัญชีที่แยกต่างหาก และไม่ใช่สมุดบัญชีที่ได้รับ</span><span class="sxs-lookup"><span data-stu-id="78045-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="78045-119">สำหรับข้อมูลเพิ่มเติม ดู [การลงรายการบัญชีด้วยสมุดบัญชีที่ได้รับ](post-derived-value-models.md)</span><span class="sxs-lookup"><span data-stu-id="78045-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>



