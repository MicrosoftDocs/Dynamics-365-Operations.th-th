---
title: สร้างข้อตกลงสินเชื่อธนาคารสำหรับเลตเตอร์ออฟเครดิต
description: 'งานนี้นำไปสู่การสร้างข้อตกลงสินเชื่อของธนาคารเพื่อประมวลผลเลตเตอร์ออฟเครดิต '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582a41a0a4a3c509eae8a05c57b0910446addb26
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834847"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="7c11d-103">สร้างข้อตกลงสินเชื่อธนาคารสำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="7c11d-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c11d-104">งานนี้นำไปสู่การสร้างข้อตกลงสินเชื่อของธนาคารเพื่อประมวลผลเลตเตอร์ออฟเครดิต </span><span class="sxs-lookup"><span data-stu-id="7c11d-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="7c11d-105">คุณจะต้องตั้งค่าสินเชื่อธนาคารและการลงบัญชีโพรไฟล์ก่อนหน้างานนี้ </span><span class="sxs-lookup"><span data-stu-id="7c11d-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="7c11d-106">งานนี้ใช้บริษัทสาธิต 'USMF'</span><span class="sxs-lookup"><span data-stu-id="7c11d-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="7c11d-107">สร้างข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7c11d-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="7c11d-108">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > ข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7c11d-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="7c11d-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7c11d-109">Click New.</span></span>
3. <span data-ttu-id="7c11d-110">ในฟิลด์หมายเลขข้อตกลง ให้ป้อนหมายเลขข้อตกลงตามข้อตกลงกับธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7c11d-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="7c11d-111">ในฟิลด์บัญชีธนาคาร ให้ป้อนหมายเลขบัญชีที่ธนาคารผู้ออก</span><span class="sxs-lookup"><span data-stu-id="7c11d-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="7c11d-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7c11d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7c11d-113">ในฟิลด์วันที่เริมต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7c11d-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="7c11d-114">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7c11d-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="7c11d-115">ขยายหรือยุบส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="7c11d-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="7c11d-116">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="7c11d-116">Click Add line.</span></span>
10. <span data-ttu-id="7c11d-117">ในฟิลด์ชนิดสินเชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7c11d-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7c11d-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7c11d-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7c11d-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7c11d-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7c11d-120">ในฟิลด์ขีดจำกัด ให้ป้อนยอดเงินสินเชื่อตามที่ได้เจรจาไว้กับธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7c11d-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="7c11d-121">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="7c11d-121">Click Save.</span></span>
15. <span data-ttu-id="7c11d-122">คลิกขยายเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7c11d-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="7c11d-123">ในฟิลด์หมายเลขข้อตกลงใหม่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7c11d-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="7c11d-124">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="7c11d-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="7c11d-125">คลิกขยาย</span><span class="sxs-lookup"><span data-stu-id="7c11d-125">Click Extend.</span></span>
19. <span data-ttu-id="7c11d-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7c11d-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]