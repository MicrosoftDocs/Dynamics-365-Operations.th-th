---
title: แบ่งสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายวิธีการแบ่งเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์หนึ่งรายการเป็นสมุดบัญชีสินทรัพย์ใหม่
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138126"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="2a159-103">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2a159-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a159-104">หัวข้อนี้อธิบายวิธีการแบ่งเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์หนึ่งรายการเป็นสมุดบัญชีสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="2a159-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="2a159-105">มีการเข้าถึงข้อมูลบทบาทของนักบัญชีและข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2a159-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="2a159-106">สร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="2a159-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="2a159-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2a159-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="2a159-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="2a159-108">Select **New**.</span></span>
3. <span data-ttu-id="2a159-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2a159-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="2a159-110">หมายเหตุ หมายเลขสินทรัพย์ถาวรที่จะใช้ในกระบวนการแบ่งในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="2a159-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="2a159-111">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="2a159-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="2a159-112">เดนมาร์ก) เป็นไปตามมาตรฐานอักขระสองตัวของ ISO ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="2a159-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="2a159-113">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="2a159-113">Split a fixed asset</span></span>
1. <span data-ttu-id="2a159-114">ในรายการ ค้นหาและเลือกลิงค์ของสินทรัพย์ถาวรที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="2a159-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="2a159-115">เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2a159-115">Select **Books**.</span></span> <span data-ttu-id="2a159-116">เลือกสมุดบัญชีเพื่อแบ่งไปยังสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="2a159-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="2a159-117">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="2a159-117">Select **Functions**.</span></span>
4. <span data-ttu-id="2a159-118">เลือก **แบ่งสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2a159-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="2a159-119">ในฟิลด์ **สินทรัพย์ถาวรสิ้นสุด** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2a159-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="2a159-120">ในฟิลด์ **ไปยังสมุดบัญชี** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="2a159-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2a159-121">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="2a159-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="2a159-122">ในฟิลด์ **เปอร์เซนต์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2a159-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="2a159-123">ในฟิลด์ **ชื่อสมุดรายวัน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2a159-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="2a159-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2a159-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="2a159-125">ลงรายการบัญชีธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="2a159-125">Post the journal transaction</span></span>
1. <span data-ttu-id="2a159-126">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="2a159-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="2a159-127">ในรายการ ให้เลือกสมุดรายวันที่สร้างขึ้นด้วยกระบวนการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="2a159-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="2a159-128">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="2a159-128">Select **Lines**.</span></span>

    - <span data-ttu-id="2a159-129">ตรวจสอบการสร้างรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="2a159-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="2a159-130">สร้างธุรกรรมการปรับปรุงการซื้อสินทรัพย์สำหรับสินทรัพย์เดิมเพื่อลดมูลค่าตามเปอร์เซ็นต์ที่ระบุไว้ในระหว่างกระบวนการแบ่ง </span><span class="sxs-lookup"><span data-stu-id="2a159-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="2a159-131">สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ใหม่สำหรับยอดเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="2a159-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="2a159-132">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2a159-132">Select **Post**.</span></span>

