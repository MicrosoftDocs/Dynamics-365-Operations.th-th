---
title: การแจ้งเตือนลูกค้าทางอีเมล
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งกฎที่ส่งการแจ้งเตือนอีเมลที่เหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ba92c3dc1debed7e98210168d1a135e2cf567aec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191304"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="13c81-103">การแจ้งเตือนลูกค้าทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="13c81-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="13c81-104">คุณสามารถกำหนดกฏการแจ้งเตือนแบบกำหนดเองที่ตรวจสอบมุมมองที่กรองแล้วของข้อมูล และส่งการแจ้งเตือนอีเมลโดยอัตโนมัติ เมื่อเหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="13c81-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="13c81-105">ตัวเลือกในการส่งการแจ้งเตือนอีเมลพร้อมใช้งานสำหรับประเภทการแจ้งเตือนที่รองรับทั้งหมด และยังสามารถถูกเปิดให้กับกฎการแจ้งเตือนที่มีอยู่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="13c81-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="13c81-106">คุณสามารถใช้การควบคุมภายในเพื่อสร้างกฎการแจ้งเตือนที่ตรวจสอบมุมมองที่กรองแล้วของชุดงานของระบบได้</span><span class="sxs-lookup"><span data-stu-id="13c81-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="13c81-107">โดยการตรวจสอบค่าของฟิลด์ **สถานะ** คุณยังสามารถตั้งค่าคอนฟิกกฎการแจ้งเตือนที่ส่งอีเมล เมื่อชุดงานล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="13c81-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="13c81-108">หลังจากการสร้างกฎการแจ้งเตือนเหล่านี้ คุณจะไม่ต้องตรวจสอบรายงานสำหรับการเปลี่ยนแปลงไปยังข้อมูลทางธุรกิจอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="13c81-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="13c81-109">คุณสามารถใช้บริการการตรวจหาการเปลี่ยนแปลงอัจฉริยาทำการตรวจสอบให้คุณแทน</span><span class="sxs-lookup"><span data-stu-id="13c81-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="13c81-110">การแจ้งเตือนไคลเอ็นต์ขึ้นอยู่กับระบบย่อยของอีเมลที่ได้รับผ่านการรวมกับ Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="13c81-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="13c81-111">เราขอแนะนำให้คุณใช้ผู้ให้บริการ Simple Mail Transfer Protocol (SMTP) เพื่อให้การกระจายอีเมลไม่ต้องขึ้นกับไคลเอ็นต์จดหมายท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="13c81-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="13c81-112">เพื่อส่งการแจ้งเตือนทางอีเมล ลูกค้าต้องตั้งค่าคอนฟิกบริการอีเมลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="13c81-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="13c81-113">มีการส่งการแจ้งเตือนทางอีเมลไปยังผู้รับในนามของเจ้าของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="13c81-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="13c81-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกอีเมลใน ดูที่ [ตั้งค่าคอนฟิกและส่งอีเมล](../organization-administration/configure-email.md)</span><span class="sxs-lookup"><span data-stu-id="13c81-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="13c81-115">ภาพต่อไปนี้แสดงกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** ซึ่งรวมตัวเลือก **ส่งอีเมล** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="13c81-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="13c81-116">[![สร้างกล่องโต้ตอบกฎการแจ้งเตือน ที่ซึ่งตัวเลือกส่งอีเมลถูดตั้งเป็น ใช่](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="13c81-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="13c81-117">เมื่อตัวเลือก **ส่งอีเมล** ถูกตั้งเป็น **ใช่** การแจ้งเตือนจะถูกส่งจากศูนย์การดำเนินการต่อไป</span><span class="sxs-lookup"><span data-stu-id="13c81-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="13c81-118">เท็มเพลตอีเมลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="13c81-118">Alert notification email templates</span></span>

<span data-ttu-id="13c81-119">บริการส่งการแจ้งเตือนอีเมลโดยใช้เท็มเพลตอีเมลที่กำหนดไว้ล่วงหน้า ซึ่งจัดส่งรายละเอียดพื้นฐานของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="13c81-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="13c81-120">ภาพต่อไปนี้แสดงโครงสร้างของการแจ้งเตือน เมื่อได้รับทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="13c81-120">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="13c81-121">[![การแจ้งเตือนตามเท็มเพลตสำหรับการสร้างเรกคอร์ด การเปลี่ยนแปลงฟิลด์ และการลบเท็มเพลต](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="13c81-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
