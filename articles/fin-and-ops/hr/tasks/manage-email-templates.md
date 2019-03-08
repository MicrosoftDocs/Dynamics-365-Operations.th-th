---
title: จัดการเท็มเพลตอีเมล
description: 'คุณสามารถโอนย้ายข้อมูลจากฐานข้อมูลขององค์กรของคุณไปยังที่คั่นหน้าในเอกสารใหม่และใช้ในเทมเพลตซึ่งช่วยให้คุณสื่อสารได้อย่างมีประสิทธิภาพกับผู้สมัครและผู้สมัคร '
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8eface8fd47378e25c7baeca9a84fa41097dfbe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "309621"
---
# <a name="manage-email-templates"></a><span data-ttu-id="4dcad-103">จัดการเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="4dcad-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dcad-104">คุณสามารถโอนย้ายข้อมูลจากฐานข้อมูลขององค์กรของคุณไปยังที่คั่นหน้าในเอกสารใหม่และใช้ในเทมเพลตซึ่งช่วยให้คุณสื่อสารได้อย่างมีประสิทธิภาพกับผู้สมัครและผู้สมัคร </span><span class="sxs-lookup"><span data-stu-id="4dcad-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="4dcad-105">การทำเช่นนี้ คุณต้องสร้างเท็มเพลตที่ประกอบด้วยข้อความมาตรฐานและที่คั่นหน้าที่ควรแทรกข้อมูลของระบบ </span><span class="sxs-lookup"><span data-stu-id="4dcad-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="4dcad-106">ตัวอย่างเช่น คุณสามารถแทรกที่อยู่และข้อมูลผู้ติดต่อสำหรับผู้สมัครลงในเอกสาร Microsoft Word ที่คุณสามารถใช้ได้ เมื่อติดต่อสื่อสารกับผู้สมัครนั้น</span><span class="sxs-lookup"><span data-stu-id="4dcad-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="4dcad-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="4dcad-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="4dcad-108">เลือกที่คั่นหน้าที่จะใช้ในเท็มเพลตอีเมล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4dcad-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="4dcad-109">ไปที่ที่คั่นหน้าใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="4dcad-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="4dcad-110">ในรายการนี้ ให้ค้นหาและเลือกการดำเนินการโต้ตอบที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dcad-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="4dcad-111">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="4dcad-111">Click Edit.</span></span>
4. <span data-ttu-id="4dcad-112">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dcad-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4dcad-113">เลือกฟิลด์คุณต้องการให้สามารถใช้ในเทมเพลตอีเมลสำหรับการดำเนินการโต้ตอบที่เลือก และย้ายไปยังฟิลด์ที่คั่นหน้า</span><span class="sxs-lookup"><span data-stu-id="4dcad-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="4dcad-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4dcad-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="4dcad-115">การสร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="4dcad-115">Create an email template</span></span>
1. <span data-ttu-id="4dcad-116">ไปที่ ทรัพยากรบุคคล > สรรหาบุคลากร > การสื่อสาร > เทมเพลตใบสมัครทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="4dcad-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="4dcad-117">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4dcad-117">Click New.</span></span>
3. <span data-ttu-id="4dcad-118">ในฟิลด์การดำเนินการโต้ตอบ เลือกการสัมภาษณ์</span><span class="sxs-lookup"><span data-stu-id="4dcad-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="4dcad-119">เลือกการดำเนินการโต้ตอบที่ประกอบด้วยที่คั่นหน้าจะใช้สำหรับชนิดการสื่อสารทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="4dcad-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="4dcad-120">ในฟิลด์เทมเพลตอีเมล ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4dcad-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="4dcad-121">ในฟิลด์ชื่อเรื่อง ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4dcad-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="4dcad-122">ในฟิลด์ข้อความ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4dcad-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="4dcad-123">ในรายการนี้ ให้ค้นหาและเลือกที่คั่นหน้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dcad-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="4dcad-124">ดำเนินการพิมพ์อีเมลของคุณและแทรกฟิลด์คั่นหน้าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dcad-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="4dcad-125">ดำเนินการพิมพ์อีเมลของคุณต่อฟิลด์ข้อความที่แทรกคั่นหน้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4dcad-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="4dcad-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4dcad-126">Click Save.</span></span>

