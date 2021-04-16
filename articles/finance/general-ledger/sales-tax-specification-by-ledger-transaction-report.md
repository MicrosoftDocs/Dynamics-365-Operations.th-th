---
title: ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามรายงานธุรกรรมบัญชีแยกประเภท
description: หัวข้อนี้จะอธิบายวิธีการใช้ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามธุรกรรมบัญชีแยกประเภทเพื่อดูและพิมพ์ข้อมูลเกี่ยวกับธุรกรรมบัญชีแยกประเภทที่มีการคำนวณภาษีขาย
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815271"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="06e49-103">ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามรายงานธุรกรรมบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="06e49-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="06e49-104">หัวข้อนี้จะอธิบายวิธีการใช้ข้อมูลรายงานจำเพาะเกี่ยวกับ **ภาษีขายโดยเรียงตามธุรกรรมบัญชีแยกประเภท** เพื่อดูและพิมพ์ข้อมูลเกี่ยวกับธุรกรรมบัญชีแยกประเภทที่มีการคำนวณภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="06e49-105">บัญชีภาษี เปรียบเทียบกับ บัญชีที่ไม่ใช่ภาษี</span><span class="sxs-lookup"><span data-stu-id="06e49-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="06e49-106">รายงาน **ข้อมูลจำเพาะภาษีขายของธุรกรรมบัญชีแยกประเภท** จะแสดงธุรกรรมภาษีสำหรับทั้งบัญชีภาษีและบัญชีที่ไม่ใช่ภาษี</span><span class="sxs-lookup"><span data-stu-id="06e49-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="06e49-107">บัญชีเหล่านี้ถูกจัดประเภทในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="06e49-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="06e49-108">**บัญชีภาษี** – บัญชีจะถือว่าเป็นบัญชีภาษีก็ต่อเมื่อมีการลงรายการบัญชีธุรกรรมภาษี และบัญชีหลักในรายการสมุดประจำวันของ **ภาษีขาย** เป็นบัญชีภาษี เช่น บัญชีเจ้าหนี้ภาษีขาย หรือบัญชีลูกหนี้ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="06e49-109">**บัญชีที่ไม่ใช่ภาษี** – บัญชีจะถือว่าเป็นบัญชีที่ไม่ใช่ภาษีก็ต่อเมือมีการลงรายการธุรกรรมภาษี และบัญชีหลักของธุรกรรมเดิมเป็นบัญชีที่ไม่ใช่ภาษี เช่น บัญชีรายได้ หรือ บัญชีรายจ่าย</span><span class="sxs-lookup"><span data-stu-id="06e49-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="06e49-110">สำหรับบัญชีภาษี คอลัมน์ **จุดเริ่มต้น**, **ลูกหนี้ภาษีขาย** และ **เจ้าหนี้ภาษีขาย** แสดงค่าเป็น **0** (ศูนย์).</span><span class="sxs-lookup"><span data-stu-id="06e49-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="06e49-111">สำหรับบัญชีที่ไม่ใช่ภาษี คอลัมน์เหล่านั้นจะแสดงยอดปกติ</span><span class="sxs-lookup"><span data-stu-id="06e49-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="06e49-112">การกรองข้อมูลที่อยู่ในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06e49-112">Filtering the data on the report</span></span>

<span data-ttu-id="06e49-113">เมื่อคุณสร้างรายงานนี้ ฟิลด์เริ่มต้นต่อไปนี้จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="06e49-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="06e49-114">คุณสามารถใช้ฟิลด์เหล่านี้เพื่อกรองข้อมูลที่จะแสดงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06e49-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="06e49-115">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="06e49-115">Field</span></span>                      | <span data-ttu-id="06e49-116">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="06e49-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="06e49-117">วัน เดือน</span><span class="sxs-lookup"><span data-stu-id="06e49-117">Date</span></span>                       | <span data-ttu-id="06e49-118">ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงวันที่สำหรับธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="06e49-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="06e49-119">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="06e49-119">Main account</span></span>               | <span data-ttu-id="06e49-120">ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงของบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="06e49-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="06e49-121">รหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-121">Sales tax code</span></span>             | <span data-ttu-id="06e49-122">ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงของรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="06e49-123">การจัดกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="06e49-123">Grouping</span></span>                   | <span data-ttu-id="06e49-124">เลือกว่าจะให้จัดกลุ่มรายงานตามบัญชีแยกประเภท หรือตามรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="06e49-125">ผลรวมย่อยตามรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="06e49-126">กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อแสดงผลรวมย่อยตามรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="06e49-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="06e49-127">เฉพาะผลรวม</span><span class="sxs-lookup"><span data-stu-id="06e49-127">Totals only</span></span>                | <span data-ttu-id="06e49-128">กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อแสดงเฉพาะผลรวม</span><span class="sxs-lookup"><span data-stu-id="06e49-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="06e49-129">บัญชีหลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="06e49-129">Main accounts only</span></span>         | <span data-ttu-id="06e49-130">กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อรวมเฉพาะบัญชีหลักบนรายงาน</span><span class="sxs-lookup"><span data-stu-id="06e49-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="06e49-131">แสดงเฉพาะบัญชีที่ไม่ใช่ภาษีในรายงาน</span><span class="sxs-lookup"><span data-stu-id="06e49-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="06e49-132">เมื่อต้องการแสดงเฉพาะบัญชีที่ไม่ใช่ภาษีในรายงาน ให้ตั้งค่าเงื่อนไขตัวกรองข้อมูล เช่น เครื่องหมายดอกจัน (\*) ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06e49-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![รายงานที่แสดงบัญชีที่ไม่ใช่ภาษี](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]