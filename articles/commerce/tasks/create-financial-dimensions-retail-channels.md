---
title: สร้างค่ามิติทางการเงินสำหรับช่องทางการค้าปลีกและตั้งค่าคอนฟิกค่ามิติบนร้านค้า
description: กระบวนงานนี้นำไปสู่การสร้างมิติทางการเงินของช่องทางการค้าด้วยค่ามิติและขั้นตอนต่างๆ เพื่อตั้งค่าคอนฟิกค่ามิติทางการเงินในร้านค้า
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc9c9a400bee1280b32f10b1e8f55e581e1984
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964756"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="14934-103">สร้างค่ามิติทางการเงินสำหรับช่องทางการค้าปลีกและตั้งค่าคอนฟิกค่ามิติบนร้านค้า</span><span class="sxs-lookup"><span data-stu-id="14934-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14934-104">กระบวนงานนี้นำไปสู่การสร้างมิติทางการเงินของช่องทางการค้าด้วยค่ามิติและขั้นตอนต่างๆ เพื่อตั้งค่าคอนฟิกค่ามิติทางการเงินในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="14934-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="14934-105">หัวข้อนี้ไม่ได้รวมถึงขั้นตอนอื่นที่เกี่ยวข้อง เช่น การสร้างเซ็ตมิติและโครงสร้างทางบัญชี </span><span class="sxs-lookup"><span data-stu-id="14934-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="14934-106">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="14934-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="14934-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="14934-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="14934-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="14934-108">Click New.</span></span>
3. <span data-ttu-id="14934-109">ในฟิลด์ ใช้ค่าจาก เลือก 'ช่องทาง Commerce'</span><span class="sxs-lookup"><span data-stu-id="14934-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="14934-110">ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="14934-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="14934-111">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="14934-111">Click Activate.</span></span>
6. <span data-ttu-id="14934-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="14934-112">Click Close.</span></span>
7. <span data-ttu-id="14934-113">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="14934-113">Click Activate.</span></span>
8. <span data-ttu-id="14934-114">คลิกค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="14934-114">Click Dimension values.</span></span>
9. <span data-ttu-id="14934-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="14934-115">Close the page.</span></span>
10. <span data-ttu-id="14934-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="14934-116">Click Save.</span></span>
11. <span data-ttu-id="14934-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="14934-117">Close the page.</span></span>
12. <span data-ttu-id="14934-118">ไปยัง การขายปลีกและการค้า > ช่องทาง > ร้านค้า > ร้านค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="14934-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="14934-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14934-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="14934-120">สลับการขยายของส่วนมิติการเงิน</span><span class="sxs-lookup"><span data-stu-id="14934-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="14934-121">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="14934-121">Click Edit.</span></span>
16. <span data-ttu-id="14934-122">ในฟิลด์ช่องทาง Commerce ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="14934-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="14934-123">ในรายการ ให้ค้นหาและเลือกค่ามิติสำหรับร้านค้าที่กำลังถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="14934-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="14934-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14934-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="14934-125">ในฟิลด์ต้นทุนศูนย์กลาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="14934-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="14934-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="14934-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="14934-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14934-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="14934-128">ในฟิลด์แผนก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="14934-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="14934-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="14934-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="14934-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="14934-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="14934-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="14934-131">Click Save.</span></span>

