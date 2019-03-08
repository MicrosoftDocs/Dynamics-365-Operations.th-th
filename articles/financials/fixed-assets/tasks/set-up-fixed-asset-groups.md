---
title: ตั้งค่ากลุ่มสินทรัพย์ถาวร
description: 'กระบวนงานนี้จะแสดงวิธีการสร้างสินทรัพย์ถาวรใหม่ '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48784ef4eb12a4a1cae3387e3a45afdf34f2a0fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "321811"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="bedd2-103">ตั้งค่ากลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bedd2-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bedd2-104">กระบวนงานนี้จะแสดงวิธีการสร้างสินทรัพย์ถาวรใหม่ </span><span class="sxs-lookup"><span data-stu-id="bedd2-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="bedd2-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="bedd2-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="bedd2-106">ไปที่สินทรัพย์ถาวร > การติดตั้ง > กลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bedd2-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="bedd2-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bedd2-107">Click New.</span></span>
3. <span data-ttu-id="bedd2-108">ในฟิลด์สินทรัพย์ถาวร พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bedd2-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="bedd2-109">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="bedd2-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bedd2-110">กำหนดหมายเลขสินทรัพย์ถาวรและจำนวนลำดับรหัสบนสินทรัพย์ถาวรจะแทนที่การตั้งค่าบนพารามิเตอร์สินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="bedd2-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="bedd2-111">คุณสามารถเปลี่ยนได้ที่นี่ถ้าสินทรัพย์ในสินทรัพย์ถาวรมีการกำหนดหมายเลขที่แตกต่างจากกลุ่มอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="bedd2-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="bedd2-112">คลิก สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="bedd2-112">Click Books.</span></span>
6. <span data-ttu-id="bedd2-113">ในฟิลด์สมุดบัญชี ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="bedd2-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="bedd2-114">ฟิลด์การคำนวณค่าเสื่อมราคาถูกตั้งค่าเป็น ใช่ ดั้งนั้นสมุดบัญชีสินทรัพย์จะรวมกับข้อเสนอค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bedd2-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="bedd2-115">ถ้าการคำนวณค่าเสื่อมราคาถูกตั้งไว้ที่ไม่ สินทรัพย์จะไม่ถูกคิดค่าเสื่อมราคาอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="bedd2-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="bedd2-116">ตั้งค่าอายุการใช้งานของสินทรัพย์ในปี</span><span class="sxs-lookup"><span data-stu-id="bedd2-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="bedd2-117">บันทึกมูลค่าของฟิลด์รอบระยะเวลาการคิดค่าเสื่อมราคาหลังคำนวณการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bedd2-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="bedd2-118">ในฟิลด์การประชุมการเสื่อมราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bedd2-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="bedd2-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bedd2-119">Close the page.</span></span>

