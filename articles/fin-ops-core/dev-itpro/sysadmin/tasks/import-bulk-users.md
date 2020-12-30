---
title: นำเข้าผู้ใช้จาก Azure Active Directory
description: กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าผู้ใช้ที่เลือกด้วยตัวเองหรือนำเข้าจำนวนผู้ใช้ปริมาณมากจาก Azure Active Directory
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679825"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="2906d-103">นำเข้าผู้ใช้จาก Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2906d-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="2906d-104">นำเข้าผู้ใช้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2906d-104">Import select users</span></span>

<span data-ttu-id="2906d-105">กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าจำนวนผู้ใช้ที่เลือกจาก Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="2906d-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="2906d-106">ผู้ใช้จะได้รับการนำเข้ากับบริษัทของรอบเวลาปัจจุบันเป็นบริษัทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2906d-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2906d-107">เปลี่ยนบริษัทปัจจุบันถ้ามีก่อนที่จะนำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2906d-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2906d-108">ไปที่ **การดูแลระบบ > ผู้ใช้ > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="2906d-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="2906d-109">คลิก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="2906d-109">Click **Import users**.</span></span>
4. <span data-ttu-id="2906d-110">เลือกผู้ใช้ที่ควรนำเข้าและเลือก **นำเข้าผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="2906d-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="2906d-111">หลังจากการนำเข้าเสร็จสมบูรณ์แล้ว จะต้องกำหนดบทบาทให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2906d-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="2906d-112">นำเข้าผู้ใช้จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="2906d-112">Import users in bulk</span></span>

<span data-ttu-id="2906d-113">กระบวนงานนี้สามารถใช้โดยผู้ดูแลระบบเพื่อนำเข้าจำนวนผู้ใช้ปริมาณมากจาก Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2906d-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="2906d-114">โปรดทราบว่าคุณไม่สามารถเลือกผู้ใช้เมื่อใช้ตัวเลือกการนำเข้าชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2906d-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="2906d-115">เรียกใช้การนำเข้าเป็นชุดงาน</span><span class="sxs-lookup"><span data-stu-id="2906d-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="2906d-116">ผู้ใช้จะได้รับการนำเข้ากับบริษัทของรอบเวลาปัจจุบันเป็นบริษัทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2906d-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="2906d-117">เปลี่ยนบริษัทปัจจุบันถ้ามีก่อนที่จะนำเข้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2906d-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="2906d-118">ไปที่ **การดูแลระบบ > ผู้ใช้ > ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="2906d-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="2906d-119">คลิก **การนำเข้าชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="2906d-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="2906d-120">ขยายส่วน **รันในพื้นหลัง**</span><span class="sxs-lookup"><span data-stu-id="2906d-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="2906d-121">เลือก **ใช่** ในฟิลด์ **การประมวลชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="2906d-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="2906d-122">ในฟิลด์ **กลุ่มชุดงาน** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="2906d-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="2906d-123">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2906d-123">This is an optional step.</span></span>  
7. <span data-ttu-id="2906d-124">เลือก **ใช่** ในฟิลด์ **ส่วนตัว**</span><span class="sxs-lookup"><span data-stu-id="2906d-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="2906d-125">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2906d-125">This is an optional step.</span></span>  
8. <span data-ttu-id="2906d-126">เลือก **ใช่** ในฟิลด์ **งานสำคัญ**</span><span class="sxs-lookup"><span data-stu-id="2906d-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="2906d-127">ขั้นตอนนี้อาจไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="2906d-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="2906d-128">ในฟิลด์ \*\*การตรวจสอบประเภท ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="2906d-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="2906d-129">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2906d-129">Click **OK**.</span></span>

<span data-ttu-id="2906d-130">หลังจากการนำเข้าเสร็จสมบูรณ์แล้ว จะต้องกำหนดบทบาทให้กับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="2906d-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="2906d-131">รันในสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="2906d-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="2906d-132">เลือก **การนำเข้าชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="2906d-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="2906d-133">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2906d-133">Select **OK**.</span></span>
