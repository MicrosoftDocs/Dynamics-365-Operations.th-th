---
title: กลับรายการธุรกรรมสัญญาเช่าที่ลงรายการบัญชี
description: หัวข้อนี้จะอธิบายถึงวิธีการกลับรายการธุรกรรมการเช่าที่ลงรายการบัญชี ธุรกรรมใดๆ ที่สร้างขึ้นโดยการเช่าสินทรัพย์สามารถกลับรายการได้
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969539"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="99715-104">กลับรายการธุรกรรมสัญญาเช่าที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="99715-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99715-105">ธุรกรรมใดๆ ที่สร้างขึ้นโดยการเช่าสินทรัพย์สามารถกลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="99715-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="99715-106">ธุรกรรมที่กลับรายการโดยการเช่าสินทรัพย์อัปเดตข้อมูลการเช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="99715-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="99715-107">ดังนั้น จึงอัปเดตค่าการถือครองของหนี้สินสัญญาเช่าและสิทธิ์การใช้สินทรัพย์ (ROU)</span><span class="sxs-lookup"><span data-stu-id="99715-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="99715-108">เมื่อต้องการสร้างธุรกรรมการกลับรายการสำหรับการเช่า ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="99715-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="99715-109">บนหน้า **ธุรกรรมสินทรัพย์** หรือหน้า **ธุรกรรมหนี้สิน** เลือกธุรกรรม จากนั้นเลือก **กลับรายการธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="99715-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="99715-110">ในกล่องโต้ตอบที่ปรากฏขึ้น คุณสามารถแก้ไขวันที่ที่จะลงรายการบัญชีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="99715-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="99715-111">ตามค่าเริ่มต้น ฟิลด์ **วันที่** จะถูกตั้งค่าเป็นวันที่ลงรายการบัญชีธุรกรรมของธุรกรรมที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="99715-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="99715-112">ไม่สามารถลงรายการบัญชีการกลับรายการก่อนหน้าวันที่ลงรายการบัญชีเดิมของธุรกรรมที่เลือก</span><span class="sxs-lookup"><span data-stu-id="99715-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="99715-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="99715-113">Select **OK**.</span></span> <span data-ttu-id="99715-114">การลงรายการบัญชีรายการสมุดรายวันที่กลับรายการที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="99715-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="99715-115">การกลับรายการจะแสดงอยู่บนหน้า **ธุรกรรมสินทรัพย์** หรือ **ธุรกรรมหนี้สิน** และยอดรวมสุทธิของยอดดุลปัจจุบันที่แสดงบนหน้าจะถูกอัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="99715-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="99715-116">เมื่อคุณเลือก **การสืบค้นกลับที่มีการกลับรายการ** กล่องโต้ตอบจะปรากฏขึ้น ซึ่งแสดงทั้งธุรกรรมเดิมและธุรกรรมที่กลับรายการ พร้อมกับหมายเลขที่เชื่อมโยงซึ่งเรียกว่า *หมายเลขการติดตาม*</span><span class="sxs-lookup"><span data-stu-id="99715-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="99715-117">เพื่อให้สามารถทำความเข้าใจและปรับปรุงการกลับรายการได้ง่ายขึ้น คุณยังสามารถติดตามการกลับรายการโดยใช้กำหนดการเช่าได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="99715-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="99715-118">ฟิลด์ **หมายเลขสมุดรายวันล่าสุด** บนหน้า **กำหนดการ** แสดงหมายเลขสมุดรายวันของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="99715-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="99715-119">เมื่อมีการกลับรายการธุรกรรม ฟิลด์นี้จะถูกอัปเดตด้วยหมายเลขสมุดรายวันของธุรกรรมการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="99715-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="99715-120">นอกจากนี้ กล่องกาเครื่องหมาย **การกลับรายการ** ถูกเลือกเพื่อบ่งชี้ว่ามีการกลับรายการธุรกรรม และฟิลด์ **ลงรายการบัญชีแล้ว** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="99715-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="99715-121">การยกเลิกธุรกรรมที่กลับรายการ</span><span class="sxs-lookup"><span data-stu-id="99715-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="99715-122">เมื่อต้องการยกเลิกธุรกรรมที่กลับรายการ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="99715-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="99715-123">บนหน้า **กำหนดการ** หรือหน้า **ธุรกรรม** ให้เลือกธุรกรรมเดิม</span><span class="sxs-lookup"><span data-stu-id="99715-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="99715-124">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="99715-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="99715-125">ถ้าคุณเลือกธุรกรรม ในหน้า **กำหนดการ** ให้ทำตามขั้นตอนสำหรับการสร้างสมุดรายวัน ใน [สร้างรายการสมุดรายวันรายเดือนในชุดงาน](create-monthly-journals-batch.md)</span><span class="sxs-lookup"><span data-stu-id="99715-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="99715-126">คุณต้องลงรายการบัญชีสมุดรายวันด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="99715-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="99715-127">ถ้าคุณเลือกธุรกรรมไว้ในหน้า **ธุรกรรม** ให้เลือก **กลับรายการธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="99715-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="99715-128">คุณได้รับข้อความแจ้งว่าการเพิกถอนนี้เป็นการยกเลิกการกลับรายการก่อนหน้านี้ และคุณสามารถแก้ไขวันที่ลงรายการบัญชีสำหรับการยกเลิกนี้ได้</span><span class="sxs-lookup"><span data-stu-id="99715-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="99715-129">อย่างไรก็ตาม การตรวจสอบความถูกต้องของธุรกิจทั่วไปจะมีผลต่อวันที่ที่สามารถป้อนในฟิลด์ **วันที่**</span><span class="sxs-lookup"><span data-stu-id="99715-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="99715-130">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="99715-130">Select **OK**.</span></span> <span data-ttu-id="99715-131">การลงรายการบัญชีรายการสมุดรายวันที่กลับรายการที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="99715-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="99715-132">การกลับรายการจะแสดงอยู่บนหน้า **ธุรกรรม** และจะมีการคืนค่ายอดดุลปัจจุบันของยอดรวมสุทธิเป็นค่าก่อนที่จะมีการกลับรายการแรก</span><span class="sxs-lookup"><span data-stu-id="99715-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="99715-133">ดังนั้น ผลกระทบที่มีต่อการกลับรายการในยอดดุล คือถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="99715-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="99715-134">เมื่อคุณเลือก **การสืบค้นกลับที่มีการกลับรายการ** กล่องโต้ตอบจะปรากฏขึ้น ซึ่งแสดงทั้งธุรกรรมเดิมและธุรกรรมที่กลับรายการ พร้อมกับหมายเลขการติดตามที่เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="99715-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="99715-135">นอกจากนี้คุณยังสามารถติดตามการเพิกถอน โดยใช้หน้า **กำหนดการ** ที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="99715-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="99715-136">ฟิลด์ **การกลับรายการ** ถูกล้าง ในขณะที่ฟิลด์ **ลงรายการบัญชีสมุดรายวัน** ถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="99715-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="99715-137">นอกจากนี้ฟิลด์ **หมายเลขสมุดรายวันล่าสุด** ถูกอัปเดตด้วยหมายเลขสมุดรายวันของธุรกรรมการเพิกถอน และฟิลด์ **หมายเลขสมุดรายวัน** จะมีการอัปเดตด้วยหมายเลขสมุดรายวันการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="99715-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
