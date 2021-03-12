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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975952"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="e7bbc-103">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e7bbc-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7bbc-104">หัวข้อนี้อธิบายวิธีการแบ่งเปอร์เซ็นต์ของสมุดบัญชีสินทรัพย์หนึ่งรายการเป็นสมุดบัญชีสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e7bbc-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="e7bbc-105">มีการเข้าถึงข้อมูลบทบาทของนักบัญชีและข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="e7bbc-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="e7bbc-106">สร้างสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="e7bbc-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="e7bbc-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="e7bbc-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-108">Select **New**.</span></span>
3. <span data-ttu-id="e7bbc-109">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7bbc-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="e7bbc-110">หมายเหตุ หมายเลขสินทรัพย์ถาวรที่จะใช้ในกระบวนการแบ่งในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="e7bbc-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="e7bbc-111">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="e7bbc-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="e7bbc-112">เดนมาร์ก เป็นไปตามมาตรฐานอักขระสองตัวของ ISO ปิดแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="e7bbc-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="e7bbc-113">แบ่งสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="e7bbc-113">Split a fixed asset</span></span>

<span data-ttu-id="e7bbc-114">ก่อนที่จะมีการแบ่งสินทรัพย์ที่คิดค่าเสื่อมราคาเต็มจำนวน สถานะของสมุดบัญชีสินทรัพย์ควรมีการเปลี่ยนแปลงด้วยตนเองจาก **ปิด** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="e7bbc-115">ต้องมีขั้นตอนนี้เนื่องจากสถานะของสมุดบัญชีต้อง **เปิด** ถ้าคุณต้องลงรายการบัญชีธุรกรรมสำหรับสินทรัพย์ (ตัวอย่างเช่น สำหรับการขายตัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="e7bbc-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="e7bbc-116">นอกจากนี้คุณต้องเปิดใช้งานพารามิเตอร์ **อนุญาตธุรกรรมต่าง ๆ ภายในหนึ่งใบสำคัญ** บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="e7bbc-117">หลังจากที่มีการเปลี่ยนแปลงสถานะของสมุดบัญชีสินทรัพย์และธุรกรรมต่าง ๆ ภายในใบสำคัญหนึ่งใบได้รับอนุญาต ให้ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อแบ่งสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e7bbc-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="e7bbc-118">ในรายการ ค้นหาและเลือกลิงค์ของสินทรัพย์ถาวรที่จะแบ่ง</span><span class="sxs-lookup"><span data-stu-id="e7bbc-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="e7bbc-119">เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-119">Select **Books**.</span></span> <span data-ttu-id="e7bbc-120">เลือกสมุดบัญชีเพื่อแบ่งไปยังสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="e7bbc-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="e7bbc-121">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-121">Select **Functions**.</span></span>
4. <span data-ttu-id="e7bbc-122">เลือก **แบ่งสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="e7bbc-123">ในฟิลด์ **สินทรัพย์ถาวรสิ้นสุด** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7bbc-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="e7bbc-124">ในฟิลด์ **ไปยังสมุดบัญชี** ให้เลือกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="e7bbc-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e7bbc-125">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="e7bbc-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="e7bbc-126">ในฟิลด์ **เปอร์เซนต์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="e7bbc-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="e7bbc-127">ในฟิลด์ **ชื่อสมุดรายวัน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7bbc-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="e7bbc-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="e7bbc-129">ลงรายการบัญชีธุรกรรมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="e7bbc-129">Post the journal transaction</span></span>

1. <span data-ttu-id="e7bbc-130">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> สินทรัพย์ถาวร \> รายการสมุดรายวัน \> สมุดรายวันของสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="e7bbc-131">ในรายการ ให้เลือกสมุดรายวันที่สร้างขึ้นด้วยกระบวนการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="e7bbc-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="e7bbc-132">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-132">Select **Lines**.</span></span>

    - <span data-ttu-id="e7bbc-133">ตรวจสอบการสร้างรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="e7bbc-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="e7bbc-134">สร้างธุรกรรมการปรับปรุงการซื้อสินทรัพย์สำหรับสินทรัพย์เดิมเพื่อลดมูลค่าตามเปอร์เซ็นต์ที่ระบุไว้ในระหว่างกระบวนการแบ่ง </span><span class="sxs-lookup"><span data-stu-id="e7bbc-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="e7bbc-135">สร้างธุรกรรมการซื้อสินทรัพย์สำหรับสินทรัพย์ใหม่สำหรับยอดเงินเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e7bbc-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="e7bbc-136">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="e7bbc-136">Select **Post**.</span></span>
