--- 
title: "ตั้งค่ากลุ่มสินทรัพย์ถาวร"
description: "กระบวนงานนี้จะแสดงวิธีการสร้างสินทรัพย์ถาวรใหม่ "
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c44ce1219c0fc860d621aa32c8eec7c5d640fa03
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="d5896-103">ตั้งค่ากลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="d5896-103">Set up fixed asset groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5896-104">กระบวนงานนี้จะแสดงวิธีการสร้างสินทรัพย์ถาวรใหม่ </span><span class="sxs-lookup"><span data-stu-id="d5896-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="d5896-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="d5896-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="d5896-106">ไปที่สินทรัพย์ถาวร > การติดตั้ง > กลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="d5896-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="d5896-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d5896-107">Click New.</span></span>
3. <span data-ttu-id="d5896-108">ในฟิลด์สินทรัพย์ถาวร พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d5896-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="d5896-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d5896-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d5896-110">กำหนดหมายเลขสินทรัพย์ถาวรและจำนวนลำดับรหัสบนสินทรัพย์ถาวรจะแทนที่การตั้งค่าบนพารามิเตอร์สินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="d5896-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="d5896-111">คุณสามารถเปลี่ยนได้ที่นี่ถ้าสินทรัพย์ในสินทรัพย์ถาวรมีการกำหนดหมายเลขที่แตกต่างจากกลุ่มอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="d5896-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="d5896-112">คลิก สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="d5896-112">Click Books.</span></span>
6. <span data-ttu-id="d5896-113">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d5896-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d5896-114">ฟิลด์การคำนวณค่าเสื่อมราคาถูกตั้งค่าเป็น ใช่ ดั้งนั้นสมุดบัญชีสินทรัพย์จะรวมกับข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="d5896-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="d5896-115">ถ้าการคำนวณค่าเสื่อมราคาถูกตั้งไว้ที่ไม่ สินทรัพย์จะไม่ถูกคิดค่าเสื่อมราคาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d5896-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="d5896-116">ตั้งค่าอายุการใช้งานของสินทรัพย์ในปี</span><span class="sxs-lookup"><span data-stu-id="d5896-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="d5896-117">บันทึกมูลค่าของฟิลด์รอบระยะเวลาการคิดค่าเสื่อมราคาหลังคำนวณการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d5896-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="d5896-118">ในฟิลด์การประชุมการเสื่อมราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d5896-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="d5896-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d5896-119">Close the page.</span></span>


