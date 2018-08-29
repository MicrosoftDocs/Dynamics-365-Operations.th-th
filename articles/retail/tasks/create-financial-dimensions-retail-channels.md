--- 
title: "สร้างมิติทางการเงินสำหรับช่องทางการค้าปลีก และตั้งค่าคอนฟิกค่ามิติบนร้านค้า"
description: "กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินของช่องทางการขายปลีกด้วยและค่ามิติและขั้นตอนต่างๆเพื่อตั้งค่าคอนฟิกค่ามิติทางการเงินในร้านค้าปลีก "
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="99aab-103">สร้างมิติทางการเงินสำหรับช่องทางการค้าปลีก และตั้งค่าคอนฟิกค่ามิติบนร้านค้า</span><span class="sxs-lookup"><span data-stu-id="99aab-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="99aab-104">กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินของช่องทางการขายปลีกด้วยและค่ามิติและขั้นตอนต่างๆเพื่อตั้งค่าคอนฟิกค่ามิติทางการเงินในร้านค้าปลีก </span><span class="sxs-lookup"><span data-stu-id="99aab-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="99aab-105">หัวข้อนี้ไม่ได้รวมถึงขั้นตอนอื่นที่เกี่ยวข้อง เช่น การสร้างเซ็ตมิติและโครงสร้างทางบัญชี </span><span class="sxs-lookup"><span data-stu-id="99aab-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="99aab-106">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="99aab-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="99aab-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="99aab-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="99aab-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="99aab-108">Click New.</span></span>
3. <span data-ttu-id="99aab-109">ในฟิลด์ ใช้ค่าจาก เลือก 'ช่องทางการขายปลีก'</span><span class="sxs-lookup"><span data-stu-id="99aab-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="99aab-110">ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="99aab-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="99aab-111">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="99aab-111">Click Activate.</span></span>
6. <span data-ttu-id="99aab-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="99aab-112">Click Close.</span></span>
7. <span data-ttu-id="99aab-113">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="99aab-113">Click Activate.</span></span>
8. <span data-ttu-id="99aab-114">คลิกค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="99aab-114">Click Dimension values.</span></span>
9. <span data-ttu-id="99aab-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="99aab-115">Close the page.</span></span>
10. <span data-ttu-id="99aab-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="99aab-116">Click Save.</span></span>
11. <span data-ttu-id="99aab-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="99aab-117">Close the page.</span></span>
12. <span data-ttu-id="99aab-118">ไปยังการขายปลีกและการค้า > ช่องทาง > ร้านค้าปลีก > ร้านค้าปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="99aab-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="99aab-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="99aab-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="99aab-120">สลับการขยายของส่วนมิติการเงิน</span><span class="sxs-lookup"><span data-stu-id="99aab-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="99aab-121">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="99aab-121">Click Edit.</span></span>
16. <span data-ttu-id="99aab-122">ในฟิลด์ช่องทางการขายปลีก คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="99aab-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="99aab-123">ในรายการ ให้ค้นหาและเลือกค่ามิติสำหรับร้านค้าที่กำลังถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="99aab-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="99aab-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="99aab-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="99aab-125">ในฟิลด์ต้นทุนศูนย์กลาง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="99aab-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="99aab-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="99aab-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="99aab-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="99aab-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="99aab-128">ในฟิลด์แผนก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="99aab-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="99aab-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="99aab-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="99aab-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="99aab-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="99aab-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="99aab-131">Click Save.</span></span>


