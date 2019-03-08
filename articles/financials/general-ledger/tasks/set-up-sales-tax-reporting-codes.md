---
title: ตั้งค่ารหัสการรายงานภาษีขาย
description: รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "335680"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="3f4a1-103">ตั้งค่ารหัสการรายงานภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3f4a1-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f4a1-104">รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l</span><span class="sxs-lookup"><span data-stu-id="3f4a1-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="3f4a1-105">รหัสนี้จะใช้โครงร่างรายงานเฉพาะประเทศและการชำระภาษีขายตามรหัสการรายงาน เพื่อพิมพ์ยอดเงินภาษีขายสำหรับรอบระยะเวลาการชำระเงินที่มีการสรุปสำหรับแต่ละรหัสการรายงาน </span><span class="sxs-lookup"><span data-stu-id="3f4a1-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="3f4a1-106">หลังจากที่คุณสร้างรหัสการรายงานภาษีขาย คุณสามารถอ้างอิงรหัสนี้กับแท็บด่วนการตั้งค่ารายงานในหน้ารหัสภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="3f4a1-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="3f4a1-107">บันทึกนี้ใช้บริษัทสาธิต DEMF </span><span class="sxs-lookup"><span data-stu-id="3f4a1-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="3f4a1-108">ไปที่ ภาษี > การตั้งค่า > ภาษีขาย > รหัสการรายงานภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3f4a1-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="3f4a1-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3f4a1-109">Click New.</span></span>
3. <span data-ttu-id="3f4a1-110">เลือกโครงร่างรายงานที่เป็นของรหัสการรายงาน</span><span class="sxs-lookup"><span data-stu-id="3f4a1-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="3f4a1-111">โครงร่างนี้จะใช้เพื่อกรองข้อมูลรหัสการรายงานที่พร้อมใช้งานสำหรับรหัสภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="3f4a1-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="3f4a1-112">แต่ละรหัสภาษีขายนั้นเป็นของรอบระยะเวลาการชำระซึ่งเป็นของหน่วยงานจัดเก็บภาษีขายซึ่งใช้โครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="3f4a1-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="3f4a1-113">ป้อนหมายเลขฟิลด์ที่อ้างถึงฟิลด์ในรายงานภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3f4a1-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="3f4a1-114">ในฟิลด์ข้อความในรายงาน ให้ป้อนคำอธิบายที่จะแสดงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="3f4a1-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="3f4a1-115">ในฟิลด์คำอธิบายย่อ ให้ป้อนคำอธิบายสำหรับจุดประสงค์ภายใน</span><span class="sxs-lookup"><span data-stu-id="3f4a1-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="3f4a1-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3f4a1-116">Click Save.</span></span>

