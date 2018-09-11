--- 
title: "สร้างออบเจ็กต์ต้นทุน  "
description: "กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน Dynamics 365 for Finance and Operations, Enterprise Edition ลงในการลงบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52b5fe092048cd7efe7b0a697cd7061ee0f65103
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="44ea2-103">สร้างออบเจ็กต์ต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="44ea2-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44ea2-104">กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน Dynamics 365 for Finance and Operations, Enterprise Edition ลงในการลงบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="44ea2-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="44ea2-105">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="44ea2-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="44ea2-106">ขั้นตอนนี้ใช้สำหรับคุณลักษณะการบัญชีต้นทุนที่ถูกเพิ่มเข้ามาใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="44ea2-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="44ea2-107">สร้างออบเจ็กต์ต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="44ea2-107">Create new cost objects</span></span>
1. <span data-ttu-id="44ea2-108">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44ea2-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="44ea2-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="44ea2-109">Click New.</span></span>
3. <span data-ttu-id="44ea2-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="44ea2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="44ea2-111">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="44ea2-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="44ea2-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="44ea2-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="44ea2-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="44ea2-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="44ea2-114">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="44ea2-114">Configure the data connector</span></span>
1. <span data-ttu-id="44ea2-115">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="44ea2-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="44ea2-116">เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44ea2-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="44ea2-117">ในฟิลด์ชื่อมิติ เลือกศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44ea2-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="44ea2-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="44ea2-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="44ea2-119">นำเข้าศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="44ea2-119">Import cost centers</span></span>
1. <span data-ttu-id="44ea2-120">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="44ea2-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="44ea2-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="44ea2-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="44ea2-122">ดูศูนย์ต้นทุนที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="44ea2-122">View the imported cost centers</span></span>
1. <span data-ttu-id="44ea2-123">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="44ea2-123">Click View dimension members.</span></span>


