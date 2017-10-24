--- 
title: "สร้างข้อตกลงสินเชื่อธนาคารสำหรับหนังสือค้ำประกัน"
description: "งานนี้สร้างข้อตกลงสินเชื่อของธนาคารที่จะประมวลผลหนังสือค้ำประกัน "
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7b6e35c922edeb3c3c7a33ff741a25e699242abf
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="9ca25-103">สร้างข้อตกลงสินเชื่อธนาคารสำหรับหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="9ca25-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ca25-104">งานนี้สร้างข้อตกลงสินเชื่อของธนาคารที่จะประมวลผลหนังสือค้ำประกัน </span><span class="sxs-lookup"><span data-stu-id="9ca25-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="9ca25-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="9ca25-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="9ca25-106">สร้างข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ca25-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="9ca25-107">ไปที่การจัดการบัญชีเงินสดและธนาคาร > หนังสือค้ำประกัน > ข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ca25-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="9ca25-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9ca25-108">Click New.</span></span>
3. <span data-ttu-id="9ca25-109">ในฟิลด์หมายเลขข้อตกลง ให้ป้อนหมายเลขข้อตกลงของธนาคารสำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9ca25-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="9ca25-110">ในฟิลด์บัญชีธนาคาร ให้เลือกหมายเลขบัญชีธนาคารซึ่งหนังสือค้ำประกันจะได้เปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="9ca25-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="9ca25-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9ca25-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9ca25-112">ในฟิลด์วันที่เริมต้น ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9ca25-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="9ca25-113">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9ca25-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="9ca25-114">เปิดปิดการขยายของส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="9ca25-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="9ca25-115">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="9ca25-115">Click Add line.</span></span>
10. <span data-ttu-id="9ca25-116">ในฟิลด์ชนิดสินเชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9ca25-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9ca25-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9ca25-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9ca25-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9ca25-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="9ca25-119">ในฟิลด์ขีดจำกัด ให้ป้อนยอดเงินตามที่เจรจาไว้กับธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ca25-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="9ca25-120">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="9ca25-120">Click Save.</span></span>
15. <span data-ttu-id="9ca25-121">สลับการขยายของส่วนหนังสือค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="9ca25-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="9ca25-122">ในฟิลด์วิธีการคำนวณ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="9ca25-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="9ca25-123">ป้อนวิธีการคำนวณและรายละเอียดเปอร์เซ็นต์สำหรับเงินประกันเงินสด ค่าคอมมิชชันของการออก ค่าคอมมิชชันของการขยายเวลา ค่าคอมมิชชันของการเพิ่มมูลค่าหรือค่าคอมมิชชันของการลดมูลค่า ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9ca25-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="9ca25-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9ca25-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="9ca25-125">ขยายเวลาข้อตกลงสินเชื่อธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9ca25-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="9ca25-126">คลิกขยายเพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="9ca25-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="9ca25-127">ในฟิลด์หมายเลขข้อตกลงใหม่ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9ca25-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="9ca25-128">ในฟิลด์วันที่สิ้นสุด ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9ca25-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="9ca25-129">คลิกขยาย</span><span class="sxs-lookup"><span data-stu-id="9ca25-129">Click Extend.</span></span>
5. <span data-ttu-id="9ca25-130">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9ca25-130">Click Save.</span></span>
6. <span data-ttu-id="9ca25-131">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9ca25-131">Close the page.</span></span>


