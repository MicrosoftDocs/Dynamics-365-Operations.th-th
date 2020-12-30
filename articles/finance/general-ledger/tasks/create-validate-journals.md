---
title: สร้างตรวจสอบความถูกต้องของสมุดรายวัน
description: ขั้นตอนนี้สร้างและตรวจสอบสมุดรายวันและรายการสมุดรายวัน
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
ms.openlocfilehash: 8ac70a6fd52a47e5edbdd21145a47c925256fa71
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646322"
---
# <a name="create-and-validate-journals"></a><span data-ttu-id="a6bec-103">สร้างตรวจสอบความถูกต้องของสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a6bec-103">Create and validate journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6bec-104">ขั้นตอนนี้สร้างและตรวจสอบสมุดรายวันและรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="a6bec-104">This procedure creates and validates journals and journal lines.</span></span> <span data-ttu-id="a6bec-105">คุณสามารถลองใช้กระบวนงานนี้ในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="a6bec-105">You can try this procedure using the USMF demo company.</span></span>  

1. <span data-ttu-id="a6bec-106">ไปที่ **บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="a6bec-106">Go to **General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="a6bec-107">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="a6bec-107">Click **New**.</span></span>
3. <span data-ttu-id="a6bec-108">ในฟิลด์ **ชื่อ** ให้คลิกปุ่มรายการแบบหล่นลงเพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="a6bec-108">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a6bec-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a6bec-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a6bec-110">คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="a6bec-110">Click **Lines**.</span></span>
6. <span data-ttu-id="a6bec-111">ในฟิลด์ **บัญชี** ให้ป้อนบัญชีที่เหมาะสมตามชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="a6bec-111">In the **Account** field enter an appropriate account based on the Account type.</span></span>
7. <span data-ttu-id="a6bec-112">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a6bec-112">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="a6bec-113">ป้อนยอดเงินสำหรับบัญชี **เดบิต** หรือ **เครดิต**</span><span class="sxs-lookup"><span data-stu-id="a6bec-113">Enter an amount for the account as either a **Debit** or **Credit**.</span></span> 
9. <span data-ttu-id="a6bec-114">ในฟิลด์ **บัญชีตรงข้าม** ให้ป้อนบัญชีที่เหมาะสมตามชนิดบัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="a6bec-114">In the **Offset account** field, enter an appropriate account based on the Offset account type.</span></span>
10. <span data-ttu-id="a6bec-115">คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a6bec-115">Click **Validate**.</span></span>
11. <span data-ttu-id="a6bec-116">คลิก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="a6bec-116">Click **Validate**.</span></span>
12. <span data-ttu-id="a6bec-117">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="a6bec-117">Click **Post**.</span></span>
13. <span data-ttu-id="a6bec-118">คลิก **ใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="a6bec-118">Click **Voucher**.</span></span>

