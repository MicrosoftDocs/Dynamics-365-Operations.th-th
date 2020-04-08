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
ms.openlocfilehash: db1a372414a38446b7e55d94a3e6a8a22a889d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142811"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="bc28c-103">สร้างสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bc28c-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc28c-104">คู่มือของงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="bc28c-104">This task guide uses the USMF demo company.</span></span>  <span data-ttu-id="bc28c-105">ที่จะสร้างสินทรัพย์ถาวรใหม่โดยใช้หน้ารายการสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bc28c-105">It will create a new fixed asset using the Fixed asset list page.</span></span>

1. <span data-ttu-id="bc28c-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="bc28c-106">Go to **Navigation pane > Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="bc28c-107">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="bc28c-107">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="bc28c-108">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bc28c-108">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="bc28c-109">ฟิลด์ **หมายเลข** จะใช้ค่าเริ่มต้น ถ้าคุณได้เปิดใช้ **ฟังก์ชันการกำหนดหมายเลขสินทรัพย์ถาวรอัตโนมัติ** ใน **พารามิเตอร์สินทรัพย์ถาวร** และ **กลุ่มสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="bc28c-109">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span>  <span data-ttu-id="bc28c-110">ถ้าไม่ได้เปิดใช้ คุณต้องป้อนหมายเลขเฉพาะเพื่อระบุสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bc28c-110">If not, you must enter a unique number to identify the fixed asset.</span></span>  
4. <span data-ttu-id="bc28c-111">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bc28c-111">In the **Name** field, type a value.</span></span> <span data-ttu-id="bc28c-112">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสินทรัพย์นี้</span><span class="sxs-lookup"><span data-stu-id="bc28c-112">Enter the additional information that your business needs for this asset.</span></span>  
5. <span data-ttu-id="bc28c-113">ใน **บานหน้าต่างการดำเนินการ** คลิก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="bc28c-113">On the **Action pane**, click **Books**.</span></span>
6. <span data-ttu-id="bc28c-114">ในฟิลด์ **วันที่ซื้อสินทรัพย์** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="bc28c-114">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="bc28c-115">ในฟิลด์ **ราคาที่ซื้อสินทรัพย์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="bc28c-115">In the **Acquisition price** field, enter a number.</span></span>
    - <span data-ttu-id="bc28c-116">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="bc28c-116">Enter the additional information that your business needs for this book.</span></span>  
    - <span data-ttu-id="bc28c-117">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="bc28c-117">Enter the additional information that your business needs for the remaining books.</span></span>  
8. <span data-ttu-id="bc28c-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bc28c-118">Close the page.</span></span>

