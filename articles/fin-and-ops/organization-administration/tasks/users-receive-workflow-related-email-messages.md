---
title: ให้ผู้ใช้สามารถรับข้อความอีเมลที่เกี่ยวข้องกับลำดับงาน
description: คุณสามารถตั้งค่าคอนฟิกระบบเพื่อส่งข้อความอีเมลไปยังผู้ใช้เมื่อเกิดเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560509"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="5ccaa-103">ให้ผู้ใช้สามารถรับข้อความอีเมลที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="5ccaa-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ccaa-104">คุณสามารถตั้งค่าคอนฟิกระบบเพื่อส่งข้อความอีเมลไปยังผู้ใช้เมื่อเกิดเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="5ccaa-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="5ccaa-105">ตัวอย่างเช่น สามารถส่งข้อความอีเมลให้กับผู้ใช้เมื่อเอกสารถูกกำหนดให้กับผู้ใช้เหล่านั้นเพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="5ccaa-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="5ccaa-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="5ccaa-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5ccaa-107">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="5ccaa-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="5ccaa-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="5ccaa-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5ccaa-109">คลิกตัวเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="5ccaa-109">Click User options.</span></span>
4. <span data-ttu-id="5ccaa-110">คลิกแท็บลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="5ccaa-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="5ccaa-111">ตรวจสอบให้แน่ใจว่ามีการขยายส่วน การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="5ccaa-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="5ccaa-112">ในส่วน การแจ้งเตือน คุณสามารถระบุวิธีที่คุณต้องการให้ผู้ใช้รับการแจ้งเตือนเกี่ยวกับเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="5ccaa-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="5ccaa-113">ในฟิลด์ชนิดการแจ้งเตือนของลำดับงานของสินค้าในรายการ เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="5ccaa-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="5ccaa-114">แบบกลุ่ม – การแจ้งเตือนสำหรับสินค้าในรายการจะถูกจัดกลุ่มลงในข้อความอีเมลเดียว</span><span class="sxs-lookup"><span data-stu-id="5ccaa-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="5ccaa-115">แบบเดี่ยว – ข้อความอีเมลที่ถูกส่งสำหรับสินค้าในรายการแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="5ccaa-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="5ccaa-116">ถ้าคุณต้องการให้ผู้ใช้สามารถได้รับการแจ้งเตือนในไคลเอนต์ เลือกกล่องกาเครื่องหมาย ส่งการแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="5ccaa-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="5ccaa-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="5ccaa-117">Click Save.</span></span>
7. <span data-ttu-id="5ccaa-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="5ccaa-118">Close the page.</span></span>

