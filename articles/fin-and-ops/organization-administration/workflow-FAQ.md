---
title: FAQ เกี่ยวกับลำดับงาน
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509302"
---
# <a name="workflow-system"></a><span data-ttu-id="21e4c-103">ระบบลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="21e4c-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21e4c-104">หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="21e4c-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="21e4c-105">การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="21e4c-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="21e4c-106">ทำไมได้รับการแจ้งเตือนจำนวนมากเมื่อรายการงานถูกปฏิเสธ?</span><span class="sxs-lookup"><span data-stu-id="21e4c-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="21e4c-107">เมื่อรายการงานถูกปฏิเสธ รายการงานถูกทำให้เสร็จสมบูรณ์เป็นถูกปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="21e4c-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="21e4c-108">รายการงานอีกรายการถูกสร้างขึ้น และถูกกำหนดให้กับผู้ริเริ่ม</span><span class="sxs-lookup"><span data-stu-id="21e4c-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="21e4c-109">นี่หมายความว่า มีการแจ้งเตือนไปยังผู้ริเริ่มสำหรับรายการงานที่ถูกปฏิเสธ และการแจ้งเตือนแบบแยกต่างหากของผู้ใช้ที่กำหนดให้กับรายการงาน "การเปลี่ยนแปลงที่ร้องขอ" ใหม่</span><span class="sxs-lookup"><span data-stu-id="21e4c-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="21e4c-110">การแจ้งเตือนแต่ละรายการมีไว้สำหรับรายการงานที่แตกต่างกัน แต่ความคล้ายคลึงอาจก่อให้เกิดความสับสน</span><span class="sxs-lookup"><span data-stu-id="21e4c-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="21e4c-111">เรากำลังดูที่วิธีการปรับปรุงรายการนี้ในรุ่นต่อไป</span><span class="sxs-lookup"><span data-stu-id="21e4c-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="21e4c-112">เหตุใดการส่งออกลำดับงานของฉันจึงล้มเหลว?</span><span class="sxs-lookup"><span data-stu-id="21e4c-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="21e4c-113">ขณะนี้มีข้อจำกัดในลักษณะการทำงานในการส่งออกลำดับงานที่ป้องกันไม่ให้ชื่อลำดับงานเกิน 48 อักขระ</span><span class="sxs-lookup"><span data-stu-id="21e4c-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="21e4c-114">การใช้ชื่อที่ยาวกว่า 48 อักขระอาจส่งผลให้เกิดข้อผิดพลาด "เซิร์ฟเวอร์ล้มเหลวในการรับรองความถูกต้องคำขอ" และ/หรือ ป้องกันไม่ให้ไฟล์ถูกส่งออกโดยไม่มีชนิดของไฟล์</span><span class="sxs-lookup"><span data-stu-id="21e4c-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="21e4c-115">โพสต์บล็อกต่อไปนี้ให้รายละเอียดเพิ่มเติม [การแก้ไขปัญหาการส่งออกลำดับงาน](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)</span><span class="sxs-lookup"><span data-stu-id="21e4c-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
