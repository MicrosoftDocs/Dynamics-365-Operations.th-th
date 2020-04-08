---
title: จัดการเท็มเพลตอีเมล
description: หัวข้อนี้อธิบายวิธีการจัดการเท็มเพลตอีเมล
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a911fea9e7d1009160a021e53533c0ce49efbfe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143707"
---
# <a name="manage-email-templates"></a><span data-ttu-id="10573-103">จัดการเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="10573-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10573-104">คุณสามารถโอนย้ายข้อมูลจากฐานข้อมูลขององค์กรของคุณไปยังที่คั่นหน้าในเอกสารใหม่ และใช้ในเท็มเพลตซึ่งช่วยให้คุณสื่อสารได้อย่างมีประสิทธิภาพกับผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="10573-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="10573-105">การทำเช่นนี้ คุณต้องสร้างเท็มเพลตที่ประกอบด้วยข้อความมาตรฐานและที่คั่นหน้าที่ควรแทรกข้อมูลของระบบ </span><span class="sxs-lookup"><span data-stu-id="10573-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="10573-106">ตัวอย่างเช่น คุณสามารถแทรกที่อยู่และข้อมูลผู้ติดต่อสำหรับผู้สมัครลงในเอกสาร Microsoft Word ที่คุณสามารถใช้ได้ เมื่อติดต่อสื่อสารกับผู้สมัครนั้น</span><span class="sxs-lookup"><span data-stu-id="10573-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="10573-107">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="10573-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="10573-108">เลือกที่คั่นหน้าที่จะใช้ในเท็มเพลตอีเมล์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="10573-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="10573-109">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > ทรัพยากรบุคคล > การสรรหาบุคลากร > การสื่อสาร > ที่คั่นหน้าใบสมัคร**</span><span class="sxs-lookup"><span data-stu-id="10573-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="10573-110">ในรายการนี้ ให้ค้นหาและเลือกการดำเนินการโต้ตอบที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10573-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="10573-111">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="10573-111">Select **Edit**.</span></span>
4. <span data-ttu-id="10573-112">เลือกฟิลด์คุณต้องการให้สามารถใช้ในเทมเพลตอีเมลสำหรับการดำเนินการโต้ตอบที่เลือก และย้ายไปยังฟิลด์ที่คั่นหน้า</span><span class="sxs-lookup"><span data-stu-id="10573-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="10573-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10573-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="10573-114">สร้างเท็มเพลตอีเมล</span><span class="sxs-lookup"><span data-stu-id="10573-114">Create an email template</span></span>
1. <span data-ttu-id="10573-115">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > ทรัพยากรบุคคล > การสรรหาบุคลากร > การสื่อสาร > เท็มเพลตอีเมล์ใบสมัคร**</span><span class="sxs-lookup"><span data-stu-id="10573-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="10573-116">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="10573-116">Select **New**.</span></span>
3. <span data-ttu-id="10573-117">ในฟิลด์ **การดำเนินการโต้ตอบ** เลือก **สัมภาษณ์**</span><span class="sxs-lookup"><span data-stu-id="10573-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="10573-118">เลือกการดำเนินการโต้ตอบที่ประกอบด้วยที่คั่นหน้าจะใช้สำหรับชนิดการสื่อสารทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="10573-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="10573-119">ในฟิลด์ **เท็มเพลตอีเมล** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10573-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="10573-120">ในฟิลด์ **ชื่อเรื่อง** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10573-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="10573-121">ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10573-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="10573-122">ในรายการนี้ ให้ค้นหาและเลือกที่คั่นหน้าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10573-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="10573-123">ดำเนินการพิมพ์อีเมลของคุณและแทรกฟิลด์คั่นหน้าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="10573-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="10573-124">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="10573-124">Select **Save**.</span></span>

