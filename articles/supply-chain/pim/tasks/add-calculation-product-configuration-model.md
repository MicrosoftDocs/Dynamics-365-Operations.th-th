---
title: เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "343178"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="f0d68-103">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="f0d68-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0d68-104">กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="f0d68-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="f0d68-105">แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="f0d68-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="f0d68-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f0d68-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="f0d68-107">เพิ่มการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f0d68-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="f0d68-108">สร้างนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="f0d68-108">Create calculation expression</span></span>
1. <span data-ttu-id="f0d68-109">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="f0d68-109">Click Edit expression.</span></span>
2. <span data-ttu-id="f0d68-110">ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish == "ขาว" 10, 15]'</span><span class="sxs-lookup"><span data-stu-id="f0d68-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="f0d68-111">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f0d68-111">Click Validate.</span></span>
4. <span data-ttu-id="f0d68-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="f0d68-112">Click Close.</span></span>
5. <span data-ttu-id="f0d68-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f0d68-113">Click OK.</span></span>

