---
title: สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022
description: 'กระบวนงานนี้แสดงวิธีการสร้างบรรทัดการชำระเงินในสมุดรายวันการชำระเงินของผู้จัดจำหน่ายและการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้าย ISO2022 '
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448510"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="ce36e-103">สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022</span><span class="sxs-lookup"><span data-stu-id="ce36e-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce36e-104">หัวข้อนี้อธิบายวิธีการสร้างรายการการชำระเงินในสมุดรายวันการชำระเงินผู้จัดจำหน่าย และสร้างไฟล์การชำระเงินผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้ายเครดิต ISO2022</span><span class="sxs-lookup"><span data-stu-id="ce36e-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="ce36e-105">นี่คือกระบวนงานที่ห้าจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ce36e-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ce36e-106">ใช้ข้อมูลสาธิต DEMF เพื่อทำให้ตัวอย่างนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ce36e-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="ce36e-107">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="ce36e-107">Example</span></span>

1.    <span data-ttu-id="ce36e-108">ไปที่ **บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ce36e-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="ce36e-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ce36e-109">Click **New**.</span></span>
3.    <span data-ttu-id="ce36e-110">ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ce36e-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="ce36e-111">คลิก **รายการ > การประชุมข้อเสนอการชำระเงิน > สร้างการประชุมข้อเสนอการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ce36e-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="ce36e-112">ขยายส่วน **เรกคอร์ดที่จะรวม**</span><span class="sxs-lookup"><span data-stu-id="ce36e-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="ce36e-113">คลิก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="ce36e-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="ce36e-114">ในรายการ เลือกแถวสำหรับ **ตารางผู้จัดจำหน่าย** และ **ฟิลด์ลูกค้าองค์กรของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="ce36e-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="ce36e-115">ในฟิลด์ **เกณฑ์** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ce36e-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ce36e-116">คุณสามารถเลือกเกณฑ์ใดๆ สำหรับการเลือกธุรกรรมผู้จัดจำหน่ายเพื่อจ่าย สำหรับตัวอย่างนี้ ใช้ DE-001 เป็นลูกค้าองค์กรของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ce36e-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="ce36e-117">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="ce36e-117">Click **OK**.</span></span>
13.    <span data-ttu-id="ce36e-118">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="ce36e-118">Click **OK**.</span></span>
14.    <span data-ttu-id="ce36e-119">คลิก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ce36e-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="ce36e-120">สร้างไฟล์การชำระเงิน ISO20022</span><span class="sxs-lookup"><span data-stu-id="ce36e-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="ce36e-121">คลิก **สร้างการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="ce36e-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="ce36e-122">ในฟิลด์ **วิธีการชำระเงิน** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ce36e-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="ce36e-123">ในฟิลด์ **ชื่อไฟล์** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ce36e-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="ce36e-124">สำหรับตัวอย่างนี้ เนื่องจากการชำระเงิน EUR ไฟล์ที่สร้างจะเป็นไปตาม SEPA</span><span class="sxs-lookup"><span data-stu-id="ce36e-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="ce36e-125">การโอนย้ายเครดิต ISO20022 พร้อมกับรูปแบบการชำระเงินของผู้จัดจำหน่ายอื่นๆ ยังสามารถใช้สำหรับการสร้างการชำระเงินในสกุลเงินอื่นๆ ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="ce36e-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="ce36e-126">ในฟิลด์ **บัญชีธนาคาร** ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ce36e-126">In the **Bank account** field, enter or select a value.</span></span>

