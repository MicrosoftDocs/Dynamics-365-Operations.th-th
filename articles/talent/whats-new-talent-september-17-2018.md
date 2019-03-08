---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (17 กันยายน 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306439"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="cc563-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (17 กันยายน 2018)</span><span class="sxs-lookup"><span data-stu-id="cc563-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc563-104">**สร้าง 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="cc563-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="cc563-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="cc563-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="cc563-106">การลางานและการขาดงาน – เวลาค้างรับค้างจ่ายตามชั่วโมงที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cc563-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="cc563-107">มีการเพิ่มชนิดการรับรู้ใหม่ไปยังแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="cc563-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="cc563-108">ขณะนี้ กำหนดการคงค้างสามารถทำได้ตามเดือนของการบริการหรือชั่วโมงที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="cc563-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="cc563-109">สำหรับข้อมูลเพิ่มเติม ดู [เวลาหยุดพักคงค้างตามชั่วโมงที่ทำงาน](leave-accrue-hours-worked.md)</span><span class="sxs-lookup"><span data-stu-id="cc563-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="cc563-110">แพลตฟอร์ม update 18</span><span class="sxs-lookup"><span data-stu-id="cc563-110">Platform update 18</span></span>

<span data-ttu-id="cc563-111">การปรับปรุงแพลตฟอร์ม 18 เป็นส่วนหนึ่งของการนำออกใช้ Talent ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="cc563-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="cc563-112">คุณจะสามารถซ่อนฟิลด์บังคับและอื่นๆ ได้โดยผ่านการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="cc563-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="cc563-113">ซึ่งช่วยให้ผู้ใช้สามารถสร้างประสบการณ์แบบง่าย ที่ซึ่งฟิลด์บังคับที่เริ่มโดยตรรกะทางธุรกิจ จะไม่แสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="cc563-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="cc563-114">นอกจากนี้ ฟิลด์บังคับที่ซ่อนไว้จะทำให้มองเห็นได้แบบชั่วคราวว่า มีข้อมูลเมื่อมีการพยายามทำการบันทึกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="cc563-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="cc563-115">ในการปรับปรุงแพลตฟอร์ม 18 ขณะนี้ ไคลเอนต์เว็บ Talent จัดเรียงภาพให้ตรงกับ Microsoft Fluent Design</span><span class="sxs-lookup"><span data-stu-id="cc563-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="cc563-116">เมื่อฟิลด์อยู่ใน "โหมดอ่าน" คุณสามารถเลือกตัวเลือกการแก้ไขในฟิลด์ได้โดยง่าย เพื่อสลับแบบฟอร์มเพื่อแก้ไข</span><span class="sxs-lookup"><span data-stu-id="cc563-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="cc563-117">การเปลี่ยนแปลงในวิธีที่ฟิลด์แสดงเมื่ออยู่ในโหมดอ่าน</span><span class="sxs-lookup"><span data-stu-id="cc563-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="cc563-118">หัวข้อในพื้นที่ทำงานและหน้าเป็นตัวหนา</span><span class="sxs-lookup"><span data-stu-id="cc563-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="cc563-119">ลักษณะการทำงานของการค้นหาแบบไม่แทนที่ ได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="cc563-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="cc563-120">สำหรับข้อมูลเพิ่มเติม ดู [ลักษณะการทำงานที่ปรับปรุงแล้วสำหรับการค้นหาแบบไม่แทนที่](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0)</span><span class="sxs-lookup"><span data-stu-id="cc563-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="cc563-121">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="cc563-121">Bug fixes</span></span>

<span data-ttu-id="cc563-122">รุ่นนี้ประกอบด้วยการแก้ไขบักเพิ่มเติมหลายรายการ ซึ่งรวมทั้งการอ้างอิงถึง ACA ADA และ I9 จะถูกเปิดใช้งานในบริษัทในสหรัฐอเมริกาในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="cc563-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
