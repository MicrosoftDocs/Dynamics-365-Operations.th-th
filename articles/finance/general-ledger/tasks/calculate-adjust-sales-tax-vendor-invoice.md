---
title: คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่ายใน Dynamics 365 Finance
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
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139978"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="042c0-103">คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="042c0-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="042c0-104">หัวข้อนี้อธิบายวิธีการปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="042c0-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="042c0-105">ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="042c0-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="042c0-106">งานนี้ใช้บริษัทสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="042c0-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="042c0-107">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="042c0-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="042c0-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="042c0-108">Select **New**.</span></span>
3. <span data-ttu-id="042c0-109">ในฟิลด์ **ชื่อ** ของแถวใหม่ ให้เลือกตัวเลือกในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="042c0-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="042c0-110">ในบานหน้าต่างการดำเนินการ เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="042c0-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="042c0-111">ในฟิลด์ **บัญชี** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="042c0-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="042c0-112">ในฟิลด์ **ใบแจ้งหนี้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="042c0-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="042c0-113">ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="042c0-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="042c0-114">ในฟิลด์ **บัญชีตรงข้าม** ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="042c0-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="042c0-115">เลือก **ภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="042c0-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="042c0-116">ในฟิลด์ **ยอดภาษีขายจริงรวม** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="042c0-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="042c0-117">บนแท็บ **การปรับปรุง** สามารถปรับปรุงยอดภาษีขายได้สำหรับรหัสภาษีขายแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="042c0-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="042c0-118">เลือก **รีเซ็ตยอดจริงจากยอดที่คำนวณ**</span><span class="sxs-lookup"><span data-stu-id="042c0-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="042c0-119">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="042c0-119">Select **OK**.</span></span>
14. <span data-ttu-id="042c0-120">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="042c0-120">Select **Save**.</span></span>

