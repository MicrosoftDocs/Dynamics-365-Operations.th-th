---
title: ตั้งค่าค่าธรรมเนียมการชำระเงินสำหรับการชำระเงินให้แก่หน่วยงานจัดเก็บ TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าค่าธรรมเนียมการชำระเงินที่เรียกเก็บจากหน่วยงานจัดเก็บภาษี ณ ที่จ่าย (TDS)
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023643"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="14da0-103">ตั้งค่าค่าธรรมเนียมการชำระเงินสำหรับการชำระเงินให้แก่หน่วยงานจัดเก็บ TDS</span><span class="sxs-lookup"><span data-stu-id="14da0-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14da0-104">หัวข้อนี้อธิบายวิธีการตั้งค่าค่าธรรมเนียมการชำระเงินที่เรียกเก็บจากหน่วยงานจัดเก็บภาษี ณ ที่จ่าย (TDS)</span><span class="sxs-lookup"><span data-stu-id="14da0-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="14da0-105">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่าการชำระเงิน \> ค่าธรรมเนียมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="14da0-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="14da0-106">[![หน้าค่าธรรมเนียมการชำระเงิน](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="14da0-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="14da0-107">เลือก **ใหม่** เพี่อสร้างค่าธรรมเนียมการชำระเงิน และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="14da0-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="14da0-108">ในฟิลด์ **ชนิดค่าธรรมเนียม** ให้เลือกชนิดของค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="14da0-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="14da0-109">**ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="14da0-109">**None**</span></span>
    - <span data-ttu-id="14da0-110">**ดอกเบี้ย** – ดอกเบี้ยจะเรียกเก็บในการจ่ายล่าช้า ที่จ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="14da0-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="14da0-111">**อื่นๆ** – ค่าธรรมเรียกอื่นๆ ที่เรียกเก็บในการจ่ายล่าช้า ที่จ่ายให้แก่ผู้จัดจำหน่ายของหน่วยงาน TDS</span><span class="sxs-lookup"><span data-stu-id="14da0-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="14da0-112">ถ้าคุณเลือก **ดอกเบี้ย** หรือ **อื่นๆ** ฟิลด์ **ค่าธรรมเนียม** จะถูกตั้งค่าเป็น **บัญชีแยกประเภท** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="14da0-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="14da0-113">ถ้าคุณเลือก **ดอกเบี้ย** หรือ **อื่นๆ** ในฟิลด์ **ชนิดฟิลด์** ในฟิลด์ **บัญชีหลัก** ให้เลือกบัญชีแยกประเภทที่จะลงรายการบัญชีดอกเบี้ยหรือค่าธรรมเนียมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="14da0-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="14da0-114">ป้อนรายละเอียดที่จำเป็นอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="14da0-114">Enter the other required details.</span></span>
6. <span data-ttu-id="14da0-115">ในบานหน้าต่างการปฏิบัติการ ให้เลือก **การตั้งค่าค่าธรรมเนียมการชำระงิน** เพื่อเปิดหน้า **การตั้งค่าค่าธรรมเนียมการชำระเงิน** ซึ่งคุณสามารถตั้งค่าค่าธรรมเนียมการชำระเงินให้กับชุดประกอบต่างๆ ของ ธนาคาร วิธีการจ่ายเงิน ข้อมูลจเพาะการจ่าย สกุลเงิน และช่วงวันที่</span><span class="sxs-lookup"><span data-stu-id="14da0-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="14da0-116">[![หน้าการตั้งค่าค่าธรรมเนียมการชำระเงิน](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="14da0-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="14da0-117">บนแท็บ **ภาพรวม** ในฟิลด์ **การจัดกลุ่ม** ให้ระบุว่าธนาคารใดที่คุณตั้งค่าค่าธรรมเนียมการชำระเงินไว้:</span><span class="sxs-lookup"><span data-stu-id="14da0-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="14da0-118">**ตาราง** – ค่าธรรมเนียมมีผลบังคับใช้เฉพาะบัญชีธนาคารหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="14da0-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="14da0-119">**กลุ่ม** – ค่าธรรมเนียมมีผลบังคับใช้เฉพาะกลุ่มธนาคารหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="14da0-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="14da0-120">**ทั้งหมด** - ค่าธรรมเนียมมีผลบังคับใช้สำหรับบัญชีธนาคารทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="14da0-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="14da0-121">ถ้าคุณเลือก **ตาราง** หรือ **กลุ่ม** ในฟิลด์ **การจัดกลุ่ม** ในฟิลด์ **ความสัมพันธ์ธนาคาร** ให้เลือกบัญชีธนาคารหรือกลุ่มธนาคารที่ต้องการ ซึ่งคุณตั้งค่าค่าธรรมเนียมการชำระเงินไว้</span><span class="sxs-lookup"><span data-stu-id="14da0-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="14da0-122">ในฟิลด์ **วิธีการชำระเงิน** ให้เลือกวิธีการชำระเงินที่จะใช้สำหรับการชำระค่าธรรมเนียมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="14da0-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="14da0-123">ในฟิลด์ **ข้อมูลจำเพาะเกี่ยวกับการชำระเงิน** ให้เลือกหรือป้อนรหัสข้อมูลจำเพาะเกี่ยวกับการชำระเงินที่สร้างขึ้นบนหน้า **ข้อมูลจำเพาะเกี่ยวกับการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="14da0-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="14da0-124">ข้อมูลจำเพาะเกี่ยวกับการชำระเงินถูกใช้กับการชำระเงินโดยวิธีการโอนเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="14da0-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="14da0-125">ในฟิลด์ **สกุลเงินในการชำระเงิน** เลือกสกุลเงินที่เรียกใช้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="14da0-126">เฉพาะธุรกรรมที่ใช้สกุลเงินที่เลือกเท่านั้น ที่สามารถเรียกใช้ค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="14da0-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="14da0-127">ถ้าคุณปล่อยฟิลด์นี้ว่างไว้ สกุลเงินทั้งหมดจะเรียกใช้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="14da0-128">ในฟิลด์ **เปอร์เซ็นต์/จํานวนเงิน** ให้เลือกวิธีการคํานวณ</span><span class="sxs-lookup"><span data-stu-id="14da0-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="14da0-129">ตัวเลือกคือ **จำนวนเงิน** **เปอร์เซ็นต์** และ **ช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="14da0-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="14da0-130">ในฟิลด์ **จํานวนเงินค่าธรรมเนียม** ให้ระบุยอดเงินค่าธรรมเนียมเป็นเปอร์เซ็นต์ของการชำระเงิน หรือยอดเงินเป็นยอดการชำระเงินรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="14da0-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="14da0-131">ในฟิลด์ **สกุลเงินค่าธรรมเนียม** ให้ระบุรหัสสกุลเงินของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="14da0-132">เลือกแท็บ **ทั่วไป** เพื่อดูหรือแก้ไขรายละเอียดเกี่ยวกับบัญชีธนาคารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14da0-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="14da0-133">[![แท็บทั่วไป](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="14da0-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="14da0-134">ในฟิลด์ **ขั้นต่ำ** ให้ป้อนยอดเงินธุรกรรมต่ำสุดที่เรียกใช้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="14da0-135">ในฟิลด์ **สูงสุด** ให้ป้อนยอดเงินธุรกรรมสูงสุดที่เรียกใช้ค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="14da0-136">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้กําหนดช่วงวันที่เพื่อคํานวณค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="14da0-137">ในฟิลด์ **ค่าธรรมเนียมขั้นต่ำ** ให้ระบุยอดเงินค่าธรรมเนียมเป็นเปอร์เซ็นต์ของการชำระเงิน หรือยอดเงินเป็นยอดการชำระเงินรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="14da0-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="14da0-138">ในฟิลด์ **กลุ่มภาษีขาย** ให้เลือกกลุ่มภาษีขายที่จะใช้ในการคํานวณภาษีขายให้กับยอดเงินค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="14da0-139">ในฟิลด์ **กลุ่มภาษีขายตามประเภทสินค้า** ให้เลือกกลุ่มภาษีขายตามประเภทสินค้าที่จะใช้ในการคํานวณกลุ่มภาษีขายตามประเภทสินค้าให้กับยอดเงินค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="14da0-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="14da0-140">เลือกแท็บ **ช่วงเวลา**</span><span class="sxs-lookup"><span data-stu-id="14da0-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="14da0-141">[![แท็บช่วงเวลา](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="14da0-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="14da0-142">ในฟิลด์ **วัน** ป้อนจำนวนวันระหว่างวันที่การลงรายการบัญชี (วันที่ให้ส่วนลด) ของการชำระเงิน และวันที่ครบกำหนดชำระของตั๋วสัญญาใช้เงิน</span><span class="sxs-lookup"><span data-stu-id="14da0-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="14da0-143">ในฟิลด์ **เปอร์เซ็นต์/จํานวนเงิน** ให้เลือกว่าข้อมูลระบุเป็นเปอร์เซ็นต์หรือจํานวนเงินที่ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="14da0-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="14da0-144">ในฟิลด์ **ยอดค่าธรรมเนียม** ให้ป้อนยอดเงินค่าธรรมเนียมเป็นเปอร์เซ็นต์ของการชำระเงิน หรือยอดเงินเป็นยอดการชำระเงินรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="14da0-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="14da0-145">ปิดหน้า **การตั้งค่าค่าธรรมเนียมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="14da0-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="14da0-146">ปิดหน้า **ค่าธรรมเนียมการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="14da0-146">Close the **Payment fee** page.</span></span>
