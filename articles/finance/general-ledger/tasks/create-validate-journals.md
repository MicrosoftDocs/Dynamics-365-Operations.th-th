---
title: สร้างตรวจสอบความถูกต้องของสมุดรายวัน
description: 'คำแนะนำงานนี้สร้างและตรวจสอบสมุดรายวันและรายการสมุดรายวัน '
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 212227afb21ac1a20d29c33b40f6c44561da14fe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144364"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="fa89f-103">สร้างตรวจสอบความถูกต้องของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="fa89f-103">Create and validate journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa89f-104">คำแนะนำงานนี้สร้างและตรวจสอบสมุดรายวันและรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="fa89f-104">This task guide creates and validates journals and journal lines.</span></span> <span data-ttu-id="fa89f-105">งานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="fa89f-105">This tasks uses the USMF demo company.</span></span>  



1. <span data-ttu-id="fa89f-106">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="fa89f-106">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="fa89f-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fa89f-107">Click New.</span></span>
3. <span data-ttu-id="fa89f-108">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fa89f-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fa89f-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fa89f-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fa89f-110">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="fa89f-110">Click Lines.</span></span>
6. <span data-ttu-id="fa89f-111">ในฟิลด์บัญชี ให้ป้อนบัญชีที่เหมาะสมตามชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="fa89f-111">In the Account field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="fa89f-112">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fa89f-112">In the Description field, type a value.</span></span>
8. <span data-ttu-id="fa89f-113">ป้อนยอดเงินสำหรับบัญชีเดบิตหรือเครดิต </span><span class="sxs-lookup"><span data-stu-id="fa89f-113">Enter an amount for the Account in either Debit or Credit.</span></span> <span data-ttu-id="fa89f-114">คำแนะนำของงานนี้จะสันนิษฐานว่าเป็นยอดเงินเดบิต</span><span class="sxs-lookup"><span data-stu-id="fa89f-114">This task guide is assuming a debit amount.</span></span>
9. <span data-ttu-id="fa89f-115">ในฟิลด์บัญชีตรงข้าม ให้ป้อนบัญชีที่เหมาะสมตามชนิดบัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="fa89f-115">In the Offset account field enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="fa89f-116">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fa89f-116">Click Validate.</span></span>
11. <span data-ttu-id="fa89f-117">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fa89f-117">Click Validate.</span></span>
12. <span data-ttu-id="fa89f-118">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="fa89f-118">Click Post.</span></span>
13. <span data-ttu-id="fa89f-119">คลิกใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="fa89f-119">Click Voucher.</span></span>

