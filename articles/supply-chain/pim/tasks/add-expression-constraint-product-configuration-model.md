---
title: เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920892"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="bde7e-103">เพิ่มข้อจำกัดนิพจน์ไปที่แบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="bde7e-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bde7e-104">กระบวนงานนี้แสดงวิธีที่คุณสามารถเพิ่มข้อจำกัดนิพจน์ใหม่ในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="bde7e-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="bde7e-105">แสดงวิธีการกำหนดว่าการป้องกันมุมต้องใช้กับลำโพง ถ้าผู้ใช้เลือกเป็นตะแกรงด้านหน้าเป็นโลหะ </span><span class="sxs-lookup"><span data-stu-id="bde7e-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="bde7e-106">กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="bde7e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="bde7e-107">สร้างข้อจำกัดนิพจน์</span><span class="sxs-lookup"><span data-stu-id="bde7e-107">Create an expression constraint</span></span>

1. <span data-ttu-id="bde7e-108">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="bde7e-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="bde7e-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bde7e-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bde7e-110">ตัวอย่างนี้ใช้แบบจำลองลำโพงระดับสูง</span><span class="sxs-lookup"><span data-stu-id="bde7e-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="bde7e-111">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bde7e-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="bde7e-112">ขยายส่วน **ข้อจำกัด**</span><span class="sxs-lookup"><span data-stu-id="bde7e-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="bde7e-113">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="bde7e-113">Select **Add**.</span></span>
7. <span data-ttu-id="bde7e-114">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="bde7e-114">Select **Create**.</span></span>
8. <span data-ttu-id="bde7e-115">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bde7e-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="bde7e-116">ป้อนนิพจน์</span><span class="sxs-lookup"><span data-stu-id="bde7e-116">Enter expression</span></span>

1. <span data-ttu-id="bde7e-117">เลือก **แก้ไขนิพจน์**</span><span class="sxs-lookup"><span data-stu-id="bde7e-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="bde7e-118">ถ้าคุณปลดล็อคอินเทอร์เฟสผู้ใช้ในงานที่บันทึกไว้ในขั้นตอนนี้ คุณจะสามารถใช้ IntelliSense และรายการของสัญลักษณ์เพื่อสร้างนิพจน์ข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="bde7e-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="bde7e-119">ในฟิลด์ **ConstraintBody** ให้ป้อน 'Implies[FrontGrill=="Metal", CornerProtection] '</span><span class="sxs-lookup"><span data-stu-id="bde7e-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="bde7e-120">ตรรกะนิพจน์นี้กล่าวว่า ถ้าตะแกรงด้านหน้าเป็นโลหะ จะต้องเลือกตัวเลือกการป้องกันมุม</span><span class="sxs-lookup"><span data-stu-id="bde7e-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="bde7e-121">เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="bde7e-121">Select **Validate**.</span></span>
    * <span data-ttu-id="bde7e-122">ฟังก์ชันการตรวจสอบดำเนินการโดยใช้นิพจน์ข้อจำกัดและตรวจสอบหาข้อผิดพลาดทางไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="bde7e-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="bde7e-123">เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bde7e-123">Select **Close**.</span></span>
5. <span data-ttu-id="bde7e-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="bde7e-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]