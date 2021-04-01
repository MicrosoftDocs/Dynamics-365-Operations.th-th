---
title: 'สร้างองค์ประกอบต้นทุน  '
description: 'มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11107993fe91e39409ccf06615a21574ad51d079
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236829"
---
# <a name="create-cost-elements"></a><span data-ttu-id="020f2-103">สร้างองค์ประกอบต้นทุน  </span><span class="sxs-lookup"><span data-stu-id="020f2-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="020f2-104">มีหลายวิธีในการสร้างองค์ประกอบต้นทุนในการลงบัญชีต้นทุน </span><span class="sxs-lookup"><span data-stu-id="020f2-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="020f2-105">กระบวนงานนี้แสดงวิธีการสร้างองค์ประกอบต้นทุนโดยการนำเข้าบัญชีหลักผ่านตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="020f2-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="020f2-106">บริษัทสาธิต USMF ถูกนำมาใช้เพื่อสร้างกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="020f2-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="020f2-107">กระบวนงานนี้มีไว้สำหรับคุณลักษณะการลงบัญชีต้นทุนที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="020f2-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="020f2-108">สร้างองค์ประกอบต้นทุนใหม่</span><span class="sxs-lookup"><span data-stu-id="020f2-108">Create new cost elements</span></span>
1. <span data-ttu-id="020f2-109">ไปที่ การลงบัญชีต้นทุนสินค้า > มิติ > มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="020f2-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="020f2-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="020f2-110">Click New.</span></span>
3. <span data-ttu-id="020f2-111">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="020f2-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="020f2-112">ในฟิลด์ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="020f2-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="020f2-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="020f2-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="020f2-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="020f2-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="020f2-115">ตั้งค่าคอนฟิกตัวเชื่อมต่อข้อมูล</span><span class="sxs-lookup"><span data-stu-id="020f2-115">Configure the data connector</span></span>
1. <span data-ttu-id="020f2-116">คลิก ตั้งค่าคอนฟิกตัวให้บริการสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="020f2-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="020f2-117">ในฟิลด์ผังบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="020f2-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="020f2-118">เลือก ใช้ร่วมกัน เพื่อใช้ผังบัญชีร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="020f2-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="020f2-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="020f2-119">Click New.</span></span>
4. <span data-ttu-id="020f2-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="020f2-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="020f2-121">คุณสามารถใช้ตัวกรองบัญชีเพื่อให้ตรงกับเกณฑ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="020f2-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="020f2-122">ในฟิลด์จากบัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="020f2-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="020f2-123">ในฟิลด์ถึงบัญชีลูกค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="020f2-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="020f2-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="020f2-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="020f2-125">นำเข้าบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="020f2-125">Import main accounts</span></span>
1. <span data-ttu-id="020f2-126">คลิก นำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="020f2-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="020f2-127">บัญชีหลักจะถูกนำเข้าไปยังการลงบัญชีต้นทุนสินค้า และใช้เป็นองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="020f2-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="020f2-128">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="020f2-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="020f2-129">ดูบัญชีที่นำเข้าเป็นองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="020f2-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="020f2-130">คลิก ดูสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="020f2-130">Click View dimension members.</span></span>
    * <span data-ttu-id="020f2-131">ดูบัญชีแยกประเภทที่นำเข้าเป็นองค์ประกอบต้นทุนในธุรกิจของคุณที่ต้นทุนสามารถไปได้</span><span class="sxs-lookup"><span data-stu-id="020f2-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]