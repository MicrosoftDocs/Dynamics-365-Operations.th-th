---
title: สร้างการจัดโครงแบบตามมิติ
description: 'กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 584bb558ee0afeaffaeb003e9f1d1b0bca42d19d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920692"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="21224-103">สร้างการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="21224-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21224-104">กระบวนงานนี้แสดงวิธีการกำหนดการปรับเปลี่ยนสำหรับผลิตภัณฑ์ตามมิติ </span><span class="sxs-lookup"><span data-stu-id="21224-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="21224-105">นี่คือกระบวนงานสุดท้ายในชุดที่อธิบายถึงวิธีการสร้างชุดงานสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="21224-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="21224-106">การดำเนินการกระบวนงานนี้จะขึ้นอยู่กับข้อมูลที่สร้างขึ้นในการบันทึกเจ็ดรายการก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="21224-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="21224-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="21224-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="21224-108">หาผลิตภัณฑ์หลักตามมิติ</span><span class="sxs-lookup"><span data-stu-id="21224-108">Find the dimension-based product master</span></span>

1. <span data-ttu-id="21224-109">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="21224-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="21224-110">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="21224-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21224-111">เลือกผลิตภัณฑ์หลักตามมิติ ที่คุณสร้างขึ้นในการบันทึกแรกในลำดับงานของการบันทึก 8 รายการนี้</span><span class="sxs-lookup"><span data-stu-id="21224-111">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="21224-112">สร้างการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="21224-112">Create configurations</span></span>

1. <span data-ttu-id="21224-113">ในบานหน้าต่างการดำเนินการ **วิศวกรรม** เลือก **รักษาการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="21224-113">On the **Engineering** Action Pane, select **Maintain configurations**.</span></span>
1. <span data-ttu-id="21224-114">เลือก **ตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="21224-114">Select **Configure**.</span></span>
1. <span data-ttu-id="21224-115">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="21224-115">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="21224-116">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21224-116">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="21224-117">เลือกสินค้าใดๆของกลุ่มการปรับเปลี่ยนแรก</span><span class="sxs-lookup"><span data-stu-id="21224-117">Select any of the items in the first configuration group.</span></span>  
1. <span data-ttu-id="21224-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="21224-118">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="21224-119">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21224-119">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="21224-120">เลือกสินค้าใดๆจากกลุ่มการปรับเปลี่ยนที่สอง</span><span class="sxs-lookup"><span data-stu-id="21224-120">Select any item from the second configuration group.</span></span>  
1. <span data-ttu-id="21224-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="21224-121">Select **OK**.</span></span>
1. <span data-ttu-id="21224-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="21224-122">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="21224-123">ในฟิลด์ **การตั้งค่าคอนฟิก** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21224-123">In the **Configuration** field, type a value.</span></span>
    * <span data-ttu-id="21224-124">ป้อนชื่อของกลุ่มการปรับเปลี่ยนที่จะทำให้ง่ายต่อการระบุการปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="21224-124">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
1. <span data-ttu-id="21224-125">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="21224-125">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="21224-126">ป้อนคำอธิบายของการปรับเปลี่ยนเพื่ออธิบายส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="21224-126">Enter a description of the configuration to explain what it contains.</span></span>  
1. <span data-ttu-id="21224-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="21224-127">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]