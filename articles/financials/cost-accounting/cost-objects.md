---
title: "มิติออบเจ็กต์ต้นทุน"
description: "เมื่อคุณวิเคราะห์ต้นทุน คุณสามารถใช้มิติองค์ประกอบต้นทุนเพื่อกำหนดว่าจะให้ต้นทุนไปที่ใด คุณสามารถใช้มิติออบเจ็กต์ต้นทุนเพื่อกำหนดตำแหน่งที่คุณควรกำหนดต้นทุน หัวข้อนี้แสดงข้อมูลเกี่ยวกับมิติออบเจ็กต์ต้นทุน"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8195b776e5d46485172c9f5550ab4ed6d8623dfc
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="2e28e-105">มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-105">Cost object dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2e28e-106">เมื่อคุณวิเคราะห์ต้นทุน คุณสามารถใช้มิติองค์ประกอบต้นทุนเพื่อกำหนดว่าจะให้ต้นทุนไปที่ใด</span><span class="sxs-lookup"><span data-stu-id="2e28e-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="2e28e-107">คุณสามารถใช้มิติออบเจ็กต์ต้นทุนเพื่อกำหนดตำแหน่งที่คุณควรกำหนดต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="2e28e-108">หัวข้อนี้แสดงข้อมูลเกี่ยวกับมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="2e28e-109">ออบเจ็กต์ต้นทุนอาจเป็นออบเจ็กต์ชนิดใดก็ได้ที่คุณต้องการประเมิน ปันส่วนต้นทุนไปยัง หรือวัดโดยตรง</span><span class="sxs-lookup"><span data-stu-id="2e28e-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="2e28e-110">โดยทั่วไปออบเจ็กต์ต้นทุนประกอบด้วยผลิตภัณฑ์ โครงการ ทรัพยากร แผนก ศูนย์ต้นทุน และภูมิภาคทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="2e28e-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="2e28e-111">การจัดการใช้ออบเจ็กต์ต้นทุนในการวัดปริมาณต้นทุนและยังใช้ในการกระตุ้นการวิเคราะห์ความสามารถในการทำกำไรอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2e28e-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="2e28e-112">มิติออบเจ็กต์ต้นทุนและสมาชิกมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="2e28e-113">ออบเจ็กต์ต้นทุนจะถูกเรียกว่า *มิติออบเจ็กต์ต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="2e28e-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="2e28e-114">หลังจากที่คุณได้เลือกเอนทิตี้ที่ควรแสดงถึงมิติออบเจ็กต์ต้นทุนแล้ว คุณต้องระบุค่ามิติแต่ละรายการ หรือนำเข้าไปยังการบัญชีต้นทุนจากระบบต้นทางอื่น</span><span class="sxs-lookup"><span data-stu-id="2e28e-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="2e28e-115">ค่ามิติแต่ละรายการเหล่านี้จะถูกเรียกว่า *สมาชิกของมิติออบเจ็กต์ต้นทุน*</span><span class="sxs-lookup"><span data-stu-id="2e28e-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="2e28e-116">ตัวอย่างเช่น คุณต้องการใช้มิติทางการเงินที่มีการตั้งชื่อศูนย์ต้นทุนเป็นมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="2e28e-117">เมื่อต้องการดูว่าต้นทุนไปยังแต่ละศูนย์ต้นทุนได้อย่างไร คุณต้องนำเข้าสมาชิกของมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="2e28e-118">ในกรณีนี้ สมาชิกของมิติออบเจ็กต์ต้นทุนเป็นศูนย์ต้นทุนจริง เช่น การขาย การผลิต การจัดการ และที่ตั้งทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="2e28e-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="2e28e-119">ภาพหน้าจอต่อไปนี้แสดงตัวอย่างของศูนย์ต้นทุนเป็นมิติออบเจ็กต์ต้นทุนที่มีศูนย์ต้นทุนจริงเป็นสมาชิกของมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="2e28e-120">[![มิติออบเจ็กต์ต้นทุน](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="2e28e-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="2e28e-121">นำเข้าสมาชิกของมิติออบเจ็กต์ต้นทุนผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="2e28e-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="2e28e-122">เมื่อต้องการทำให้การนำเข้าสมาชิกของมิติออบเจ็กต์ต้นทุนง่ายขึ้น คุณสามารถใช้ตัวเชื่อมต่อข้อมูลเพื่อดึงค่าจากเอนทิตี้ที่คุณต้องการใช้เป็นมิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="2e28e-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="2e28e-123">คุณสามารถใช้ตัวเชื่อมต่อข้อมูลที่สร้างไว้ล่วงหน้าหรือตัวเชื่อมต่อข้อมูลที่กำหนดเองที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="2e28e-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




