---
title: ตั้งค่ารหัสการรายงานภาษีขาย
description: รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l
author: twheeloc
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e040bac6ef9e950e8d7f97e3c136636acf1fe43
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813542"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="54345-103">ตั้งค่ารหัสการรายงานภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="54345-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54345-104">รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l</span><span class="sxs-lookup"><span data-stu-id="54345-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="54345-105">ใช้ในโครงร่างรายงานเฉพาะประเทศ</span><span class="sxs-lookup"><span data-stu-id="54345-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="54345-106">ใช้ในรายงานการชำระภาษีขายโดยเรียงตามรหัสด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="54345-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="54345-107">รายงานดังกล่าวแสดงยอดภาษีขายสำหรับรอบระยะเวลาการจ่ายเงินสรุปสำหรับแต่ละรหัสการรายงาน</span><span class="sxs-lookup"><span data-stu-id="54345-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="54345-108">หลังจากที่คุณสร้างรหัสการรายงานภาษีขาย คุณสามารถอ้างอิงรหัสนี้กับแท็บด่วนการตั้งค่ารายงานในหน้ารหัสภาษีขาย ซึ่งคุณสามารถเข้าถึงจากหน้า **รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="54345-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="54345-109">บันทึกนี้ใช้บริษัทสาธิต DEMF </span><span class="sxs-lookup"><span data-stu-id="54345-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="54345-110">ใน **บานหน้าต่างนำทาง** ไปที่ **ภาษี > การตั้งค่า > ภาษีขาย > รหัสการรายงานภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="54345-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="54345-111">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="54345-111">Click **New**.</span></span>
3. <span data-ttu-id="54345-112">เลือกโครงร่างรายงานที่เป็นของรหัสการรายงาน</span><span class="sxs-lookup"><span data-stu-id="54345-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="54345-113">โครงร่างนี้จะใช้เพื่อกรองข้อมูลรหัสการรายงานที่พร้อมใช้งานสำหรับรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="54345-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="54345-114">แต่ละรหัสภาษีขายนั้นเป็นของรอบระยะเวลาการชำระซึ่งเป็นของหน่วยงานจัดเก็บภาษีขายซึ่งใช้โครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="54345-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="54345-115">ในฟิลด์ **รหัสการรายงาน** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="54345-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="54345-116">ในฟิลด์ **ข้อความในรายงาน** ให้ป้อนคำอธิบายที่จะแสดงในรายงาน</span><span class="sxs-lookup"><span data-stu-id="54345-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="54345-117">ในฟิลด์ **คำอธิบายย่อ** ให้ป้อนคำอธิบายสำหรับจุดประสงค์ภายใน</span><span class="sxs-lookup"><span data-stu-id="54345-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="54345-118">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="54345-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]