---
title: สร้างบัญชีหลัก
description: 'คำแนะนำงานนี้ระบุการเพิ่มบัญชีหลักให้กับผังบัญชีที่มีอยู่ '
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, CompanyInfoList
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f1d1bfe358bbff1720e7d013c3bfeaba1a598ed0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216484"
---
# <a name="create-a-main-account"></a><span data-ttu-id="b2564-103">สร้างบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="b2564-103">Create a main account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2564-104">คำแนะนำงานนี้ระบุการเพิ่มบัญชีหลักให้กับผังบัญชีที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="b2564-104">This task guide steps through adding a main account to an existing chart of accounts.</span></span> <span data-ttu-id="b2564-105">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="b2564-105">This recording uses the USMF demo company.</span></span>  

1. <span data-ttu-id="b2564-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="b2564-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Accounts > Main accounts**.</span></span>
2. <span data-ttu-id="b2564-107">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b2564-107">Click **New**.</span></span>
3. <span data-ttu-id="b2564-108">ในฟิลด์ **บัญชีหลัก** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b2564-108">In the **Main account** field, type a value.</span></span>
4. <span data-ttu-id="b2564-109">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b2564-109">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b2564-110">ในฟิลด์ **ชนิดบัญชีหลัก** ให้เลือกชนิดที่แสดงยอดดุลบัญชีและสถานที่ในงบการเงินได้ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="b2564-110">In the **Main account type** field, select the type that best represents the accounts balance and location on financial statements.</span></span>
6. <span data-ttu-id="b2564-111">ในรายการ ให้เลือกประเภทบัญชีที่เป็นของบัญชีหลัก </span><span class="sxs-lookup"><span data-stu-id="b2564-111">In the list, select the account category the main account belongs to.</span></span> <span data-ttu-id="b2564-112">ประเภทลูกค้าองค์กรถูกใช้สำหรับรายงานทางการเงินเริ่มต้นและเนื้อหาแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="b2564-112">Account category is used for default financial reports and Power BI dashboard content.</span></span>  
7. <span data-ttu-id="b2564-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2564-113">In the list, click the link in the selected row.</span></span> <span data-ttu-id="b2564-114">เปลี่ยนยอดดุลเดบิตหรือเครดิตเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b2564-114">Change the default debit or credit balance.</span></span>  
8. <span data-ttu-id="b2564-115">ในฟิลด์ **สกุลเงินเริ่มต้น** ให้เลือกค่าจากรายการของสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="b2564-115">In the **Default currency** field, select a value from the list of currencies.</span></span>
9. <span data-ttu-id="b2564-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b2564-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b2564-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2564-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b2564-118">สลับการขยายของส่วน **การแทนที่นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="b2564-118">Toggle the expansion of the **Legal entity overrides** section.</span></span>
12. <span data-ttu-id="b2564-119">คลิก **เพิ่ม** เพื่อเลือกนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b2564-119">Click **Add** to select a legal entity.</span></span>
13. <span data-ttu-id="b2564-120">ในรายการ ให้เลือกนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b2564-120">In the list, select the Legal entity.</span></span>
14. <span data-ttu-id="b2564-121">คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="b2564-121">Click **Add**.</span></span>
15. <span data-ttu-id="b2564-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2564-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="b2564-123">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมาย **ระงับแล้ว**</span><span class="sxs-lookup"><span data-stu-id="b2564-123">Check or uncheck the **Suspended** checkbox.</span></span>
17. <span data-ttu-id="b2564-124">ขยายส่วน **การรายงานทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="b2564-124">Expand the **Financial reporting** section.</span></span>
18. <span data-ttu-id="b2564-125">ในฟิลด์ **ชนิดอัตราแลกเปลี่ยน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b2564-125">In the **Exchange rate type** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b2564-126">ในรายการ เลือก **ชนิดอัตราแลกเปลี่ยนสำหรับบัญชี**</span><span class="sxs-lookup"><span data-stu-id="b2564-126">In the list, select the **Exchange rate type for the account**.</span></span>
20. <span data-ttu-id="b2564-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b2564-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="b2564-128">ในฟิลด์ **ชนิดการแปลงสกุลเงิน** ให้เลือกวิธีสำหรับการคำนวณอัตราแลกเปลี่ยนสำหรับบัญชี</span><span class="sxs-lookup"><span data-stu-id="b2564-128">In the **Currency translation type** field, select the method for calculating exchange rates for the account.</span></span>
22. <span data-ttu-id="b2564-129">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b2564-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]