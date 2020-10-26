---
title: การตั้งค่าหน่วยงานจัดเก็บภาษี
description: 'หน่วยงานจัดเก็บภาษีขายเป็นองค์กรอิสระที่เก็บรวบรวมภาษีขายที่จะต้องถูกรายงานและชำระ '
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 63b1b023181e1ead16571102c524a61edfdabdca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976828"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="428e4-103">การตั้งค่าหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="428e4-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="428e4-104">หน่วยงานจัดเก็บภาษีขายเป็นองค์กรอิสระที่เก็บรวบรวมภาษีขายที่จะต้องถูกรายงานและชำระ </span><span class="sxs-lookup"><span data-stu-id="428e4-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="428e4-105">คุณสามารถชำระภาษีขายที่หน่วยงานโดยตรงหรือผ่านบัญชีผู้จัดจำหน่ายที่คุณสร้างขึ้นสำหรับหน่วยงานจัดเก็บภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="428e4-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="428e4-106">บริษัทจะสามารถใช้งานประจำในการชำระเงินโดยปกติของตนในการชำระเงินต่อหน่วยงานจัดเก็บภาษีขายได้ตามเวลา</span><span class="sxs-lookup"><span data-stu-id="428e4-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="428e4-107">หากไม่ได้ตั้งค่าหน่วยงานจัดเก็บภาษีเป็นผู้จัดจำหน่าย คุณต้องมีบุคคลเตรียมการชำระเงินด้วยตนเองแก่หน่วยงานจัดเก็บภาษีตามเวลาครบกำหนดที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="428e4-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="428e4-108">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="428e4-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="428e4-109">ไปที่ภาษี > ภาษีทางอ้อม > ภาษีขาย > หน่วยงานจัดเก็บภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="428e4-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="428e4-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="428e4-110">Click New.</span></span>
3. <span data-ttu-id="428e4-111">ในฟิลด์หน่วยงานจัดเก็บภาษี ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="428e4-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="428e4-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="428e4-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="428e4-113">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="428e4-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="428e4-114">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="428e4-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="428e4-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="428e4-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="428e4-116">เลือกโครงร่างรายงานสำหรับประเทศ/ภูมิภาคของคุณ ถ้ามี </span><span class="sxs-lookup"><span data-stu-id="428e4-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="428e4-117">ถ้าโครงร่างรายงานไม่สอดคล้องกับความต้องการของหน่วยงานจัดเก็บภาษีขาย ให้ใช้รูปแบบเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="428e4-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="428e4-118">ป้อนค่าในแบบฟอร์มการปัดเศษและฟิลด์การปัดเศษเพื่อระบุวิธีการชำระยอดเงินภาษีรวมว่าควรจะมีการปัดเศษอย่างไร </span><span class="sxs-lookup"><span data-stu-id="428e4-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="428e4-119">ผลต่างจากการปัดเศษใด ๆ จะถูกลงรายการบัญชีสำหรับธุรกรรมอัตโนมัติที่ตั้งค่าไว้ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="428e4-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="428e4-120">ในฟิลด์การปัดเศษ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="428e4-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="428e4-121">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="428e4-121">Click Save.</span></span>

