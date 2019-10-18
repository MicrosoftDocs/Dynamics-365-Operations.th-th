---
title: ตั้งค่ากลุ่มสินทรัพย์ถาวร
description: หัวข้อนี้จะอธิบายวิธีการสร้างกลุ่มสินทรัพย์ถาวรใหม่
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186888"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="c2320-103">ตั้งค่ากลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="c2320-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2320-104">หัวข้อนี้จะอธิบายวิธีการสร้างกลุ่มสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="c2320-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="c2320-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="c2320-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="c2320-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > การตั้งค่า > กลุ่มสินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="c2320-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="c2320-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="c2320-107">Select **New**.</span></span>
3. <span data-ttu-id="c2320-108">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="c2320-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="c2320-109">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c2320-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="c2320-110">กำหนดหมายเลขสินทรัพย์ถาวรและลำดับรหัสหมายเลขโดยอัตโนมัติบนกลุ่ม **สินทรัพย์ถาวร** จะแทนที่การตั้งค่าบนพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="c2320-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="c2320-111">คุณสามารถเปลี่ยนได้ที่นี่ถ้าสินทรัพย์ในสินทรัพย์ถาวรมีการกำหนดหมายเลขที่แตกต่างจากกลุ่มอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="c2320-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="c2320-112">เลือก **สมุดบัญชี**</span><span class="sxs-lookup"><span data-stu-id="c2320-112">Select **Books**.</span></span>
6. <span data-ttu-id="c2320-113">ในฟิลด์ **สมุดบัญชี** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="c2320-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="c2320-114">ฟิลด์ **คำนวณค่าเสื่อมราคา** ถูกตั้งค่าเป็น **ใช่** ดังนั้นสมุดบัญชีสินทรัพย์จะถูกรวมในข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="c2320-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="c2320-115">ถ้า **คำนวณค่าเสื่อมราคา** ถูกตั้งค่าเป็น **ไม่** สินทรัพย์จะไม่ถูกคิดค่าเสื่อมราคาโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="c2320-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="c2320-116">ตั้งค่าอายุการใช้งานของสินทรัพย์ในปี</span><span class="sxs-lookup"><span data-stu-id="c2320-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="c2320-117">โปรดทราบว่ามูลค่าของฟิลด์ **รอบระยะเวลาของค่าเสื่อมราคา** จะถูกคำนวณ หลังจากการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c2320-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="c2320-118">ในฟิลด์ **แบบแผนการคิดค่าเสื่อมราคา** ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="c2320-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="c2320-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="c2320-119">Close the page.</span></span>

