---
title: เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986514"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="e6879-103">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e6879-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6879-104">กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="e6879-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="e6879-105">แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="e6879-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="e6879-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="e6879-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="e6879-107">เพิ่มการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e6879-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="e6879-108">สร้างนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="e6879-108">Create calculation expression</span></span>
1. <span data-ttu-id="e6879-109">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="e6879-109">Click Edit expression.</span></span>
2. <span data-ttu-id="e6879-110">ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish == "ขาว" 10, 15]'</span><span class="sxs-lookup"><span data-stu-id="e6879-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="e6879-111">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="e6879-111">Click Validate.</span></span>
4. <span data-ttu-id="e6879-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="e6879-112">Click Close.</span></span>
5. <span data-ttu-id="e6879-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e6879-113">Click OK.</span></span>

