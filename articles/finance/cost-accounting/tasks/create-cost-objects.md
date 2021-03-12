---
title: 'สร้างออบเจ็กต์ต้นทุน  '
description: กระบวนการนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน ลงในบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990778"
---
# <a name="create-cost-objects"></a><span data-ttu-id="b7444-103">สร้างออบเจ็กต์ต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="b7444-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7444-104">กระบวนการนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน ลงในบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b7444-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b7444-105">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="b7444-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="b7444-106">สร้างออบเจ็กต์ต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="b7444-106">Create new cost objects</span></span>
1. <span data-ttu-id="b7444-107">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b7444-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b7444-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b7444-108">Click New.</span></span>
3. <span data-ttu-id="b7444-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="b7444-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b7444-110">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="b7444-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b7444-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b7444-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b7444-112">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b7444-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b7444-113">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b7444-113">Configure the data connector</span></span>
1. <span data-ttu-id="b7444-114">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="b7444-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b7444-115">เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b7444-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b7444-116">ในฟิลด์ชื่อมิติ เลือกศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b7444-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b7444-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b7444-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b7444-118">นำเข้าศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="b7444-118">Import cost centers</span></span>
1. <span data-ttu-id="b7444-119">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="b7444-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="b7444-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b7444-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b7444-121">ดูศูนย์ต้นทุนที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="b7444-121">View the imported cost centers</span></span>
1. <span data-ttu-id="b7444-122">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="b7444-122">Click View dimension members.</span></span>

