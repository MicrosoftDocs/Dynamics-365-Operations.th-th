---
title: คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย
description: ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545182"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="d86bc-103">คำนวณและปรับปรุงภาษีขายในใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="d86bc-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d86bc-104">ถ้าเอกสารต้นทางที่เป็นต้นฉบับแสดงยอดเงินภาษีที่แตกต่างกันจากการคำนวณ คุณสามารถปรับปรุงยอดเงินเหล่านั้นก่อนที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d86bc-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="d86bc-105">งานนี้ใช้บริษัทสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="d86bc-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="d86bc-106">ไปที่บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="d86bc-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="d86bc-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d86bc-107">Click New.</span></span>
3. <span data-ttu-id="d86bc-108">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d86bc-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d86bc-109">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d86bc-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d86bc-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d86bc-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d86bc-111">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="d86bc-111">Click Lines.</span></span>
7. <span data-ttu-id="d86bc-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d86bc-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d86bc-113">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d86bc-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="d86bc-114">ในฟิลด์ใบแจ้งหนี้ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d86bc-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="d86bc-115">ในฟิลด์เครดิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="d86bc-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="d86bc-116">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d86bc-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="d86bc-117">คลิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="d86bc-117">Click Sales tax.</span></span>
13. <span data-ttu-id="d86bc-118">ในฟิลด์ยอดภาษีขายจริงรวม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d86bc-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="d86bc-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d86bc-119">Click OK.</span></span>
15. <span data-ttu-id="d86bc-120">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="d86bc-120">Click Save.</span></span>
16. <span data-ttu-id="d86bc-121">คลิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="d86bc-121">Click Sales tax.</span></span>
17. <span data-ttu-id="d86bc-122">บนแท็บการปรับปรุง ยอดภาษีขายสามารถปรับปรุงได้แต่ละรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="d86bc-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="d86bc-123">คลิกรีเซ็ตยอดจริงจากยอดที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="d86bc-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="d86bc-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d86bc-124">Click OK.</span></span>
20. <span data-ttu-id="d86bc-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d86bc-125">Click Save.</span></span>

