--- 
title: "สร้างออบเจ็กต์ต้นทุน  "
description: "กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน Dynamics 365 for Finance and Operations ลงในการลงบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล"
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2c76a26ea63d1fd44c20fbee271d2767b8ea68b1
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="0fa6a-103">สร้างออบเจ็กต์ต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="0fa6a-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0fa6a-104">กระบวนงานนี้แสดงวิธีการสร้างออบเจ็กต์ต้นทุนโดยการนำเข้ามิติทางการเงินของศูนย์ต้นทุน Dynamics 365 for Finance and Operations ลงในการลงบัญชีต้นทุนสินค้าผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0fa6a-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="0fa6a-105">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="0fa6a-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="0fa6a-106">ขั้นตอนนี้ใช้สำหรับคุณลักษณะการบัญชีต้นทุนที่ถูกเพิ่มเข้ามาใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="0fa6a-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="0fa6a-107">สร้างออบเจ็กต์ต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="0fa6a-107">Create new cost objects</span></span>
1. <span data-ttu-id="0fa6a-108">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0fa6a-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="0fa6a-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0fa6a-109">Click New.</span></span>
3. <span data-ttu-id="0fa6a-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="0fa6a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0fa6a-111">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0fa6a-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="0fa6a-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="0fa6a-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0fa6a-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0fa6a-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="0fa6a-114">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="0fa6a-114">Configure the data connector</span></span>
1. <span data-ttu-id="0fa6a-115">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="0fa6a-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="0fa6a-116">เลือก CostCenter เพื่อนำเข้ามิติ CostCenter ลงในการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0fa6a-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="0fa6a-117">ในฟิลด์ชื่อมิติ เลือกศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0fa6a-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="0fa6a-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0fa6a-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="0fa6a-119">นำเข้าศูนย์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="0fa6a-119">Import cost centers</span></span>
1. <span data-ttu-id="0fa6a-120">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="0fa6a-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="0fa6a-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="0fa6a-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="0fa6a-122">ดูศูนย์ต้นทุนที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="0fa6a-122">View the imported cost centers</span></span>
1. <span data-ttu-id="0fa6a-123">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="0fa6a-123">Click View dimension members.</span></span>


