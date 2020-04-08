---
title: ดูรายการสมุดรายวันหรือธุรกรรม
description: กระบวนงานนี้แสดงวิธีการใช้การสอบถามเกี่ยวกับธุรกรรมใบสำคัญที่จะค้นหารายการสมุดรายวันหรือธุรกรรม
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f463b7764288918609cba364acf342eed28ad929
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144662"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="1a544-103">ดูรายการสมุดรายวันหรือธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1a544-103">View journal entries or transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a544-104">กระบวนงานนี้แสดงวิธีการใช้การสอบถามเกี่ยวกับธุรกรรมใบสำคัญที่จะค้นหารายการสมุดรายวันหรือธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1a544-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="1a544-105">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > การสอบถามและรายงาน > ธุรกรรมใบสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="1a544-105">Go to **Navigation pane > Modules > General ledger > Inquiries and reports > Voucher transactions**.</span></span>
2. <span data-ttu-id="1a544-106">เลือกฟิลด์ที่คุณต้องการกำหนดเกณฑ์ตัวกรองให้</span><span class="sxs-lookup"><span data-stu-id="1a544-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="1a544-107">ป้อนเกณฑ์ตัวกรองสำหรับฟิลด์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a544-107">Enter your filter critieria for the selected field.</span></span> <span data-ttu-id="1a544-108">คุณสามารถกรองค่าหรือช่วงเดียวได้ </span><span class="sxs-lookup"><span data-stu-id="1a544-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="1a544-109">ในขณะที่กำหนดช่วง ให้ตรวจสอบว่าการใช้ไวยากรณ์ถูกต้องหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="1a544-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="1a544-110">ค่าควรถูกคั่นด้วยเครื่องหมายมหัพภาคสองตัว (..)</span><span class="sxs-lookup"><span data-stu-id="1a544-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="1a544-111">คลิกแท็บ **รวม** เพื่อเพิ่มตารางเพิ่มเติมจากที่จะกรอง</span><span class="sxs-lookup"><span data-stu-id="1a544-111">Click the **Joins** tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="1a544-112">ในแผนภูมิ เลือก **ตาราง/รายการสมุดรายวันทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="1a544-112">In the tree, select **Tables/General journal entry**.</span></span>
6. <span data-ttu-id="1a544-113">คลิก **เพิ่มการรวมตาราง**</span><span class="sxs-lookup"><span data-stu-id="1a544-113">Click **Add table join**.</span></span>
7. <span data-ttu-id="1a544-114">คลิก **ยกเลิก** ถ้าคุณตัดสินใจที่จะไม่เพิ่มตารางเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1a544-114">Click **Cancel** if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="1a544-115">คลิกแท็บ **ช่วง**</span><span class="sxs-lookup"><span data-stu-id="1a544-115">Click the **Range** tab.</span></span>
9. <span data-ttu-id="1a544-116">คลิก **ตกลง** เพื่อรันแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="1a544-116">Click **OK** to run the query.</span></span>
10. <span data-ttu-id="1a544-117">ในบานหน้าต่างการดำเนินการ คลิก **จุดเริ่มต้นของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="1a544-117">On the Action pane, click **Transaction origin**.</span></span> <span data-ttu-id="1a544-118">สามารถใช้ปุ่มต่างๆ เกี่ยวกับกริดเพื่อศึกษาข้อมูลเพิ่มเติมเกี่ยวกับเรกคอร์ดที่เลือกของใบสำคัญ </span><span class="sxs-lookup"><span data-stu-id="1a544-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="1a544-119">ปุ่มบางปุ่มอาจไม่พร้อมใช้งาน ทั้งนี้ขึ้นอยู่กับชนิดของธุรกรรมและลักษณะของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="1a544-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>
11. <span data-ttu-id="1a544-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a544-120">Close the page.</span></span>
12. <span data-ttu-id="1a544-121">ในบานหน้าต่างการดำเนินการ คลิก **เอกสารต้นฉบับ**</span><span class="sxs-lookup"><span data-stu-id="1a544-121">On the Action pane, Click **Original document**.</span></span>
13. <span data-ttu-id="1a544-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a544-122">Close the page.</span></span>

