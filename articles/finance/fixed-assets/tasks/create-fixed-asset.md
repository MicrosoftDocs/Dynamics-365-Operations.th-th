---
title: สร้างสินทรัพย์ถาวร
description: คู่มือของงานนี้ใช้บริษัทสาธิต USMF
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59d2b421fcce3551145b85e004380ed06cd45626
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180126"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="d591a-103">สร้างสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="d591a-103">Create a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d591a-104">คู่มือของงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="d591a-104">This task guide uses the USMF demo company.</span></span>  <span data-ttu-id="d591a-105">ที่จะสร้างสินทรัพย์ถาวรใหม่โดยใช้หน้ารายการสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="d591a-105">It will create a new fixed asset using the Fixed asset list page.</span></span>

1. <span data-ttu-id="d591a-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="d591a-106">Go to **Navigation pane > Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="d591a-107">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d591a-107">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="d591a-108">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d591a-108">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="d591a-109">ฟิลด์ **หมายเลข** จะใช้ค่าเริ่มต้น ถ้าคุณได้เปิดใช้ **ฟังก์ชันการกำหนดหมายเลขสินทรัพย์ถาวรอัตโนมัติ** ใน **พารามิเตอร์สินทรัพย์ถาวร** และ **กลุ่มสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="d591a-109">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span>  <span data-ttu-id="d591a-110">ถ้าไม่ได้เปิดใช้ คุณต้องป้อนหมายเลขเฉพาะเพื่อระบุสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="d591a-110">If not, you must enter a unique number to identify the fixed asset.</span></span>  
4. <span data-ttu-id="d591a-111">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d591a-111">In the **Name** field, type a value.</span></span> <span data-ttu-id="d591a-112">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสินทรัพย์นี้</span><span class="sxs-lookup"><span data-stu-id="d591a-112">Enter the additional information that your business needs for this asset.</span></span>  
5. <span data-ttu-id="d591a-113">ใน **บานหน้าต่างการดำเนินการ** คลิก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="d591a-113">On the **Action pane**, click **Books**.</span></span>
6. <span data-ttu-id="d591a-114">ในฟิลด์ **วันที่ซื้อสินทรัพย์** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d591a-114">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="d591a-115">ในฟิลด์ **ราคาที่ซื้อสินทรัพย์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="d591a-115">In the **Acquisition price** field, enter a number.</span></span>
    - <span data-ttu-id="d591a-116">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="d591a-116">Enter the additional information that your business needs for this book.</span></span>  
    - <span data-ttu-id="d591a-117">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="d591a-117">Enter the additional information that your business needs for the remaining books.</span></span>  
8. <span data-ttu-id="d591a-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d591a-118">Close the page.</span></span>

