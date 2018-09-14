--- 
title: "ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ"
description: "กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 742c7d732ff121bff841ac0149b15bef5a94c756
ms.contentlocale: th-th
ms.lasthandoff: 09/14/2018

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="967ed-103">ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="967ed-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="967ed-104">กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="967ed-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="967ed-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="967ed-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="967ed-106">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="967ed-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="967ed-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="967ed-107">Click New.</span></span>
3. <span data-ttu-id="967ed-108">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="967ed-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="967ed-109">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="967ed-109">Click Lines.</span></span>
5. <span data-ttu-id="967ed-110">คลิกข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="967ed-110">Click Proposals.</span></span>
6. <span data-ttu-id="967ed-111">คลิกที่ข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="967ed-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="967ed-112">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="967ed-112">Click Filter.</span></span>
8. <span data-ttu-id="967ed-113">คลิกรีเซ็ตเพื่อล้างค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="967ed-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="967ed-114">เลือกแถวจำนวนสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="967ed-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="967ed-115">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="967ed-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="967ed-116">กำหนดเงื่อนไขที่เหลือสำหรับสินทรัพย์ถาวรที่คุณต้องการได้รับกับข้อเสนอนี้</span><span class="sxs-lookup"><span data-stu-id="967ed-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="967ed-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="967ed-117">Click OK.</span></span>
12. <span data-ttu-id="967ed-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="967ed-118">Click OK.</span></span>
    * <span data-ttu-id="967ed-119">ตรวจสอบการทำธุรกรรมที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="967ed-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="967ed-120">เฉพาะสินทรัพย์ถาวรที่มีวันที่ซื้อสินทรัพย์ และราคาทุนของสินทรัพย์ที่ตั้งค่าไว้ในสมุดบัญชีจะรวมอยู่ในข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="967ed-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="967ed-121">คลิกแท็บสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="967ed-121">Click the Books tab.</span></span>
14. <span data-ttu-id="967ed-122">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="967ed-122">Click Post.</span></span>


