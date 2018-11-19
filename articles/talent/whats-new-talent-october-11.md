---
title: "มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (15 ตุลาคม 2018)"
description: "หัวข้อนี้อธิบายถึงคุณลักษณะใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 for Talent Core HR"
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 1d48bc4bad795611ce322b5f09b78886a50c415c
ms.contentlocale: th-th
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-15-2018"></a><span data-ttu-id="a41e8-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (15 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="a41e8-103">What's new or changed in Dynamics 365 for Talent Core HR (October 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a41e8-104">**สร้าง 8.1.1056**</span><span class="sxs-lookup"><span data-stu-id="a41e8-104">**Build 8.1.1056**</span></span>

<span data-ttu-id="a41e8-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="a41e8-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="a41e8-106">การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="a41e8-106">Changes</span></span>
<span data-ttu-id="a41e8-107">นอกจากการแก้ไขเบ็ดเตล็ด มีการทำการปรับปรุงต่อไปนี้ในรุ่นนี้:</span><span class="sxs-lookup"><span data-stu-id="a41e8-107">In addition to miscellanous fixes, the following updates have been made in this release:</span></span>
- <span data-ttu-id="a41e8-108">ขณะนี้วันสุดท้ายที่ทำงานถูกตั้งค่า เมื่อมีการจ้างงานหรือการตั้งค่าวันที่สิ้นสุดการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="a41e8-108">Last Day worked now set when hiring or setting an employment end date.</span></span>
- <span data-ttu-id="a41e8-109">การอ้างอิงการปฏิบัติตามกฎระเบียบของสหรัฐอเมริกาถูกลบออก เมื่ออยู่ในบริษัทที่ไม่ใช่สหรัฐอเมริกา (ACA ADA และ I9)</span><span class="sxs-lookup"><span data-stu-id="a41e8-109">US compliance references removed when in non US companies (ACA, ADA, and I9).</span></span>
- <span data-ttu-id="a41e8-110">วันที่ไม่ถูกต้อง (1/1/1900) จะถูกซ่อนบนหน้าการวิเคราะห์ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="a41e8-110">Invalid dates (1/1/1900) are now hidden on analytics pages.</span></span>

## <a name="known-issue"></a><span data-ttu-id="a41e8-111">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="a41e8-111">Known issue</span></span>

<span data-ttu-id="a41e8-112">**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="a41e8-112">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="a41e8-113">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a41e8-113">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="a41e8-114">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="a41e8-114">(This issue will be fixed in the next platform update.)</span></span>

