---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (7 มกราคม 2020)
description: บทความนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462716"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="fe3d8-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (7 มกราคม 2020)</span><span class="sxs-lookup"><span data-stu-id="fe3d8-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="fe3d8-104">บทความนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลงใน Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="fe3d8-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="fe3d8-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="fe3d8-105">Changes in Attract</span></span>

<span data-ttu-id="fe3d8-106">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="fe3d8-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="fe3d8-107">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="fe3d8-107">Changes in Onboard</span></span>

<span data-ttu-id="fe3d8-108">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="fe3d8-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="fe3d8-109">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="fe3d8-109">Changes in Core HR</span></span>

<span data-ttu-id="fe3d8-110">การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2697</span><span class="sxs-lookup"><span data-stu-id="fe3d8-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="fe3d8-111">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="fe3d8-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="fe3d8-112">ไม่สามารถลบผู้ปฏิบัติงานที่ไม่มีเรกคอร์ดการจ้างงานได้ - (386157)</span><span class="sxs-lookup"><span data-stu-id="fe3d8-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="fe3d8-113">การเปลี่ยนแปลงนี้จะเพิ่มตัวเลือกการลบในฟอร์ม **ผู้ปฏิบัติงานที่ไม่มีการจ้างงาน**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="fe3d8-114">ผู้ปฏิบัติงานจะปรากฏในฟอร์มนี้ เมื่อไม่มีจ้างงานในอดีต ในปัจจุบัน หรือในอนาคต สำหรับผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="fe3d8-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="fe3d8-115">ในรุ่นนี้ การลบจะถูกเปิดใช้งานเฉพาะผู้ดูแลระบบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fe3d8-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="fe3d8-116">อย่างไรก็ตาม ในการนำออกใช้ของสัปดาห์ถัดไป จะมีการอัพเดตการรักษาความปลอดภัยเพื่ออนุญาตให้ผู้ใช้ทั้งหมดที่มีบทบาทผู้ช่วยของ HR สามารถลบพนักงานได้โดยไม่มีจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="fe3d8-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="fe3d8-117">นอกจากนี้ คุณยังสามารถทำการเปลี่ยนแปลงเหล่านี้ได้ด้วยตนเองโดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe3d8-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="fe3d8-118">ไปที่ **การตั้งค่าคอนฟิกการรักษาความปลอดภัย**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="fe3d8-119">ในแท็บ **สิทธิ์** ให้กรองรายการ **สิทธิ์** ไปยัง **รักษาผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="fe3d8-120">ในคอลัมน์ **อ้างอิง** เลือก **รายการเมนูที่แสดง**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="fe3d8-121">ใน **รายการเมนูที่แสดง** เลือก **HcmWOrkersWithoutEmployment**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="fe3d8-122">ตั้งค่าสิทธิ์ **ลบ** เพื่อให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="fe3d8-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="fe3d8-123">เลือกแท็บ **ออบเจ็กต์ที่ยังไม่ได้เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="fe3d8-124">เลือก **เผยแพร่ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="fe3d8-124">Select **Publish all**.</span></span>
