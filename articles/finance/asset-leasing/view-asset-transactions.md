---
title: ดูธุรกรรมการหนี้สิน สินทรัพย์ และค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายถึงวิธีการดูธุรกรรมสำหรับสินทรัพย์ที่ให้เช่า ธุรกรรมเหล่านี้รวมถึงธุรกรรมหนี้สินสัญญาเช่าและธุรกรรมค่าใช้จ่ายในการจัดการสินทรัพย์ที่ลงรายการบัญชีแล้ว
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448624"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="e065d-104">ดูธุรกรรมการหนี้สิน สินทรัพย์ และค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e065d-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e065d-105">หัวข้อนี้จะอธิบายถึงวิธีการดูธุรกรรมสำหรับสินทรัพย์ที่ให้เช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="e065d-106">ธุรกรรมเหล่านี้รวมถึงธุรกรรมหนี้สินสัญญาเช่าและธุรกรรมค่าใช้จ่ายในการจัดการสินทรัพย์ที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="e065d-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="e065d-107">มูลค่าการถือครองของหนี้สินและสิทธิ์การใช้สินทรัพย์ที่ใช้จะถูกใช้ในรายงานหลายฉบับ</span><span class="sxs-lookup"><span data-stu-id="e065d-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="e065d-108">นอกจากนี้ยังใช้ในการคำนวณมูลค่าการปรับปรุงด้วย</span><span class="sxs-lookup"><span data-stu-id="e065d-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="e065d-109">ธุรกรรมหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="e065d-109">Liability transactions</span></span>

<span data-ttu-id="e065d-110">ถ้าต้องการดูธุรกรรมหนี้สินสัญญาเช่า ให้เลือกสัญญาเช่าในหน้า **สรุปสัญญาเช่า** แล้วเลือก **สมุดบัญชี** ที่จะเปิดสมุดบัญชีที่แนบกับเรกคอร์ดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="e065d-111">หลังจากที่มีการลงรายการบัญชีการรับรู้เริ่มต้น ใบแจ้งหนี้ หรือสมุดรายวันดอกเบี้ยมีการลงรายการบัญชีแล้ว ให้เลือก **ธุรกรรมหนี้สิน**</span><span class="sxs-lookup"><span data-stu-id="e065d-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="e065d-112">หน้า **ธุรกรรมหนี้สิน** แสดงธุรกรรมที่เพิ่มหรือลดหนี้สินสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="e065d-113">ยอดเงินค่าลบในหน้านี้แสดงถึงธุรกรรมเครดิตในแอปพลิเคชันมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="e065d-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="e065d-114">ดอกเบี้ยค้างรับจะแสดงเป็นค่าลบและเพิ่มหนี้สินสัญญาเช่ารวม</span><span class="sxs-lookup"><span data-stu-id="e065d-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="e065d-115">การปรับปรุงสัญญาเช่าใด ๆ จะแสดงเป็นค่าบวกหรือค่าลบ ทั้งนี้ขึ้นอยู่กับลักษณะและผลกระทบของสมุดบัญชีสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="e065d-116">ยอดดุลรวมสุทธิปัจจุบันของหนี้สินสัญญาเช่าสำหรับสัญญาเช่าที่เลือกจะแสดงที่ด้านล่างซ้ายของหน้า</span><span class="sxs-lookup"><span data-stu-id="e065d-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="e065d-117">ธุรกรรมสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e065d-117">Asset transactions</span></span>

<span data-ttu-id="e065d-118">ถ้าต้องการดูธุรกรรมสินทรัพย์สัญญาเช่า ให้เลือกสัญญาเช่าในหน้า **สรุปสัญญาเช่า** แล้วเลือก **สมุดบัญชี** ที่จะเปิดสมุดบัญชีสัญญาเช่าที่แนบกับเรกคอร์ดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="e065d-119">จากนั้น เลือก **ธุรกรรมสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e065d-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="e065d-120">หน้า **ธุรกรรมสินทรัพย์** แสดงธุรกรรมที่เป็นส่วนหนึ่งของการเพิ่มหรือลดมูลค่าสินทรัพย์สัญญาเช่าและบัญชีค่าเสื่อมราคาสะสม</span><span class="sxs-lookup"><span data-stu-id="e065d-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="e065d-121">เดบิตจะแสดงเป็นค่าบวก และเครดิตจะแสดงเป็นค่าลบ ตามหน้า **ธุรกรรมหนี้สิน**</span><span class="sxs-lookup"><span data-stu-id="e065d-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="e065d-122">การรับรู้เริ่มต้นที่ลงรายการบัญชีแล้วและการคิดค่าเสื่อมราคาสะสมถัดไปจะแสดงอยู่ที่ด้านล่างซ้ายของหน้าเป็นยอดดุลสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e065d-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="e065d-123">ธุรกรรมค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="e065d-123">Expenses transactions</span></span>

<span data-ttu-id="e065d-124">ถ้าต้องการดูธุรกรรมค่าใช้จ่ายสัญญาเช่า ให้เลือกสัญญาเช่าในหน้า **สรุปสัญญาเช่า** แล้วเลือก **สมุดบัญชี** ที่จะเปิดสมุดบัญชีสัญญาเช่าที่แนบกับเรกคอร์ดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="e065d-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="e065d-125">จากนั้นเลือก **ธุรกรรมค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="e065d-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="e065d-126">หน้า **ธุรกรรมค่าใช้จ่าย** จะแสดงค่าใช้จ่ายทั้งหมดที่ได้ลงรายการบัญชีสำหรับสัญญาเช่า เช่น ค่าใช้จ่ายดอกเบี้ย ค่าเสื่อมราคา และค่าใช้จ่ายในการจัดการสินทรัพย์ใด ๆ</span><span class="sxs-lookup"><span data-stu-id="e065d-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
