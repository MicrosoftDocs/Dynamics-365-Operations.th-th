---
title: สร้างหน่วยปฏิบัติงาน
description: หน่วยปฏิบัติงานเป็นองค์กรที่ใช้ในการแบ่งการควบคุมทรัพยากรทางเศรษฐกิจและกระบวนการในการดำเนินงานในธุรกิจหนึ่ง ๆ
author: sericks007
manager: AnnBe
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, OMInternalOrganizationSelector
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38db4a5f93f4b755cfd6fee43eaef27672551077
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143851"
---
# <a name="create-an-operating-unit"></a><span data-ttu-id="d6114-103">สร้างหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="d6114-103">Create an operating unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6114-104">หน่วยปฏิบัติงานเป็นองค์กรที่ใช้ในการแบ่งการควบคุมทรัพยากรทางเศรษฐกิจและกระบวนการในการดำเนินงานในธุรกิจหนึ่ง ๆ</span><span class="sxs-lookup"><span data-stu-id="d6114-104">An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business.</span></span> <span data-ttu-id="d6114-105">บุคลากรในหน่วยปฏิบัติงานมีภาษีการขยายการใช้ทรัพยากร scarce กระบวนการปรับปรุง และบัญชีสำหรับประสิทธิภาพการทำงานของตน</span><span class="sxs-lookup"><span data-stu-id="d6114-105">People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance.</span></span> <span data-ttu-id="d6114-106">ชนิดของหน่วยปฏิบัติงานรวมศูนย์ต้นทุน หน่วยธุรกิจ แผนก มิติ และค่าสตรีม</span><span class="sxs-lookup"><span data-stu-id="d6114-106">The types of operating units include cost centers, business units, departments, and value streams.</span></span> <span data-ttu-id="d6114-107">ใช้ขั้นตอนต่อไปนี้เพื่อสร้างหน่วยปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="d6114-107">Use the following procedure to create an operating unit.</span></span> <span data-ttu-id="d6114-108">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="d6114-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d6114-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการองค์กร > องค์กร > หน่วยปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="d6114-109">Go to **Navigation pane > Modules > Organization administration > Organizations > Operating units.**</span></span>
2. <span data-ttu-id="d6114-110">คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d6114-110">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="d6114-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d6114-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="d6114-112">เลือกชนิดของหน่วยปฏิบัติงานที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="d6114-112">Select the type of operating unit you want to create.</span></span>  
4. <span data-ttu-id="d6114-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d6114-113">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6114-114">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d6114-114">In the **Name** field, type a value.</span></span>
    + <span data-ttu-id="d6114-115">ขยายส่วน **ทั่วไป** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d6114-115">Expand the **General** section, if necessary.</span></span>  
    + <span data-ttu-id="d6114-116">ระบุข้อมูลทั่วไปเกี่ยวกับหน่วยปฏิบัติงานเช่น การระบุรหัสประจำตัว หมายเลข DUNS และผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="d6114-116">Provide general information about the operating unit, such as an identification number, DUNS number, and manager.</span></span>    
    + <span data-ttu-id="d6114-117">ขยายส่วน **ที่อยู่** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d6114-117">Expand the **Addresses** section, if necessary.</span></span>  
    + <span data-ttu-id="d6114-118">ป้อนรายละเอียดที่อยู่เช่น ชื่อถนนและหมายเลข รหัสไปรษณีย์ และเมือง </span><span class="sxs-lookup"><span data-stu-id="d6114-118">Enter address information, such as the street name and number, postal code, and city.</span></span> <span data-ttu-id="d6114-119">คลิก **เพิ่ม** เพื่อป้อนเรกคอร์ดที่อยู่ใหม่ หรือคลิกแก้ไขเพื่อปรับเปลี่ยนเรกคอร์ดที่อยู่เดิม</span><span class="sxs-lookup"><span data-stu-id="d6114-119">Click **Add** to enter a new address record, or click Edit to modify an existing address record.</span></span>   
    + <span data-ttu-id="d6114-120">ขยายส่วน **ข้อมูลผู้ติดต่อ** ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d6114-120">Expand the **Contact information** section, if necessary.</span></span>  
    + <span data-ttu-id="d6114-121">ป้อนข้อมูลเกี่ยวกับวิธีการสื่อสารเช่น ที่อยู่อีเมล URLs และหมายเลขโทรศัพท์ </span><span class="sxs-lookup"><span data-stu-id="d6114-121">Enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span> <span data-ttu-id="d6114-122">เพื่อป้อนเรกคอร์ดการสื่อสารใหม่ ให้คลิกที่ ใหม่ </span><span class="sxs-lookup"><span data-stu-id="d6114-122">To enter a new communication record, click New.</span></span> <span data-ttu-id="d6114-123">เพื่อปรับเปลี่ยนเรกคอร์ดการติดต่อสื่อสารที่มีอยู่ ให้คลิก **ตัวเลือกเพิ่มเติม > ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="d6114-123">To modify an existing communication record, click **More options > Advanced**.</span></span>   
6. <span data-ttu-id="d6114-124">อีกทางหนึ่งคือ เปลี่ยน **หมายเลขหน่วยปฏิบัติงาน** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="d6114-124">Optionally, change the **Operating unit number** as needed.</span></span> <span data-ttu-id="d6114-125">โปรดทราบว่าหมายเลขนี้เป็นตัวระบุที่ไม่ซ้ำกันสำหรับเรกคอร์ด **ฝ่าย** ที่สัมพันธ์กัน และต้องไม่เหมือนกับหน่วยปฏิบัติงานอื่นใดๆ</span><span class="sxs-lookup"><span data-stu-id="d6114-125">Note that this number is a unique idenitifier for the correspondng **Party** record and cannot be the same as any other operating unit.</span></span>
7. <span data-ttu-id="d6114-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d6114-126">Select **Save**.</span></span>
