---
title: แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683585"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="041f5-103">แก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน</span><span class="sxs-lookup"><span data-stu-id="041f5-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="041f5-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาสำหรับการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="041f5-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="041f5-105">กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาที่เกี่ยวข้องกับการรับรู้โซลูชัน</span><span class="sxs-lookup"><span data-stu-id="041f5-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="041f5-106">ปัญหาบางอย่างที่ที่อยู่ของหัวข้อนี้อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="041f5-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="041f5-107">ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่</span><span class="sxs-lookup"><span data-stu-id="041f5-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="041f5-108">ข้อผิดพลาดในหน้าการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="041f5-108">Error on the Dual-write page</span></span>

<span data-ttu-id="041f5-109">บนหน้า **การรวมแบบสองทิศทาง** คุณอาจได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="041f5-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="041f5-110">*ไม่พบเอนทิตี้ที่มีชื่อว่า 'msdyn\_dualwriteentitymap' with namemapping='Logical' ใน MetadataCache*</span><span class="sxs-lookup"><span data-stu-id="041f5-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="041f5-111">เมื่อต้องการแก้ไขปัญหานี้ โปรดตรวจสอบให้แน่ใจว่าได้ติดตั้งโซลูชันหลักของการรวมแบบสองทิศทางแล้วใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="041f5-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="041f5-112">โซลูชันหลักของการรวมแบบสองทิศทางเป็นข้อกำหนดเบื้องต้นสำหรับการรับรู้โซลูชัน</span><span class="sxs-lookup"><span data-stu-id="041f5-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
