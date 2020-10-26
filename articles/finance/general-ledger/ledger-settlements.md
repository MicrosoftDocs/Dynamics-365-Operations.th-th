---
title: การชำระบัญชีแยกประเภท
description: หัวข้อนี้อธิบายวิธีการใช้หน้าการชำระบัญชีแยกประเภท เพื่อชำระธุรกรรมบัญชีแยกประเภท และกลับรายการการชำระ
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977130"
---
# <a name="ledger-settlements"></a><span data-ttu-id="7746d-103">การชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7746d-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7746d-104">การชำระบัญชีแยกประเภทช่วยให้คุณสามารถจับคู่ธุรกรรมเดบิตและเครดิตในบัญชีแยกประเภททั่วไป และทำเครื่องหมายเป็นจ่ายเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7746d-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="7746d-105">ด้วยวิธีนี้ คุณสามารถมั่นใจว่า ธุรกรรมที่เกี่ยวข้องถูกล้างออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="7746d-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="7746d-106">คุณยังสามารถกลับรายการการชำระ ถ้ามีการดำเนินการโดยไม่ได้ตั้งใจ</span><span class="sxs-lookup"><span data-stu-id="7746d-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="7746d-107">เปิดใช้งานการชำระบัญชีแยกประเภทขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7746d-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="7746d-108">หน้าการชำระบัญชีแยกประเภทขั้นสูงให้ความสามารถเพิ่มเติม สำหรับการกรองข้อมูลและการเลือกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7746d-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="7746d-109">ในการเปิดใช้งานหน้าการชำระบัญชีแยกประเภทขั้นสูง ให้ปฏิบัติตามขั้นตอนดังนี้</span><span class="sxs-lookup"><span data-stu-id="7746d-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="7746d-110">เลือก **บัญชีแยกประเภททั่วไป** \> **การตั้งค่าบัญชีแยกประเภท** \> **พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="7746d-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="7746d-111">บนแท็บ **การจับคู่บัญชีแยกประเภท** ตั้งค่าตัวเลือก **การชำระบัญชีแยกประเภทขั้นสูง** เป็น **ใช่** เพื่อเปิดใช้งานฟังก์ชันการชำระบัญชีแยกประเภทขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7746d-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="7746d-112">หน้า **การชำระบัญชีแยกประเภท** ขั้นสูง จะถูกใช้เมื่อคุณเลือก **การชำระบัญชีแยกประเภท** ใน **งานประจำงวด**</span><span class="sxs-lookup"><span data-stu-id="7746d-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="7746d-113">คุณต้องป้อนรายการของบัญชีที่จะใช้สำหรับการชำระบัญชีแยกประเภทสำหรับผังบัญชีแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="7746d-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="7746d-114">รายการนี้จะใช้เพื่อกรองข้อมูลรายการธุรกรรมที่ปรากฏในหน้า **การชำระบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="7746d-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="7746d-115">ในรายการ **ผังบัญชี** เลือกผังบัญชี และจากนั้น เลือก **สร้าง** เพื่อเพิ่มบัญชีใหม่ลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="7746d-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="7746d-116">ชำระธุรกรรม โดยใช้หน้าการชำระบัญชีแยกประเภทขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="7746d-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="7746d-117">เมื่อต้องการชำระธุรกรรมบัญชีแยกประเภท ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7746d-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="7746d-118">เลือก **บัญชีแยกประเภททั่วไป** \> **งานประจำงวด** \> **การชำระบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="7746d-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="7746d-119">ตั้งค่าตัวกรองที่ด้านบนของหน้า:</span><span class="sxs-lookup"><span data-stu-id="7746d-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="7746d-120">เลือกช่วงวันที่ หรือเลือก **รหัสช่วงวันที่** เพื่อกรอกช่วงวันที่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7746d-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="7746d-121">เปลี่ยนแปลงชั้นการลงรายการบัญชี ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7746d-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="7746d-122">ในการแสดงบัญชีแยกประเภทและมิติโดยแยกต่างหาก เลือกชุดมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="7746d-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="7746d-123">เลือก **แสดงธุรกรรม** เพื่อแสดงธุรกรรมทั้งหมดที่ตรงกับตัวกรองที่คุณตั้งค่าและรายการบัญชีที่คุณระบุ เมื่อคุณตั้งค่ารายการผังบัญชีในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7746d-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="7746d-124">ถ้าคุณเปลี่ยนแปลงตัวกรองหรือชุดมิติใดๆ คุณต้องเลือก **แสดงธุรกรรม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="7746d-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="7746d-125">เลือกรายการอย่างน้อยหนึ่งรายการที่คุณกำลังพิจารณาสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7746d-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="7746d-126">ค่าของฟิลด์ **ยอดเงินที่เลือก** ที่ด้านบนของหน้า เพิ่มหรือลดด้วยยอดเงินรวมในรายการที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="7746d-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="7746d-127">หลังจากที่คุณเสร็จสิ้นการเลือกธุรกรรม เลือก **ทำเครื่องหมายรายการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="7746d-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="7746d-128">เครื่องหมายถูกปรากฏขึ้นในคอลัมน์ **ที่ทำเครื่องหมาย** สำหรับธุรกรรมแต่ละรายการที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="7746d-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="7746d-129">นอกจากนี้ ค่าของฟิลด์ **จำนวนที่มีการทำเครื่องหมาย** เหนือกริด เพิ่มหรือลดโดยจำนวนรวมของรายการที่คุณทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="7746d-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="7746d-130">เมื่อค่า **จำนวนที่ทำเครื่องหมาย** คือ **0** (ศูนย์) เลือก **ชำระธุรกรรมที่ทำเครื่องหมาย**</span><span class="sxs-lookup"><span data-stu-id="7746d-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="7746d-131">สถานะของธุรกรรมที่ทำเครื่องหมายจะถูกปรับปรุงเป็น **ชำระแล้ว**</span><span class="sxs-lookup"><span data-stu-id="7746d-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="7746d-132">ทำให้ค้นหาธุรกรรมได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="7746d-132">Make transactions easier to find</span></span>

<span data-ttu-id="7746d-133">หน้า **การชำระบัญชีแยกประเภท** ประกอบด้วยความสามารถที่ทำให้ดูธุรกรรมที่คุณต้องใช้สำหรับการชำระเงินง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="7746d-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="7746d-134">ปุ่ม **ยกเลิกการทำเครื่องหมายรายการที่เลือก** ล้างข้อมูลฟิลด์ **ที่ทำเครื่องหมาย** สำหรับรายการทั้งหมดที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7746d-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="7746d-135">ตัวกรอง **ที่ทำเครื่องหมาย** ช่วยให้คุณสามารถกรองธุรกรรมที่ขึ้นอยู่กับว่าฟิลด์ **ที่ทำเครื่องหมาย** จะถูกเลือก หรือถูกยกเลิกการเลือก</span><span class="sxs-lookup"><span data-stu-id="7746d-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="7746d-136">ตัวกรอง **สถานะ** ช่วยให้คุณสามารถกรองธุรกรรมที่ขึ้นอยู่กับว่าสถานะของพวกเขาคือ **ชำระแล้ว** หรือ **ยังไม่ได้ชำระ**</span><span class="sxs-lookup"><span data-stu-id="7746d-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="7746d-137">ปุ่ม **เรียงตามจำนวนเต็ม** ช่วยให้คุณสามารถเรียงลำดับจำนวนค่าสัมบูรณ์ เพื่อให้คุณสามารถจัดกลุ่มเดบิตและเครดิตที่มียอดเงินเดียวกันเข้าด้วยกัน</span><span class="sxs-lookup"><span data-stu-id="7746d-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="7746d-138">กลับรายการการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7746d-138">Reverse a settlement</span></span>

<span data-ttu-id="7746d-139">คุณสามารถกลับรายการการชำระเงินที่ทำโดยไม่ได้ตั้งใจ</span><span class="sxs-lookup"><span data-stu-id="7746d-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="7746d-140">ทำตามขั้นตอนที่ 1 ถึง 3 ในส่วน "ชำระธุรกรรม โดยใช้หน้าการชำระบัญชีแยกประเภทขั้นสูง" เพื่อแสดงธุรกรรมที่คุณกำลังค้นหา</span><span class="sxs-lookup"><span data-stu-id="7746d-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="7746d-141">ในตัวกรอง **สถานะ** เลือก **ชำระแล้ว**</span><span class="sxs-lookup"><span data-stu-id="7746d-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="7746d-142">เลือกรายการอย่างน้อยหนึ่งรายการที่คุณกำลังพิจารณาสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="7746d-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="7746d-143">ค่าของฟิลด์ **ยอดเงินที่เลือก** ที่ด้านบนของหน้า เพิ่มหรือลดด้วยยอดเงินรวมในรายการที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="7746d-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="7746d-144">หลังจากที่คุณเสร็จสิ้นการเลือกธุรกรรม เลือก **ทำเครื่องหมายรายการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="7746d-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="7746d-145">เครื่องหมายถูกปรากฏขึ้นในคอลัมน์ **ที่ทำเครื่องหมาย** สำหรับธุรกรรมแต่ละรายการที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="7746d-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="7746d-146">นอกจากนี้ ค่าของฟิลด์ **จำนวนที่มีการทำเครื่องหมาย** ที่ด้านบนของหน้า เพิ่มหรือลดโดยจำนวนรวมของรายการที่คุณทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="7746d-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="7746d-147">เมื่อค่า **จำนวนที่ทำเครื่องหมาย** คือ **0** (ศูนย์) เลือก **กลับรายการธุรกรรมที่ทำเครื่องหมาย**</span><span class="sxs-lookup"><span data-stu-id="7746d-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="7746d-148">สถานะของธุรกรรมทำเครื่องหมายจะถูกปรับปรุงเป็น **ยังไม่ได้ชำระ**</span><span class="sxs-lookup"><span data-stu-id="7746d-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="7746d-149">อัพเดตรายการของบัญชีที่รวมอยู่ในรายการของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7746d-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="7746d-150">เลือก **บัญชีการชำระบัญชีแยกประเภท** เพื่อเปิดกล่องโต้ตอบที่ซึ่งคุณสามารถแก้ไขบัญชีที่รวมอยู่ในรายการธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="7746d-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="7746d-151">เลือก **สร้าง** เพื่อเพิ่มบัญชีใหม่ลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="7746d-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="7746d-152">รายการนี้จะใช้เพื่อกรองข้อมูลรายการธุรกรรมที่ปรากฏในหน้า **การชำระบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="7746d-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
