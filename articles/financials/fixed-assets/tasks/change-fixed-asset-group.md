--- 
title: "เปลี่ยนกลุ่มสินทรัพย์ถาวร"
description: "ควรจะกำหนดสินทรัพย์ถาวรในกลุ่มสินทรัพย์ถาวรที่ถูกต้อง "
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetChangeGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 15e725d409addd46973c2b6a4615c1a50ab75f4d
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="change-a-fixed-asset-group"></a><span data-ttu-id="39287-103">เปลี่ยนกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="39287-103">Change a fixed asset group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39287-104">ควรจะกำหนดสินทรัพย์ถาวรในกลุ่มสินทรัพย์ถาวรที่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="39287-104">Fixed assets should be assigned to the correct fixed assets group.</span></span> <span data-ttu-id="39287-105">กลุ่มสินทรัพย์ถาวรจะถูกนำไปใช้เมื่อคุณ:</span><span class="sxs-lookup"><span data-stu-id="39287-105">The fixed assets group is used when you:</span></span>

 - <span data-ttu-id="39287-106">สร้างการสอบถามและรายงาน</span><span class="sxs-lookup"><span data-stu-id="39287-106">Create inquiries and reports</span></span>

 - <span data-ttu-id="39287-107">ตั้งค่าสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="39287-107">Set up new fixed assets</span></span>

 - <span data-ttu-id="39287-108">รวมบัญชีแยกประเภทและลงรายการบัญชีธุรกรรมสินทรัพย์ถาวรที่บัญชีแยกประเภทที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="39287-108">Integrate ledgers and post fixed asset transactions to the appropriate ledger accounts</span></span>

<span data-ttu-id="39287-109">คำแนะนำนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="39287-109">This guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="39287-110">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="39287-110">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="39287-111">เลือกสินทรัพย์ถาวรที่คุณต้องการจะเปลี่ยนกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="39287-111">Select the fixed asset you would like to change the fixed asset group on.</span></span>
3. <span data-ttu-id="39287-112">คลิก เปลี่ยนกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="39287-112">Click Change fixed asset group.</span></span>
4. <span data-ttu-id="39287-113">ในฟิลด์กลุ่มใหม่ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="39287-113">In the New group field, enter or select a value.</span></span>
5. <span data-ttu-id="39287-114">เลือกตัวเลือกนี้เพื่อกำหนดหมายเลขสินทรัพย์ถาวรให้กับสินทรัพย์ถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="39287-114">Select this option to assign a fixed asset number to the selected fixed asset.</span></span>
    * <span data-ttu-id="39287-115">ฟิลด์หมายเลขสินทรัพย์ถาวรจะพร้อมใช้งานถ้าคุณเลือกตัวเลือกหมายเลขสินทรัพย์ถาวรใหม่ </span><span class="sxs-lookup"><span data-stu-id="39287-115">The Fixed asset number field is available if you select the New fixed asset number option.</span></span>   <span data-ttu-id="39287-116">ถ้าการกำหนดหมายเลขอัตโนมัติถูกตั้งค่าสำหรับสินทรัพย์ถาวร ฟิลด์นี้จะแสดงหมายเลขสินทรัพย์ถาวรที่พร้อมใช้งานถัดไป </span><span class="sxs-lookup"><span data-stu-id="39287-116">If automatic numbering is set up for fixed assets, this field shows the next available fixed asset number.</span></span> <span data-ttu-id="39287-117">คุณสามารถเปลี่ยนหมายเลขได้ </span><span class="sxs-lookup"><span data-stu-id="39287-117">You can change the number.</span></span>   <span data-ttu-id="39287-118">ถ้ามีการตั้งค่าการกำหนดหมายเลขด้วยตนเอง ฟิลด์นี้จะว่างและคุณต้องป้อนหมายเลขสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="39287-118">If manual numbering is set up, this field is blank and you must enter the new fixed asset number.</span></span>     
6. <span data-ttu-id="39287-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="39287-119">Click OK.</span></span>
7. <span data-ttu-id="39287-120">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="39287-120">Click Yes.</span></span>


