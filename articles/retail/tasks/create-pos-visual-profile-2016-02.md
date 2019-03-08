---
title: สร้างโพรไฟล์ภาพการขายหน้าร้าน (POS)
description: 'กระบวนการนี้นำไปสู่การสร้างโพรไฟล์ภาพการขายหน้าร้าน (POS) ขึ้นใหม่ '
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0234512e037d8818ce2282959cfd0763b41b9429
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "358151"
---
# <a name="create-point-of-sale-pos-visual-profiles"></a><span data-ttu-id="140d9-103">สร้างโพรไฟล์ภาพการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="140d9-103">Create point of sale (POS) visual profiles</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="140d9-104">กระบวนการนี้นำไปสู่การสร้างโพรไฟล์ภาพการขายหน้าร้าน (POS) ขึ้นใหม่ </span><span class="sxs-lookup"><span data-stu-id="140d9-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="140d9-105">โพรไฟล์ภาพประกอบด้วยข้อมูลพื้นฐานที่กำหนดรูปลักษณ์ของเครื่องบันทึกเงินสด POS </span><span class="sxs-lookup"><span data-stu-id="140d9-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="140d9-106">คุณสามารถสร้างโพรไฟล์ภาพต่าง ๆ และกำหนดโพรไฟล์เฉพาะให้ทำงานบนเครื่องบันทึกเงินสดหนึ่ง ๆ </span><span class="sxs-lookup"><span data-stu-id="140d9-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="140d9-107">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="140d9-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="140d9-108">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > การตั้งค่า POS > โพรไฟล์ POS > โพรไฟล์ภาพ</span><span class="sxs-lookup"><span data-stu-id="140d9-108">Go to Retail and commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="140d9-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="140d9-109">Click New.</span></span>
3. <span data-ttu-id="140d9-110">ในฟิลด์หมายเลขโพรไฟล์ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="140d9-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="140d9-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="140d9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="140d9-112">ในฟิลด์ชนิดของแอพพลิเคชั่น ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="140d9-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="140d9-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="140d9-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="140d9-114">ในฟิลด์ชุดรูปแบบ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="140d9-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="140d9-115">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="140d9-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="140d9-116">ในฟิลด์สีอักขระการออกเสียง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="140d9-116">In the Accent color field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="140d9-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="140d9-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="140d9-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="140d9-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="140d9-119">สลับการขยายของการล็อกอินในส่วนพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="140d9-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="140d9-120">ในฟิลด์รหัสรูปภาพแนวนอน ให้เลือกหรือป้อนรหัสรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="140d9-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="140d9-121">ในฟิลด์รหัสรูปภาพแนวตั้ง ให้เลือกหรือป้อนรหัสรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="140d9-121">In the Portait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="140d9-122">สลับการขยายส่วนพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="140d9-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="140d9-123">RequestPopup รหัสรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="140d9-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="140d9-124">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="140d9-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="140d9-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="140d9-125">Click Save.</span></span>

