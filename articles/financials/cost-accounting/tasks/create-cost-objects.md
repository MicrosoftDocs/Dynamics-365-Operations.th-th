---
title: 'สร้างออบเจ็กต์ต้นทุน  '
description: กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินต้นทุน Dynamics 365 for Finance and Operations Enterprise edition ลงในการบัญชีต้นทุนผ่านทางตัวเชื่อมต่อข้อมูล
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "322685"
---
# <a name="create-cost-objects"></a><span data-ttu-id="e7727-103">สร้างออบเจ็กต์ต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="e7727-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7727-104">กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินต้นทุน Dynamics 365 for Finance and Operations Enterprise edition ลงในการบัญชีต้นทุนผ่านทางตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e7727-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="e7727-105">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="e7727-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="e7727-106">กระบวนงานนี้มีไว้สำหรับคุณลักษณะการลงบัญชีต้นทุนที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="e7727-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="e7727-107">สร้างออบเจ็กต์ต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="e7727-107">Create new cost objects</span></span>
1. <span data-ttu-id="e7727-108">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e7727-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="e7727-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="e7727-109">Click New.</span></span>
3. <span data-ttu-id="e7727-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="e7727-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e7727-111">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="e7727-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="e7727-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="e7727-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e7727-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="e7727-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="e7727-114">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e7727-114">Configure the data connector</span></span>
1. <span data-ttu-id="e7727-115">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="e7727-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="e7727-116">เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e7727-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="e7727-117">ในฟิลด์ชื่อมิติ เลือกศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e7727-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="e7727-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e7727-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="e7727-119">นำเข้าศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="e7727-119">Import cost centers</span></span>
1. <span data-ttu-id="e7727-120">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="e7727-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="e7727-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="e7727-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="e7727-122">ดูศูนย์ต้นทุนที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="e7727-122">View the imported cost centers</span></span>
1. <span data-ttu-id="e7727-123">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="e7727-123">Click View dimension members.</span></span>

