---
title: เรกคอร์ด TaxTrans ไม่ถูกสร้าง
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่สามารถช่วยเรกคอร์ด TaxTrans ไม่ถูกสร้าง
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947715"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="fd53c-103">เรกคอร์ด TaxTrans ไม่ถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="fd53c-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd53c-104">ถ้าคุณเลือก **ภาษีขายที่ลงรายการบัญชีแล้ว** ของธุรกรรม แต่หน้า **ภาษีขายที่ลงรายการบัญชี** ไม่แสดงรายการภาษีหรือไม่มีรายการภาษี แสดงว่าเรกคอร์ด **TaxTrans** อาจไม่ได้ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd53c-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="fd53c-105">[![หน้าภาษีขายที่ลงรายการบัญชีที่ไม่มีสินค้าในรายการ](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="fd53c-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="fd53c-106">เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="fd53c-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="fd53c-107">ตรวจสอบภาษีขายก่อนที่คุณจะลงรายการบัญชีธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="fd53c-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="fd53c-108">ก่อนที่คุณจะลงรายการบัญชีธุรกรรม บนหน้า **การลงรายการบัญชีใบแจ้งหนี้** ให้เลือก **ภาษีขาย** เพื่อตรวจสอบการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="fd53c-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="fd53c-109">[![ปุ่มภาษีขายบนหน้าการลงรายการบัญชีใบแจ้งหนี้](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="fd53c-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="fd53c-110">บนหน้า **ธุรกรรมภาษีขายชั่วคราว** ให้ตรวจทานผลลัพธ์ของการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="fd53c-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="fd53c-111">ถ้าไม่มีการคํานวณภาษี ให้ดูที่ [ภาษีไม่ได้คํานวณหรือยอดภาษีเป็นศูนย์](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md)</span><span class="sxs-lookup"><span data-stu-id="fd53c-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="fd53c-112">ค้นหาเรกคอร์ด TaxTrans ในภาษีขายที่ลงรายการบัญชีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fd53c-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="fd53c-113">ไปที่ **ภาษี** \> **การสอบถามและรายงาน** \> **การสอบถามภาษีขาย** > **ภาษีขายที่ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="fd53c-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="fd53c-114">ในหัวข้อคอลัมน์ **ใบสำคัญ** ให้เลือกสัญลักษณ์ตัวกรองข้อมูลเพื่อค้นหาเรกคอร์ด **TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="fd53c-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="fd53c-115">ถ้าคุณไม่พบเรกคอร์ดภาษีขายที่คุณค้นหา ให้ตรวจสอบวันที่</span><span class="sxs-lookup"><span data-stu-id="fd53c-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="fd53c-116">ถ้าวันที่แตกต่างจากวันที่ของหัวข้อสมุดรายวัน ให้สร้างคำขอบริการของ Microsoft เพื่อรับการสนับสนุนเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd53c-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="fd53c-117">[![หน้าภาษีขายที่ลงรายการบัญชี](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="fd53c-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="fd53c-118">ดีบักเพื่อตรวจสอบรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="fd53c-118">Debug to check details</span></span>

1. <span data-ttu-id="fd53c-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับดีบักและระบุว่า **TmpTaxWorkTrans** และ **TaxUncommitted** สร้างขึ้นอย่างถูกต้องหรือไม่ ดู [ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md)</span><span class="sxs-lookup"><span data-stu-id="fd53c-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="fd53c-120">ถ้า **TaxTmpWorkTrans** หรือ **TaxUncommitted** ถูกสร้างขึ้นอย่างถูกต้อง ให้เพิ่มจุดสั่งหยุดที่ **TaxPost::SaveAndPost()** และ **Tax::SaveAndPost** เพื่อดีบักเหตุผลที่ไม่มีการแทรก **TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="fd53c-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="fd53c-121">[![จุดสั่งหยุดที่เพิ่มในรหัส](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="fd53c-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="fd53c-122">[![ผลลัพธ์ของจุดสั่งหยุดที่เพิ่ม](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="fd53c-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="fd53c-123">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd53c-123">Determine whether customization exists</span></span>

<span data-ttu-id="fd53c-124">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="fd53c-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="fd53c-125">ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd53c-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
