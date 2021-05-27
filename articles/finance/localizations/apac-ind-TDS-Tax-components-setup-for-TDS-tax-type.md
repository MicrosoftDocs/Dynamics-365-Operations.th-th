---
title: ตั้งค่าส่วนประกอบภาษีสำหรับชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษีที่หักที่ต้นทาง (TDS) และยังอธิบายวิธีการกําหนดขีดจํากัดที่ใช้ในการคํานวณ TDS สำหรับส่วนประกอบ TDS แต่ละรายการด้วย
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023623"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="327e6-104">ตั้งค่าส่วนประกอบภาษีสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="327e6-105">หัวข้อนี้อธิบายวิธีการตั้งค่าส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="327e6-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="327e6-106">ส่วนประกอบ TDS ได้แก่ TDS, การเก็บเงินเพิ่ม, PE-Cess และ SHE Cess</span><span class="sxs-lookup"><span data-stu-id="327e6-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="327e6-107">หัวข้อนี้ยังอธิบายวิธีการกําหนดขีดจํากัดที่ใช้ในการคํานวณ TDS สำหรับส่วนประกอบ TDS แต่ละรายการด้วย</span><span class="sxs-lookup"><span data-stu-id="327e6-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="327e6-108">นอกจากนี้ คุณยังสามารถกําหนดขีดจำกัดข้อยกเว้นที่ใช้คํานวณ TDS สำหรับส่วนประกอบ TDS แต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="327e6-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="327e6-109">ให้ดำเนินการตามขั้นตอนเหล่านี้เพื่อตั้งค่าส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="327e6-110">ไปที่ **ภาษี \> การตั้งค่า \> ภาษีหัก ณ ที่จ่าย \> ส่วนประกอบภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="327e6-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="327e6-111">[![หน้าส่วนประกอบภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="327e6-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="327e6-112">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อตั้งค่าส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="327e6-113">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="327e6-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="327e6-114">ในฟิลด์ **ส่วนประกอบภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อสำหรับส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="327e6-115">ในฟิลด์ **กลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย** ให้เลือกกลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายของ TDS เพื่อแนบส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="327e6-116">บน FastTab **ทั่วไป** ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายของส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="327e6-117">ในบานหน้าต่างการดำเนินการ ให้เลือก **ขีดจำกัด** เพื่อเปิดหน้า **ขีดจำกัด** เพื่อให้คุณสามารถกําหนดขีดจำกัดที่ใช้ในการคํานวณ TDS สำหรับส่วนประกอบ TDS ได้</span><span class="sxs-lookup"><span data-stu-id="327e6-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="327e6-118">ใช้ฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** เพื่อกําหนดรอบระยะเวลาที่ใช้ขีดจำกัดนี้</span><span class="sxs-lookup"><span data-stu-id="327e6-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="327e6-119">บน FastTab **ทั่วไป** ในฟิลด์ **ขีดจำกัด** ให้ป้อนจำนวนเงินขีดจำกัดที่ใช้ในการคํานวณ TDS สำหรับส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="327e6-120">ภาษีจะถูกหักที่ต้นทางเฉพาะเมื่อยอดเงินในใบแจ้งหนี้สะสมเกินขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="327e6-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="327e6-121">ตัวอย่างเช่น ถ้ายอดเงินขีดจำกัดคือ 10,000 จะมีการคํานวณ TDS หลังจากยอดเงินใบแจ้งหนี้สะสมเกินกว่า 10,000 (กล่าวอีกอย่างคือ เมื่อยอดเงินเป็น 10,001 หรือมากกว่า)</span><span class="sxs-lookup"><span data-stu-id="327e6-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="327e6-122">ในฟิลด์ **ขีดจำกัดข้อยกเว้น** ให้ป้อนจำนวนเงินขีดจำกัดข้อยกเว้นที่ใช้ในการคํานวณ TDS สำหรับส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="327e6-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="327e6-123">ภาษีในบรรทัดใบแจ้งหนี้จะถูกหักที่ต้นทาง เฉพาะเมื่อยอดเงินในใบแจ้งหนี้สะสมเกินขีดจำกัดข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="327e6-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="327e6-124">ตัวอย่างเช่น ถ้ายอดเงินขีดจำกัดข้อยกเว้นคือ 5,000 จะมีการคํานวณ TDS บนบรรทัดใบแจ้งหนี้เฉพาะ ถ้ายอดเงินบรรทัดใบแจ้งหนี้เกิน 5,000 (กล่าวอีกอย่างคือ ถ้ายอดเงินเป็น 5,001 หรือมากกว่า)</span><span class="sxs-lookup"><span data-stu-id="327e6-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="327e6-125">[![หน้าขีดจำกัด](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="327e6-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="327e6-126">ยอดเงินขีดจากข้อยกเว้นต้องน้อยกว่าหรือเท่ากับยอดเงินขีดจำกัด</span><span class="sxs-lookup"><span data-stu-id="327e6-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="327e6-127">ภาษีจะถูกหักออกสำหรับธุรกรรม ถ้ายอดเงินธุรกรรมเกินขีดจำกัดข้อยกเว้น แม้ว่ายอดเงินในใบแจ้งหนี้สะสมจะไม่เกินขีดจำกัดที่ระบุไว้ในฟิลด์ **ขีดจำกัด**</span><span class="sxs-lookup"><span data-stu-id="327e6-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="327e6-128">ปิดหน้า **ขีดจำกัด** เพื่อกลับไปที่หน้า **ส่วนประกอบภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="327e6-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="327e6-129">ในบานหน้าต่างการดำเนินการ ให้เลือก **คัดลอก** เพื่อเปิดกล่องโต้ตอบ **คัดลอกส่วนประกอบภาษีหัก ณ ที่จ่าย** เพื่อให้คุณสามารถคัดลอกส่วนประกอบ TDS ที่ถูกตั้งค่าไว้ให้กับกลุ่มส่วนประกอบ TDS หนึ่งไปยังกลุ่มส่วนประกอบ TDS อื่น</span><span class="sxs-lookup"><span data-stu-id="327e6-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="327e6-130">ในฟิลด์ **จาก** ให้เลือกกลุ่มส่วนประกอบ TDS ที่จะคัดลอกส่วนประกอบ TDS มา</span><span class="sxs-lookup"><span data-stu-id="327e6-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="327e6-131">ในฟิลด์ **ไปยัง** ให้เลือกกลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายที่จะคัดลอกส่วนประกอบ TDS ไป</span><span class="sxs-lookup"><span data-stu-id="327e6-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="327e6-132">ไม่มีการคัดลอกส่วนประกอบ TDS ทั่วไปที่ถูกแนบกับกลุ่มส่วนประกอบ TDS ทั้งสองกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="327e6-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="327e6-133">เลือก **ตกลง** เพื่อคัดลอกและสร้างส่วนประกอบ TDS สำหรับกลุ่มส่วนประกอบ TDS อื่นๆ ในหน้าส่วนประกอบ **ภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="327e6-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="327e6-134">[![กล่องโต้ตอบคัดลอกส่วนประกอบภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="327e6-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="327e6-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="327e6-135">Close the page.</span></span>
