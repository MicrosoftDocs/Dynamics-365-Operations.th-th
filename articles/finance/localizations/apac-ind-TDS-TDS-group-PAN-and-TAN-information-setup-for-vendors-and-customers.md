---
title: ตั้งค่าข้อมูลกลุ่ม TDS, PAN และ TAN สำหรับผู้จัดจำหน่ายและลูกค้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลเกี่ยวกับกลุ่มภาษีที่หักที่ต้นทาง (TDS) หมายเลขบัญชีถาวร (PAN) และหมายเลขบัญชีภาษี (TAN) ของผู้จัดจำหน่ายและลูกค้า
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023629"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="b726c-103">การตั้งค่าข้อมูลกลุ่ม TDS, PAN และ TAN สำหรับผู้จัดจำหน่ายและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b726c-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b726c-104">หัวข้อนี้อธิบายวิธีการตั้งค่าข้อมูลเกี่ยวกับกลุ่มภาษีที่หักที่ต้นทาง (TDS) หมายเลขบัญชีถาวร (PAN) และหมายเลขบัญชีภาษี (TAN) ของผู้จัดจำหน่ายและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b726c-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="b726c-105">ไปที่ **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด** หรือ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b726c-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="b726c-106">[![หน้าผู้จัดจำหน่ายทั้งหมด](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="b726c-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="b726c-107">ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างผู้จัดจำหน่ายหรือลูกค้า และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="b726c-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="b726c-108">หรือเลือกผู้จัดจำหน่ายหรือลูกค้าที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b726c-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="b726c-109">บน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในส่วน **ภาษีหัก ณ ที่จ่าย** ให้ตั้งค่าตัวเลือก **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่** เพื่อคํานวณภาษีหัก ณ ที่จ่าย, TDS หรือภาษีที่เรียกเก็บที่ต้นทาง (TCS) สำหรับผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b726c-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="b726c-110">TDS สำหรับใบแจ้งหนี้การซื้อจะถูกคํานวณตามกลุ่ม TDS เริ่มต้นที่กําหนดไว้สำหรับผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b726c-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="b726c-111">ในฟิลด์ **กลุ่ม TDS** ให้เลือกกลุ่ม TDS เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b726c-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b726c-112">เมื่อคุณเลือกกลุ่ม TDS ในฟิลด์ **กลุ่ม TCS** **กลุ่มภาษีหัก ณ ที่จ่าย** และ **กลุ่ม TDS** จะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="b726c-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="b726c-113">บน FastTab **ข้อมูลภาษี** ในส่วน **ข้อมูล PAN** ในฟิลด์ **สถานะ** ให้เลือกสถานะของหมายเลขบัญชีถาวรสำหรับผู้จัดจำหน่ายหรือลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b726c-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="b726c-114">**ไม่พร้อมใช้งาน** – ผู้จัดจำหน่ายหรือลูกค้าไม่มี PAN</span><span class="sxs-lookup"><span data-stu-id="b726c-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="b726c-115">**ได้รับแล้ว** – ผู้จัดจำหน่ายหรือลูกค้ามี PAN</span><span class="sxs-lookup"><span data-stu-id="b726c-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="b726c-116">**นำไปใช้แล้ว** – ผู้จัดจำหน่ายหรือลูกค้าได้นำไปใช้แล้วสำหรับ PAN</span><span class="sxs-lookup"><span data-stu-id="b726c-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="b726c-117">**ไม่ถูกต้อง** – ผู้จัดจำหน่ายหรือลูกค้ามี PAN แต่ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b726c-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="b726c-118">ถ้าคุณเลือก **ได้รับแล้ว** ในฟิลด์ **สถานะ** เพื่อบ่งชี้ว่าผู้จัดจำหน่ายหรือลูกค้ามี PAN ให้ป้อน PAN ในฟิลด์ **หมายเลข**</span><span class="sxs-lookup"><span data-stu-id="b726c-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="b726c-119">PAN ต้องประกอบด้วยอักขระตัวอักษรห้าอักขระ ตามด้วยอักขระตัวเลขสี่อักขระ แล้วจากนั้น อักขระตัวอักษรหนึ่งอักขระ</span><span class="sxs-lookup"><span data-stu-id="b726c-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="b726c-120">นี่คือตัวอย่าง: **ABCDE1260A**</span><span class="sxs-lookup"><span data-stu-id="b726c-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="b726c-121">ถ้าคุณเลือก **นำไปใช้แล้ว** ในฟิลด์ **สถานะ** เพื่อบ่งชี้ว่าผู้จัดจำหน่ายหรือลูกค้าได้นำไปใช้แล้วสำหรับ PAN ให้ป้อนหมายเลขอ้างอิงในฟิลด์ **หมายเลขอ้างอิง**</span><span class="sxs-lookup"><span data-stu-id="b726c-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="b726c-122">ในฟิลด์ **ลักษณะของผู้ถูกประเมิน** เลือกประเภทลักษณะของผู้ถูกประเมินที่ผู้จัดจำหน่ายหรือลูกค้าเป็นสมาชิกอยู่:</span><span class="sxs-lookup"><span data-stu-id="b726c-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="b726c-123">บริษัท</span><span class="sxs-lookup"><span data-stu-id="b726c-123">Company</span></span>
    - <span data-ttu-id="b726c-124">HUF</span><span class="sxs-lookup"><span data-stu-id="b726c-124">HUF</span></span>
    - <span data-ttu-id="b726c-125">ยืนยันยอด</span><span class="sxs-lookup"><span data-stu-id="b726c-125">Firm</span></span>
    - <span data-ttu-id="b726c-126">บุคคล</span><span class="sxs-lookup"><span data-stu-id="b726c-126">Individual</span></span>
    - <span data-ttu-id="b726c-127">AOP</span><span class="sxs-lookup"><span data-stu-id="b726c-127">AOP</span></span>
    - <span data-ttu-id="b726c-128">BOI</span><span class="sxs-lookup"><span data-stu-id="b726c-128">BOI</span></span>
    - <span data-ttu-id="b726c-129">หน่วยงานท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="b726c-129">Local authority</span></span>
    - <span data-ttu-id="b726c-130">อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="b726c-130">Others</span></span>

    <span data-ttu-id="b726c-131">[![FastTab ข้อมูลภาษี](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="b726c-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="b726c-132">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **การลงทะเบียน** ให้เลือก **รหัสการลงทะเบียน** เพื่อเปิดหน้า **จัดการที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="b726c-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="b726c-133">บนหน้า **จัดการที่อยู่** บน FastTab **ข้อมูลภาษี** ให้เลือก **เพิ่ม** หรือ **แก้ไข** เพื่อเปิดหน้า **จัดการข้อมูลภาษี** ที่ซึ่งคุณสามารถรักษารายการทะเบียนภาษีได้</span><span class="sxs-lookup"><span data-stu-id="b726c-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="b726c-134">บนหน้า **จัดการข้อมูลภาษี** บน FastTab **ภาษีหัก ณ ที่จ่าย** ในฟิลด์ **หมายเลขบัญชีภาษี (TAN)** ให้ป้อน TAN</span><span class="sxs-lookup"><span data-stu-id="b726c-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="b726c-135">TAN ต้องประกอบด้วยอักขระตัวอักษรสี่อักขระ ตามด้วยอักขระตัวเลขห้าอักขระ แล้วจากนั้น อักขระตัวอักษรหนึ่งอักขระ</span><span class="sxs-lookup"><span data-stu-id="b726c-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="b726c-136">นี่คือตัวอย่าง: **AFGH54821T**</span><span class="sxs-lookup"><span data-stu-id="b726c-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="b726c-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b726c-137">Close the page.</span></span>
