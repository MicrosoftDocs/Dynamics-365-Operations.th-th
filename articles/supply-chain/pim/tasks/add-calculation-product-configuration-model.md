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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438498"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="b8adc-103">เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b8adc-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8adc-104">กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="b8adc-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="b8adc-105">แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น </span><span class="sxs-lookup"><span data-stu-id="b8adc-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="b8adc-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="b8adc-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="b8adc-107">เพิ่มการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b8adc-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="b8adc-108">สร้างนิพจน์การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b8adc-108">Create calculation expression</span></span>
1. <span data-ttu-id="b8adc-109">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="b8adc-109">Click Edit expression.</span></span>
2. <span data-ttu-id="b8adc-110">ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish=="White", 10, 15]'</span><span class="sxs-lookup"><span data-stu-id="b8adc-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="b8adc-111">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b8adc-111">Click Validate.</span></span>
4. <span data-ttu-id="b8adc-112">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="b8adc-112">Click Close.</span></span>
5. <span data-ttu-id="b8adc-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b8adc-113">Click OK.</span></span>

