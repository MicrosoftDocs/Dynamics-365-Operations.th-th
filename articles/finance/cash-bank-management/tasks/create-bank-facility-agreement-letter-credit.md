---
title: สร้างข้อตกลงสินเชื่อธนาคารสำหรับเลตเตอร์ออฟเครดิต
description: 'งานนี้นำไปสู่การสร้างข้อตกลงสินเชื่อของธนาคารเพื่อประมวลผลเลตเตอร์ออฟเครดิต '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e63e0ffa4ddafd38595d7e9d84ffa2399a9f67b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188222"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="64f49-103">สร้างข้อตกลงสินเชื่อธนาคารสำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="64f49-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64f49-104">งานนี้นำไปสู่การสร้างข้อตกลงสินเชื่อของธนาคารเพื่อประมวลผลเลตเตอร์ออฟเครดิต </span><span class="sxs-lookup"><span data-stu-id="64f49-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="64f49-105">คุณจะต้องตั้งค่าสินเชื่อธนาคารและการลงบัญชีโพรไฟล์ก่อนหน้างานนี้ </span><span class="sxs-lookup"><span data-stu-id="64f49-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="64f49-106">งานนี้ใช้บริษัทสาธิต 'USMF'</span><span class="sxs-lookup"><span data-stu-id="64f49-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="64f49-107">สร้างข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="64f49-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="64f49-108">ไปที่การจัดการเงินสดและธนาคาร > เลตเตอร์ออฟเครดิต > ข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="64f49-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="64f49-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="64f49-109">Click New.</span></span>
3. <span data-ttu-id="64f49-110">ในฟิลด์หมายเลขข้อตกลง ให้ป้อนหมายเลขข้อตกลงตามข้อตกลงกับธนาคาร</span><span class="sxs-lookup"><span data-stu-id="64f49-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="64f49-111">ในฟิลด์บัญชีธนาคาร ให้ป้อนหมายเลขบัญชีที่ธนาคารผู้ออก</span><span class="sxs-lookup"><span data-stu-id="64f49-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="64f49-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="64f49-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="64f49-113">ในฟิลด์วันที่เริมต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="64f49-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="64f49-114">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="64f49-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="64f49-115">ขยายหรือยุบส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="64f49-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="64f49-116">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="64f49-116">Click Add line.</span></span>
10. <span data-ttu-id="64f49-117">ในฟิลด์ชนิดสินเชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="64f49-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="64f49-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="64f49-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="64f49-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="64f49-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="64f49-120">ในฟิลด์ขีดจำกัด ให้ป้อนยอดเงินสินเชื่อตามที่ได้เจรจาไว้กับธนาคาร</span><span class="sxs-lookup"><span data-stu-id="64f49-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="64f49-121">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="64f49-121">Click Save.</span></span>
15. <span data-ttu-id="64f49-122">คลิกขยายเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="64f49-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="64f49-123">ในฟิลด์หมายเลขข้อตกลงใหม่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="64f49-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="64f49-124">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="64f49-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="64f49-125">คลิกขยาย</span><span class="sxs-lookup"><span data-stu-id="64f49-125">Click Extend.</span></span>
19. <span data-ttu-id="64f49-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="64f49-126">Close the page.</span></span>

