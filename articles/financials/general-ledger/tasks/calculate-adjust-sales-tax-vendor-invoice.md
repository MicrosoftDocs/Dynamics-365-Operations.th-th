---
title: คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 for Finance and Operations
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862625"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="beb1a-103">คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="beb1a-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="beb1a-104">หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="beb1a-104">This topic explains how to adjust sales tax on a vendor invoice in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="beb1a-105">ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="beb1a-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="beb1a-106">งานนี้ใช้บริษัทสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="beb1a-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="beb1a-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="beb1a-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="beb1a-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="beb1a-108">Select **New**.</span></span>
3. <span data-ttu-id="beb1a-109">ในฟิลด์ **ชื่อ** ของแถวใหม่ ให้เลือกตัวเลือกในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="beb1a-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="beb1a-110">ในบานหน้าต่างการดำเนินการ เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="beb1a-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="beb1a-111">ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beb1a-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="beb1a-112">ในฟิลด์ **ใบแจ้งหนี้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="beb1a-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="beb1a-113">ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="beb1a-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="beb1a-114">ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="beb1a-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="beb1a-115">เลือก **ภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="beb1a-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="beb1a-116">ในฟิลด์ **ยอดภาษีขายจริงรวม** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="beb1a-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="beb1a-117">บนแท็บ **การปรับปรุง** สามารถปรับปรุงยอดภาษีขายได้สำหรับรหัสภาษีขายแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="beb1a-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="beb1a-118">เลือก **รีเซ็ตยอดจริงจากยอดที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="beb1a-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="beb1a-119">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="beb1a-119">Select **OK**.</span></span>
14. <span data-ttu-id="beb1a-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="beb1a-120">Select **Save**.</span></span>

