---
title: สร้างสินทรัพย์ถาวร
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างเรกคอร์ดสินทรัพย์ถาวรใหม่จากหน้ารายการสินทรัพย์ถาวร
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
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000254"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="ee1ec-103">สร้างสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="ee1ec-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee1ec-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างเรกคอร์ดสินทรัพย์ถาวรใหม่จากหน้ารายการ **สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="ee1ec-105">ระบบจะกำหนดหมายเลขสินทรัพย์ โดยยึดตามลำดับหมายเลขที่กำหนดให้กับกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="ee1ec-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="ee1ec-106">ถ้าคุณใช้เท็มเพลตสินทรัพย์ถาวรเพื่อนำเข้าสินทรัพย์ผ่าน add-in ของ Microsoft Excel หรือถ้าคุณใช้งานนำเข้าอื่น ระบบจะสร้างเรกคอร์ดสินทรัพย์ถาวรและเพิ่มหมายเลขสินทรัพย์โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ee1ec-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="ee1ec-107">เพื่อสร้างเรกคอร์ดสินทรัพย์ด้วยตนเอง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ee1ec-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="ee1ec-108">ไปที่ **บานหน้าต่างนำทาง \> โมดูล \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร \> สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="ee1ec-109">บน **บานหน้าต่างการดำเนินการ** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="ee1ec-110">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="ee1ec-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="ee1ec-111">ฟิลด์ **หมายเลข** จะใช้ค่าเริ่มต้น ถ้าคุณได้เปิดใช้ **ฟังก์ชันการกำหนดหมายเลขสินทรัพย์ถาวรอัตโนมัติ** ใน **พารามิเตอร์สินทรัพย์ถาวร** และ **กลุ่มสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="ee1ec-112">ถ้าไม่ได้เปิดใช้ คุณต้องป้อนหมายเลขเฉพาะเพื่อระบุสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="ee1ec-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="ee1ec-113">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ee1ec-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="ee1ec-114">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสินทรัพย์นี้</span><span class="sxs-lookup"><span data-stu-id="ee1ec-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="ee1ec-115">บน **บานหน้าต่างการดำเนินการ** เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="ee1ec-116">ในฟิลด์ **วันที่ซื้อสินทรัพย์** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ee1ec-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="ee1ec-117">ในฟิลด์ **ราคาที่ซื้อสินทรัพย์** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ee1ec-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="ee1ec-118">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="ee1ec-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="ee1ec-119">ป้อนข้อมูลเพิ่มเติมที่ธุรกิจของคุณจำเป็นต้องใช้สำหรับสมุดบัญชีที่เหลือ</span><span class="sxs-lookup"><span data-stu-id="ee1ec-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="ee1ec-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ee1ec-120">Close the page.</span></span>

<span data-ttu-id="ee1ec-121">นอกจากนี้ คุณยังสามารถนำเข้าสินทรัพย์ถาวรโดยใช้ add-in ของ Excel หรือโดยการรันงานการนำเข้าจากพื้นที่ทำงาน **การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ee1ec-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="ee1ec-122">ก่อนที่คุณจะรันการนำเข้า ให้ป้อนค่าสำหรับฟิลด์ที่จำเป็นในเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="ee1ec-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="ee1ec-123">ถ้าคุณไม่ได้กำหนดหมายเลขสินทรัพย์ถาวรในเท็มเพลตของ add-in ของ Excel หรือในการจัดการข้อมูล ระบบจะสร้างหมายเลขสินทรัพย์ถาวรสำหรับสินทรัพย์ที่นำเข้าแต่ละรายการ และเพิ่มลำดับหมายเลขสำหรับแต่ละสินทรัพย์ให้แต่ละรายการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ee1ec-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="ee1ec-124">อย่างไรก็ตาม ถ้าคุณนำเข้าสินทรัพย์และกำหนดหมายเลขสินทรัพย์ในเท็มเพลต ระบบจะ **ไม่** เพิ่มลำดับหมายเลขโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ee1ec-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="ee1ec-125">ในกรณีนี้ ผู้ดูแลระบบอาจต้องอัพเดตลำดับหมายเลขด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ee1ec-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="ee1ec-126">ถ้าคุณได้กำหนดหมายเลขสินทรัพย์ถาวรในเท็มเพลตของ add-in ของ Excel ระบบจะใช้หมายเลขสินทรัพย์ถาวรที่กำหนดและเพิ่มลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="ee1ec-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>
