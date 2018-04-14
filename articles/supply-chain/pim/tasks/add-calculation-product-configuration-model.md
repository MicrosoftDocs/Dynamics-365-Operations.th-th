--- 
title: "เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์"
description: "กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ "
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 01434e8dbd1e66ae04d0b7910ef2be582297ac84
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="1bb57-103">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="1bb57-103">Add a calculation to a product configuration model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bb57-104">กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="1bb57-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="1bb57-105">แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="1bb57-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="1bb57-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="1bb57-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="1bb57-107">เพิ่มการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1bb57-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="1bb57-108">สร้างนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="1bb57-108">Create calculation expression</span></span>
1. <span data-ttu-id="1bb57-109">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="1bb57-109">Click Edit expression.</span></span>
2. <span data-ttu-id="1bb57-110">ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish == "ขาว" 10, 15]'</span><span class="sxs-lookup"><span data-stu-id="1bb57-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="1bb57-111">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="1bb57-111">Click Validate.</span></span>
4. <span data-ttu-id="1bb57-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="1bb57-112">Click Close.</span></span>
5. <span data-ttu-id="1bb57-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="1bb57-113">Click OK.</span></span>


