---
title: ตั้งค่ารหัสการรายงานภาษีขาย
description: รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916102"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="c1eda-103">ตั้งค่ารหัสการรายงานภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="c1eda-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1eda-104">รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l</span><span class="sxs-lookup"><span data-stu-id="c1eda-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="c1eda-105">รหัสนี้จะใช้โครงร่างรายงานเฉพาะประเทศและการชำระภาษีขายตามรหัสการรายงาน เพื่อพิมพ์ยอดเงินภาษีขายสำหรับรอบระยะเวลาการชำระเงินที่มีการสรุปสำหรับแต่ละรหัสการรายงาน </span><span class="sxs-lookup"><span data-stu-id="c1eda-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="c1eda-106">หลังจากที่คุณสร้างรหัสการรายงานภาษีขาย คุณสามารถอ้างอิงรหัสนี้กับแท็บด่วนการตั้งค่ารายงานในหน้ารหัสภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="c1eda-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="c1eda-107">บันทึกนี้ใช้บริษัทสาธิต DEMF </span><span class="sxs-lookup"><span data-stu-id="c1eda-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="c1eda-108">ใน **บานหน้าต่างนำทาง** ไปที่ **ภาษี > การตั้งค่า > ภาษีขาย > รหัสการรายงานภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="c1eda-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="c1eda-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c1eda-109">Click **New**.</span></span>
3. <span data-ttu-id="c1eda-110">เลือกโครงร่างรายงานที่เป็นของรหัสการรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1eda-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="c1eda-111">โครงร่างนี้จะใช้เพื่อกรองข้อมูลรหัสการรายงานที่พร้อมใช้งานสำหรับรหัสภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="c1eda-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="c1eda-112">แต่ละรหัสภาษีขายนั้นเป็นของรอบระยะเวลาการชำระซึ่งเป็นของหน่วยงานจัดเก็บภาษีขายซึ่งใช้โครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1eda-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="c1eda-113">ในฟิลด์ **รหัสการรายงาน** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="c1eda-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="c1eda-114">ในฟิลด์ **ข้อความในรายงาน** ให้ป้อนคำอธิบายที่จะแสดงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="c1eda-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="c1eda-115">ในฟิลด์ **คำอธิบายย่อ** ให้ป้อนคำอธิบายสำหรับจุดประสงค์ภายใน</span><span class="sxs-lookup"><span data-stu-id="c1eda-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="c1eda-116">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="c1eda-116">Click **Save**.</span></span>

