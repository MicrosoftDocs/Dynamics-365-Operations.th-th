---
title: เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ac010b96892450c8d37bb08f967ecf4491b4b5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148020"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="416fc-103">เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="416fc-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="416fc-104">กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="416fc-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="416fc-105">แสดงวิธีการกำหนดว่าการป้องกันมุมต้องใช้กับลำโพง ถ้าผู้ใช้เลือกเป็นตะแกรงด้านหน้าเป็นโลหะ </span><span class="sxs-lookup"><span data-stu-id="416fc-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="416fc-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="416fc-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="416fc-107">สร้างข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="416fc-107">Create an expression constraint</span></span>
1. <span data-ttu-id="416fc-108">คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="416fc-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="416fc-109">คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="416fc-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="416fc-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="416fc-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="416fc-111">ตัวอย่างนี้ใช้แบบจำลองลำโพงระดับสูง</span><span class="sxs-lookup"><span data-stu-id="416fc-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="416fc-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="416fc-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="416fc-113">ขยายส่วนข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="416fc-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="416fc-114">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="416fc-114">Click Add.</span></span>
7. <span data-ttu-id="416fc-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="416fc-115">Click Create.</span></span>
8. <span data-ttu-id="416fc-116">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="416fc-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="416fc-117">ป้อนนิพจน์</span><span class="sxs-lookup"><span data-stu-id="416fc-117">Enter expression</span></span>
1. <span data-ttu-id="416fc-118">คลิกแก้ไขนิพจน์</span><span class="sxs-lookup"><span data-stu-id="416fc-118">Click Edit expression.</span></span>
    * <span data-ttu-id="416fc-119">ถ้าคุณปลดล็อคอินเทอร์เฟสผู้ใช้ในงานที่บันทึกไว้ในขั้นตอนนี้ คุณจะสามารถใช้ IntelliSense และรายการของสัญลักษณ์เพื่อสร้างนิพจน์ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="416fc-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="416fc-120">ในฟิลด์ ConstraintBody ให้ป้อน ' Implies [FrontGrill == "โลหะ" CornerProtection] '</span><span class="sxs-lookup"><span data-stu-id="416fc-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="416fc-121">ตรรกะนิพจน์นี้กล่าวว่า ถ้าตะแกรงด้านหน้าเป็นโลหะ จะต้องเลือกตัวเลือกการป้องกันมุม</span><span class="sxs-lookup"><span data-stu-id="416fc-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="416fc-122">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="416fc-122">Click Validate.</span></span>
    * <span data-ttu-id="416fc-123">ฟังก์ชันการตรวจสอบดำเนินการโดยใช้นิพจน์ข้อจำกัดและตรวจสอบหาข้อผิดพลาดทางไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="416fc-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="416fc-124">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="416fc-124">Click Close.</span></span>
5. <span data-ttu-id="416fc-125">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="416fc-125">Click OK.</span></span>

