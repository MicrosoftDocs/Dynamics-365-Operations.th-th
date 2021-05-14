---
title: ตั้งค่ารอบระยะเวลาการชำระภาษีขาย
description: หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระภาษีขายใน Dynamics 365 Finance
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944788"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="94942-103">ตั้งค่ารอบระยะเวลาการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="94942-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94942-104">หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="94942-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="94942-105">รอบระยะเวลาการจ่ายภาษีขาย ประกอบด้วยข้อมูลเกี่ยวกับช่วงรอบระยะเวลาสำหรับที่ภาษีขายจำเป็นต้องถูกรายงานและชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="94942-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="94942-106">สามารถดำเนินการกระบวนการชำระเงินได้สำหรับรอบระยะเวลาการชำระเงินสำหรับช่วงวันที่เฉพาะ </span><span class="sxs-lookup"><span data-stu-id="94942-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="94942-107">รหัสภาษีทั้งหมดที่เชื่อมโยงกับรอบระยะเวลาการจ่ายเงินจะถูกตั้งค่า </span><span class="sxs-lookup"><span data-stu-id="94942-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="94942-108">ภาระภาษีจะถูกลงรายการบัญชีของผู้จัดจำหน่ายหรือบัญชีแยกประเภททั่วไปอย่างใดอย่างหนึ่ง ขึ้นอยู่กับการตั้งค่าของหน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้อง </span><span class="sxs-lookup"><span data-stu-id="94942-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="94942-109">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="94942-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="94942-110">ในบานหน้าต่างนำทางให้ ไปที่ **โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีขาย > รอบระยะเวลาการชำระภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="94942-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="94942-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="94942-111">Select **New**.</span></span>
3. <span data-ttu-id="94942-112">ในฟิลด์ **ระยะเวลาการชำระเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="94942-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="94942-113">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="94942-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="94942-114">ในฟิลด์ **หน่วยงานจัดเก็บภาษี** ให้เลือกหน่วยงานจัดเก็บภาษีขายที่ได้รับรายงานและการชำระเงินที่สร้างขึ้นสำหรับรอบระยะเวลาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="94942-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="94942-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="94942-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="94942-116">ในฟิลด์ **เงื่อนไขการชำระเงิน** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="94942-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="94942-117">หน่วยงานจัดเก็บภาษีขายที่เกี่ยวข้องสามารถถูกตั้งค่าให้เป็นผู้จัดจำหน่ายและการชำระภาษีขายจะสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง </span><span class="sxs-lookup"><span data-stu-id="94942-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="94942-118">เงื่อนไขการชำระเงินจะกำหนดวันครบกำหนดชำระสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายคงค้าง</span><span class="sxs-lookup"><span data-stu-id="94942-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="94942-119">เลือกชนิดสำหรับช่วงรอบระยะเวลาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="94942-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="94942-120">ป้อนหมายเลขของหน่วยช่วงรอบระยะเวลาต่อรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="94942-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="94942-121">ตัวอย่างเช่น หนึ่งไตรมาสมี 3 เดือน</span><span class="sxs-lookup"><span data-stu-id="94942-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="94942-122">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ใช้การประมวลผลชุดงานสำหรับการชำระภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="94942-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="94942-123">กระบวนการชำระสำหรับรอบระยะเวลาการชำระสามารถประมวลผลเป็นชุดงานในเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="94942-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="94942-124">ซึ่งเหมาะสำหรับธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="94942-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="94942-125">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี**</span><span class="sxs-lookup"><span data-stu-id="94942-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="94942-126">โดยค่าเริ่มต้น ระบบจะสร้างธุรกรรมออฟเซ็ตภาษีในระหว่างกระบวนการชำระเงิน ซึ่งทำให้เกิดปัญหาประสิทธิภาพการทำงาน ถ้ามีธุรกรรมภาษีจำนวนมากภายในช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="94942-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="94942-127">เลือกกล่องกาเครื่องหมายนี้เพื่อป้องกันไม่ให้สร้างธุรกรรมออฟเซ็ตภาษี</span><span class="sxs-lookup"><span data-stu-id="94942-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="94942-128">ขยายแท็บ **ช่วงรอบระยะเวลา**</span><span class="sxs-lookup"><span data-stu-id="94942-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="94942-129">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="94942-129">Select **Add**.</span></span>
14. <span data-ttu-id="94942-130">ในฟิลด์ **วันที่เริ่มต้น** ในแถวใหม่ ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="94942-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="94942-131">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="94942-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="94942-132">เลือก **ช่วงรอบระยะเวลาใหม่**</span><span class="sxs-lookup"><span data-stu-id="94942-132">Select **New period interval**.</span></span> <span data-ttu-id="94942-133">เมื่อมีการป้อนรอบระยะเวลาแรก รอบระยะเวลาใหม่จะถูกสร้างโดยอัตโนมัติ </span><span class="sxs-lookup"><span data-stu-id="94942-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="94942-134">คุณสามารถกลับมาและเพิ่มช่วงรอบระยะเวลาใหม่ตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="94942-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="94942-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="94942-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
