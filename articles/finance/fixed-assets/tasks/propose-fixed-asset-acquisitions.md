---
title: นำเสนอการซื้อสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายวิธีการได้รับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205039"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="857f7-103">นำเสนอการซื้อสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="857f7-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="857f7-104">หัวข้อนี้อธิบายวิธีการได้รับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="857f7-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="857f7-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="857f7-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="857f7-106">เมื่อต้องการรับสินทรัพย์ถาวรโดยใช้สมุดรายวันข้อเสนอสินทรัพย์ถาวร คุณต้องสร้างเรกคอร์ดสินทรัพย์ถาวรก่อนแล้วกำหนดราคาการซื้อสินทรัพย์ในสมุดบัญชีสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="857f7-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="857f7-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="857f7-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="857f7-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="857f7-108">Select **New**.</span></span>
3. <span data-ttu-id="857f7-109">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="857f7-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="857f7-110">ในบานหน้าต่างการดำเนินการ เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="857f7-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="857f7-111">เลือก **ข้อเสนอ**</span><span class="sxs-lookup"><span data-stu-id="857f7-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="857f7-112">เลือก **ข้อเสนอการซื้อสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="857f7-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="857f7-113">เลือก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="857f7-113">Select **Filter**.</span></span> <span data-ttu-id="857f7-114">เลือก **รีเซ็ต** เพื่อล้างค่าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="857f7-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="857f7-115">เลือกแถว **จำนวนสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="857f7-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="857f7-116">ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="857f7-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="857f7-117">กำหนดเงื่อนไขที่เหลือสำหรับสินทรัพย์ถาวรที่คุณต้องการได้รับกับข้อเสนอนี้</span><span class="sxs-lookup"><span data-stu-id="857f7-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="857f7-118">เลือก **ตกลง** สองครั้ง เพื่อออกจากบานหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="857f7-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="857f7-119">ตรวจสอบการทำธุรกรรมที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="857f7-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="857f7-120">เฉพาะสินทรัพย์ถาวรที่มีวันที่ซื้อสินทรัพย์ และราคาทุนของสินทรัพย์ที่ตั้งค่าไว้ในสมุดบัญชีจะรวมอยู่ในข้อเสนอการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="857f7-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="857f7-121">บนหน้า เลือกแท็บ **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="857f7-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="857f7-122">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="857f7-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]