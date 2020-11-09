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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000304"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="6ff53-103">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="6ff53-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ff53-104">หัวข้อนี้อธิบายวิธีการแบ่งเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์หนึ่งรายการเป็นสมุดบัญชีสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ff53-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="6ff53-105">มีการเข้าถึงข้อมูลบทบาทของนักบัญชีและข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="6ff53-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="6ff53-106">สร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="6ff53-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="6ff53-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="6ff53-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="6ff53-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="6ff53-108">Select **New**.</span></span>
3. <span data-ttu-id="6ff53-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ff53-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="6ff53-110">หมายเหตุ หมายเลขสินทรัพย์ถาวรที่จะใช้ในกระบวนการแบ่งในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="6ff53-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="6ff53-111">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6ff53-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="6ff53-112">เดนมาร์ก เป็นไปตามมาตรฐานอักขระสองตัวของ ISO ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="6ff53-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="6ff53-113">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="6ff53-113">Split a fixed asset</span></span>

<span data-ttu-id="6ff53-114">ก่อนที่จะมีการแบ่งสินทรัพย์ที่คิดค่าเสื่อมราคาเต็มจำนวน สถานะของสมุดบัญชีสินทรัพย์ควรมีการเปลี่ยนแปลงด้วยตนเองจาก **ปิด** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="6ff53-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="6ff53-115">ต้องมีขั้นตอนนี้เนื่องจากสถานะของสมุดบัญชีต้อง **เปิด** ถ้าคุณต้องลงรายการบัญชีธุรกรรมสำหรับสินทรัพย์ (ตัวอย่างเช่น สำหรับการขายตัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="6ff53-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="6ff53-116">หลังจากมีการเปลี่ยนสถานะของสมุดบัญชีสินทรัพย์ ให้ทำตามขั้นตอนต่อไปนี้เพื่อแบ่งสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6ff53-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="6ff53-117">ในรายการ ค้นหาและเลือกลิงค์ของสินทรัพย์ถาวรที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="6ff53-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="6ff53-118">เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="6ff53-118">Select **Books**.</span></span> <span data-ttu-id="6ff53-119">เลือกสมุดบัญชีเพื่อแบ่งไปยังสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6ff53-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="6ff53-120">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="6ff53-120">Select **Functions**.</span></span>
4. <span data-ttu-id="6ff53-121">เลือก **แบ่งสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="6ff53-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="6ff53-122">ในฟิลด์ **สินทรัพย์ถาวรสิ้นสุด** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ff53-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="6ff53-123">ในฟิลด์ **ไปยังสมุดบัญชี** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="6ff53-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6ff53-124">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6ff53-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="6ff53-125">ในฟิลด์ **เปอร์เซนต์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6ff53-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="6ff53-126">ในฟิลด์ **ชื่อสมุดรายวัน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="6ff53-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="6ff53-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="6ff53-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="6ff53-128">ลงรายการบัญชีธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="6ff53-128">Post the journal transaction</span></span>

1. <span data-ttu-id="6ff53-129">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> สินทรัพย์ถาวร \> รายการสมุดรายวัน \> สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="6ff53-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="6ff53-130">ในรายการ ให้เลือกสมุดรายวันที่สร้างขึ้นด้วยกระบวนการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="6ff53-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="6ff53-131">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="6ff53-131">Select **Lines**.</span></span>

    - <span data-ttu-id="6ff53-132">ตรวจสอบการสร้างรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="6ff53-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="6ff53-133">สร้างธุรกรรมการปรับปรุงการซื้อสินทรัพย์สำหรับสินทรัพย์เดิมเพื่อลดมูลค่าตามเปอร์เซ็นต์ที่ระบุไว้ในระหว่างกระบวนการแบ่ง </span><span class="sxs-lookup"><span data-stu-id="6ff53-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="6ff53-134">สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ใหม่สำหรับยอดเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="6ff53-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="6ff53-135">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="6ff53-135">Select **Post**.</span></span>
