---
title: FAQ เกี่ยวกับลำดับงาน
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/01/2019
ms.locfileid: "773235"
---
# <a name="workflow-system"></a><span data-ttu-id="39aac-103">ระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="39aac-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39aac-104">หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="39aac-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="39aac-105">การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="39aac-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="39aac-106">ทำไมได้รับการแจ้งเตือนจำนวนมากเมื่อรายการงานถูกปฏิเสธ?</span><span class="sxs-lookup"><span data-stu-id="39aac-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="39aac-107">เมื่อรายการงานถูกปฏิเสธ รายการงานถูกทำให้เสร็จสมบูรณ์เป็นถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="39aac-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="39aac-108">รายการงานอีกรายการถูกสร้างขึ้น และถูกกำหนดให้กับผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="39aac-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="39aac-109">นี่หมายความว่า มีการแจ้งเตือนไปยังผู้ริเริ่มสำหรับรายการงานที่ถูกปฏิเสธ และการแจ้งเตือนแบบแยกต่างหากของผู้ใช้ที่กำหนดให้กับรายการงาน "การเปลี่ยนแปลงที่ร้องขอ" ใหม่</span><span class="sxs-lookup"><span data-stu-id="39aac-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="39aac-110">การแจ้งเตือนแต่ละรายการมีไว้สำหรับรายการงานที่แตกต่างกัน แต่ความคล้ายคลึงอาจก่อให้เกิดความสับสน</span><span class="sxs-lookup"><span data-stu-id="39aac-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="39aac-111">เรากำลังดูที่วิธีการปรับปรุงรายการนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="39aac-111">We are looking at ways to improve this in a future release.</span></span>
