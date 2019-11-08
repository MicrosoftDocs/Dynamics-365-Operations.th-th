---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent - Core HR (17 มกราคม 2019)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: Darinkramer
manager: AnnBe
ms.date: 01/18/2019
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
ms.search.validFrom: 2019-01-17
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 12a0ce1591bc5d65459efdedaddc67e88710cc73
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550239"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-17-2019"></a><span data-ttu-id="39e39-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent - Core HR (17 มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="39e39-103">What's new or changed in Dynamics 365 Talent - Core HR (January 17, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39e39-104">**สร้าง 8.1.2107**</span><span class="sxs-lookup"><span data-stu-id="39e39-104">**Build 8.1.2107**</span></span>

<span data-ttu-id="39e39-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="39e39-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="minor-changes-and-bug-fixes-included-in-this-release"></a><span data-ttu-id="39e39-106">การเปลี่ยนแปลงเล็กน้อยและการแก้ไขบักรวมอยู่ในรุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="39e39-106">Minor changes and bug fixes included in this release</span></span>

### <a name="new-position-assignment-start-datetime-default-has-been-corrected"></a><span data-ttu-id="39e39-107">ค่าเริ่มต้นของวัน/เวลาเริ่มต้นของการมอบหมายตำแหน่งงานใหม่ได้รับการแก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="39e39-107">New position assignment start date/time default has been corrected</span></span>
<span data-ttu-id="39e39-108">เมื่อโอนย้ายพนักงาน ระบบจะกำหนดค่าเริ่มต้นวัน/เวลาจนถึงวันที่ที่เลือกและเวลาในช่วงเริ่มต้นของวันใหม่ สำหรับโซนเวลาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="39e39-108">When transferring employees, the system will default the date/time to the date selected and the time at the beginning of the day, for the user's time zone.</span></span>

### <a name="all-employees-have-the-same-position-description-in-the-exited-worker-task-management-list"></a><span data-ttu-id="39e39-109">พนักงานทั้งหมดมีคำอธิบายตำแหน่งที่เหมือนกันในรายการการจัดการงานของผู้ปฏิบัติงานที่ออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="39e39-109">All employees have the same position description in the exited worker task management list</span></span>
<span data-ttu-id="39e39-110">มีการอัพเดตในพื้นที่ทำงาน **การจัดการงาน** เพื่อแสดงคำอธิบายตำแหน่งที่ถูกต้องสำหรับพนักงานทั้งหมดที่เพิ่งออกจากบริษัท</span><span class="sxs-lookup"><span data-stu-id="39e39-110">An update has been made in the **Task Management** workspace to display the correct position descriptions for all employees that have recently exited the company.</span></span>

### <a name="action-requested-by-field-is-now-populated-on-workers-action-page"></a><span data-ttu-id="39e39-111">ขณะนี้มีการเติมข้อมูลฟิลด์ "การดำเนินการที่ร้องขอโดย" บนหน้าการดำเนินการของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="39e39-111">"Action requested by" field is now populated on Workers action page</span></span>
<span data-ttu-id="39e39-112">ด้วยการเปลี่ยนแปลงนี้ ขณะนี้ค่าเริ่มต้นสำหรับฟิลด์ **การดำเนินการที่ร้องขอโดย** คือผู้ใช้ที่ร้องขอการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="39e39-112">With this change, the default for the **Action requested by** field is now the user that is requesting the change.</span></span>

### <a name="ideas-portal-updated"></a><span data-ttu-id="39e39-113">พอร์ทัลแนวคิดได้รับการอัพเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="39e39-113">Ideas portal updated</span></span>
<span data-ttu-id="39e39-114">ในลิงก์แอพลิเคชันเพื่อส่งความคิดสำหรับ Talent ได้รับการอัพเดตไปยังพอร์ทัลแนวคิดใหม่แล้ว</span><span class="sxs-lookup"><span data-stu-id="39e39-114">In app links to submit an idea for Talent have been updated to the new Ideas portal.</span></span> <span data-ttu-id="39e39-115">แนวคิดทั้งหมดที่ป้อนในพอร์ทัลเดิมถูกย้าย ดังนั้นแนวคิดที่ดีทั้งหมดของคุณจะยังคงอยู่ในนั้น และพร้อมใช้งานเพื่อที่จะได้ลงคะแนนโดยบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="39e39-115">All ideas entered in the old portal have been migrated, so all your great ideas are still there and available to be voted on by others.</span></span>  

