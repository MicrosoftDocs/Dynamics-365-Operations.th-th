---
title: นำเสนอการซื้อสินทรัพย์ถาวร
description: กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "350653"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="777c9-103">นำเสนอการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="777c9-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="777c9-104">กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="777c9-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="777c9-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="777c9-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="777c9-106">ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="777c9-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="777c9-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="777c9-107">Click New.</span></span>
3. <span data-ttu-id="777c9-108">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="777c9-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="777c9-109">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="777c9-109">Click Lines.</span></span>
5. <span data-ttu-id="777c9-110">คลิกข้อเสนอ</span><span class="sxs-lookup"><span data-stu-id="777c9-110">Click Proposals.</span></span>
6. <span data-ttu-id="777c9-111">คลิกที่ข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="777c9-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="777c9-112">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="777c9-112">Click Filter.</span></span>
8. <span data-ttu-id="777c9-113">คลิกรีเซ็ตเพื่อล้างค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="777c9-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="777c9-114">เลือกแถวจำนวนสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="777c9-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="777c9-115">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="777c9-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="777c9-116">กำหนดเงื่อนไขที่เหลือสำหรับสินทรัพย์ถาวรที่คุณต้องการได้รับกับข้อเสนอนี้</span><span class="sxs-lookup"><span data-stu-id="777c9-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="777c9-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777c9-117">Click OK.</span></span>
12. <span data-ttu-id="777c9-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="777c9-118">Click OK.</span></span>
    * <span data-ttu-id="777c9-119">ตรวจสอบการทำธุรกรรมที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="777c9-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="777c9-120">เฉพาะสินทรัพย์ถาวรที่มีวันที่ซื้อสินทรัพย์ และราคาทุนของสินทรัพย์ที่ตั้งค่าไว้ในสมุดบัญชีจะรวมอยู่ในข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="777c9-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="777c9-121">คลิกแท็บสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="777c9-121">Click the Books tab.</span></span>
14. <span data-ttu-id="777c9-122">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="777c9-122">Click Post.</span></span>

