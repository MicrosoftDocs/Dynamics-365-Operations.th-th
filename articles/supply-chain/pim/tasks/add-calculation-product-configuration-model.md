---
title: เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812696"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="95be9-103">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="95be9-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95be9-104">กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="95be9-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="95be9-105">แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="95be9-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="95be9-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="95be9-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="95be9-107">เพิ่มการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="95be9-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="95be9-108">สร้างนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="95be9-108">Create calculation expression</span></span>
1. <span data-ttu-id="95be9-109">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="95be9-109">Click Edit expression.</span></span>
2. <span data-ttu-id="95be9-110">ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish == "ขาว" 10, 15]'</span><span class="sxs-lookup"><span data-stu-id="95be9-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="95be9-111">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="95be9-111">Click Validate.</span></span>
4. <span data-ttu-id="95be9-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="95be9-112">Click Close.</span></span>
5. <span data-ttu-id="95be9-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="95be9-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]