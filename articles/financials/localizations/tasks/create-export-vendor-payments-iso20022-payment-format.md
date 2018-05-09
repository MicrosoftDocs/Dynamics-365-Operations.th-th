--- 
title: "สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022"
description: "กระบวนงานนี้แสดงวิธีการสร้างบรรทัดการชำระเงินในสมุดรายวันการชำระเงินของผู้จัดจำหน่ายและการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้าย ISO2022 "
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 906f9611370e19ad4f063d15608d3564c5292c96
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="ff83b-103">สร้างและส่งออกการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้รูปแบบการชำระเงิน ISO20022</span><span class="sxs-lookup"><span data-stu-id="ff83b-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff83b-104">กระบวนงานนี้แสดงวิธีการสร้างบรรทัดการชำระเงินในสมุดรายวันการชำระเงินของผู้จัดจำหน่ายและการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายโดยใช้ตัวอย่างการโอนย้าย ISO2022 </span><span class="sxs-lookup"><span data-stu-id="ff83b-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="ff83b-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="ff83b-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="ff83b-106">นี่คือกระบวนงานที่ห้าจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ff83b-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ff83b-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="ff83b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="ff83b-108">สร้างบรรทัดรายการการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ff83b-108">Create payment lines</span></span>
1. <span data-ttu-id="ff83b-109">ไปที่ > บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ff83b-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="ff83b-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ff83b-110">Click New.</span></span>
3. <span data-ttu-id="ff83b-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ff83b-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ff83b-112">ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff83b-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="ff83b-113">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="ff83b-113">Click Lines.</span></span>
6. <span data-ttu-id="ff83b-114">คลิก ข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ff83b-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="ff83b-115">คลิกสร้างข้อเสนอการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ff83b-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="ff83b-116">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="ff83b-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="ff83b-117">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="ff83b-117">Click Filter.</span></span>
10. <span data-ttu-id="ff83b-118">ในรายการ เลือกแถวสำหรับตารางผู้จัดจำหน่ายและฟิลด์บัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ff83b-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="ff83b-119">ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ff83b-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="ff83b-120">คุณสามารถใช้เกณฑ์ใดๆ สำหรับการเลือกธุรกรรมของผู้จัดจำหน่ายที่จะชำระเงิน สำหรับตัวอย่างนี้จะใช้ DE-001 เป็นบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ff83b-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="ff83b-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ff83b-121">Click OK.</span></span>
13. <span data-ttu-id="ff83b-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="ff83b-122">Click OK.</span></span>
14. <span data-ttu-id="ff83b-123">คลิกสร้างการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ff83b-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="ff83b-124">สร้างไฟล์การชำระเงิน ISO20022</span><span class="sxs-lookup"><span data-stu-id="ff83b-124">Generate an ISO20022 payment file</span></span>


