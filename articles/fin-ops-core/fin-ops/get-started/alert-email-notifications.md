---
title: การแจ้งเตือนลูกค้าทางอีเมล
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับวิธีการตั้งกฎที่ส่งการแจ้งเตือนอีเมลที่เหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe422d645c8f2c0c564af30624090828e10ea4bf
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567263"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="2448c-103">การแจ้งเตือนลูกค้าทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="2448c-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2448c-104">คุณสามารถกำหนดกฏการแจ้งเตือนแบบกำหนดเองที่ตรวจสอบมุมมองที่กรองแล้วของข้อมูล และส่งการแจ้งเตือนอีเมลโดยอัตโนมัติ เมื่อเหตุการณ์ที่กำหนดไว้ล่วงหน้าเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2448c-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="2448c-105">ตัวเลือกในการส่งการแจ้งเตือนทางอีเมลพร้อมใช้งานสำหรับชนิดการแจ้งเตือนที่รองรับทั้งหมด และคุณยังสามารถเปิดสำหรับกฎการแจ้งเตือนที่มีอยู่ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="2448c-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="2448c-106">คุณสามารถใช้การควบคุมภายในเพื่อสร้างกฎการแจ้งเตือนที่ตรวจสอบมุมมองที่กรองแล้วของชุดงานของระบบได้</span><span class="sxs-lookup"><span data-stu-id="2448c-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="2448c-107">โดยการตรวจสอบค่าของฟิลด์ **สถานะ** คุณยังสามารถตั้งค่าคอนฟิกกฎการแจ้งเตือนที่ส่งอีเมล เมื่อชุดงานล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="2448c-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="2448c-108">หลังจากที่คุณสร้างกฎการแจ้งเตือนเหล่านี้ คุณจะไม่ต้องตรวจสอบรายงานสำหรับการเปลี่ยนแปลงไปยังข้อมูลทางธุรกิจอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="2448c-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="2448c-109">คุณสามารถใช้บริการการตรวจหาการเปลี่ยนแปลงอัจฉริยาทำการตรวจสอบให้คุณแทน</span><span class="sxs-lookup"><span data-stu-id="2448c-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="2448c-110">การแจ้งเตือนไคลเอ็นต์ขึ้นอยู่กับระบบย่อยของอีเมลที่ได้รับผ่านการรวมกับ Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="2448c-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="2448c-111">เราขอแนะนำให้คุณใช้ผู้ให้บริการ Simple Mail Transfer Protocol (SMTP) เพื่อให้การกระจายอีเมลไม่ต้องขึ้นกับไคลเอ็นต์จดหมายท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="2448c-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="2448c-112">เพื่อส่งการแจ้งเตือนทางอีเมล ลูกค้าต้องตั้งค่าคอนฟิกบริการอีเมลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="2448c-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="2448c-113">มีการส่งการแจ้งเตือนทางอีเมลไปยังผู้รับในนามของเจ้าของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="2448c-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="2448c-114">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกอีเมลใน ดูที่ [ตั้งค่าคอนฟิกและส่งอีเมล](../organization-administration/configure-email.md)</span><span class="sxs-lookup"><span data-stu-id="2448c-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="2448c-115">ภาพต่อไปนี้แสดงกล่องโต้ตอบ **สร้างกฎการแจ้งเตือน** ซึ่งรวมตัวเลือก **ส่งอีเมล** ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="2448c-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="2448c-116">[![สร้างกล่องโต้ตอบกฎการแจ้งเตือน ที่ซึ่งตัวเลือกส่งอีเมลถูดตั้งเป็น ใช่](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="2448c-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2448c-117">เมื่อตัวเลือก **ส่งอีเมล** ถูกตั้งเป็น **ใช่** การแจ้งเตือนจะถูกส่งจากศูนย์การดำเนินการต่อไป</span><span class="sxs-lookup"><span data-stu-id="2448c-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="2448c-118">เท็มเพลตอีเมลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="2448c-118">Alert notification email templates</span></span>

<span data-ttu-id="2448c-119">บริการส่งการแจ้งเตือนอีเมลโดยใช้เท็มเพลตอีเมลที่กำหนดไว้ล่วงหน้า ซึ่งจัดส่งรายละเอียดพื้นฐานของการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="2448c-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="2448c-120">ภาพต่อไปนี้แสดงโครงสร้างของการแจ้งเตือน เมื่อได้รับทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="2448c-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="2448c-121">[![การแจ้งเตือนตามเท็มเพลตสำหรับการสร้างเรกคอร์ด การเปลี่ยนแปลงฟิลด์ และการลบเท็มเพลต](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="2448c-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]